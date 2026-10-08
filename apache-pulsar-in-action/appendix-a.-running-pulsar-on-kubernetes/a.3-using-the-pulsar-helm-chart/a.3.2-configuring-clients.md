### A.3.2 Configuring clients

The main challenge with connecting to a Pulsar cluster inside a K8s environment is finding the ports that the cluster is listening on. The default binary port, 6650 and HTTP admin port, 8080 are not exposed outside of the K8s environment. Therefore, you first need to determine where these node ports are mapped to.

By default, the Pulsar Helm chart exposes the Pulsar cluster through a Kubernetes load balancer. In minikube, you can use the command shown in listing A.14 to check the proxy service. The output from this command will tell us which node ports the Pulsar cluster’s binary port and HTTP port are mapped to. The port after 80: is the HTTP port, while the port after 6650: is the binary port.

Listing A.14 Determining the Pulsar Client ports

\$kubectl get services -n pulsar \| grep pulsar-mini-proxy                  ❶\
 \
pulsar-mini-proxy            LoadBalancer   10.110.67.72     \<pending\>     \
➥ 80:30210/TCP,6650:32208/TCP   4h16m                                    ❷\
 \
\$minikube service pulsar-mini-proxy -n pulsar --url                       ❸\
http://192.168.64.3:30210                                                 ❹\
http://192.168.64.3:32208                                                 ❺

❶ Command to determine port mappings

❷ The output tells us port 80 is mapped to port 30210, and port 6650 is mapped to port 32208.

❸ Command to find the IP address of the exposed ports inside minikube

❹ The proxy’s HTTP URL

❺ The proxy’s binary URL

At this point, you have service URLs you need to connect your clients to the Pulsar cluster running inside minikube, and you can use them, along with required security tokens that we generated earlier when configuring your Pulsar clients to interact with the cluster.
