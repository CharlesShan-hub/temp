### A.3.1 Administering Pulsar on Kubernetes

Once you have deployed a Pulsar cluster to a Kubernetes environment, one of your first concerns will be deciding how to administer the pulsar cluster. Fortunately, the Pulsar Helm chart creates a pod named pulsar-mini-toolset-0 that contains the pulsar-admin CLI tool, which is already configured to interact with the deployed Pulsar cluster. Consequently, all that is required to administer the cluster is to use the kubectl exec command to access the pod and execute the commands directly against the cluster, as shown in the following listing.

Listing A.13 Administering Pulsar on Kubernetes

kubectl exec -it -n pulsar pulsar-mini-toolset-0 /bin/bash\
 \
bin/pulsar-admin tenants create manning  \
 \
bin/pulsar-admin tenants list   \
  \
"manning"\
"public"\
"pulsar"

Since the pulsar-admin CLI tool is the same for both the Kubernetes cluster and the Docker standalone container, the docker exec and kubectl exec commands can be used interchangeably throughout this book if you choose to follow the examples using Kubernetes rather than Docker. For more details on the pulsar-admin CLI, please refer to the documentation.
