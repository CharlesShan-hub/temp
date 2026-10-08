## A.3 Using the Pulsar Helm chart

Now that we have downloaded and examined the Pulsar Helm chart, the next step is to use it to provide our Pulsar cluster. The first step in this process is to add the Pulsar Helm chart to your local Helm repository and initialize it, as shown in the following listing. This will allow your local Helm client to locate and download the Pulsar Helm chart.

Listing A.11 Adding the Pulsar Helm chart to your Helm repository

helm repo add apache https://pulsar.apache.org/charts                   ❶\
 \
./scripts/pulsar/prepare_helm_release.sh \\\
 --create-namespace \\                                                  ❷\
 --namepsace pulsar \\                                                  ❸\
 --release pulsar-mini                                                  ❹\
 \
namespace/pulsar created\
generate the token keys for the pulsar cluster                          ❺\
The private key and public key are generated to /var/folders/zw/\
➥ x39hv0dd7133w9v9cgnt1lvr0000gn/T/tmp.QT3EjywR and \
➥ /var/folders/zw/x39hv0dd7133w9v9cgnt1lvr0000gn/T/tmp.YkhhbAyG \
➥ successfully.\
secret/pulsar-mini-token-asymmetric-key created\
generate the tokens for the super-users: proxy-admin,broker-admin,admin\
generate the token for proxy-admin\
secret/pulsar-mini-token-proxy-admin created\
generate the token for broker-admin\
secret/pulsar-mini-token-broker-admin created\
generate the token for admin\
secret/pulsar-mini-token-admin created                                  ❻\
-------------------------------------\
 \
The jwt token secret keys are generated under:                          ❼\
    - 'pulsar-mini-token-asymmetric-key'\
 \
The jwt tokens for superusers are generated and stored as below:        ❽\
    - 'proxy-admin':secret('pulsar-mini-token-proxy-admin')\
    - 'broker-admin':secret('pulsar-mini-token-broker-admin')\
    - 'admin':secret('pulsar-mini-token-admin')

❶ Add the Pulsar Helm repo to your local Helm repo.

❷ Instruct Helm to create the Kubernetes namespace.

❸ The name of the Kubernetes namespace to create

❹ The Pulsar release name

❺ Generating the public and private token files

❻ Generating the tokens for the various admin users

❼ Generating the JWT secret

❽ Generating the JWT access tokens

The final step in the process is to use Helm to install the Pulsar cluster, as shown in the following listing. It is important to specify initialize=true when installing a Pulsar release for the first time because it will ensure that the cluster metadata for both BookKeeper and Pulsar is properly initialized.

Listing A.12 Install Pulsar using the Helm chart

helm install \\\
--set initialize=true \\                    ❶\
--values examples/values-minikube.yaml \\   ❷\
pulsar-mini \\                              ❸\
apache/pulsar                               ❹\
 \
kubectl get pods -n pulsar -o name          ❺\
pod/pulsar-mini-bookie-0\
pod/pulsar-mini-bookie-init-94r5z\
pod/pulsar-mini-broker-0\
pod/pulsar-mini-grafana-6746b4bf69-bjtff\
pod/pulsar-mini-prometheus-5556dbb8b8-m8287\
pod/pulsar-mini-proxy-0\
pod/pulsar-mini-pulsar-init-dmztl\
pod/pulsar-mini-pulsar-manager-6c6889dff-q9t5q\
pod/pulsar-mini-toolset-0\
pod/pulsar-mini-zookeeper-0

❶ Request that the cluster metadata be initialized.

❷ The values file to use

❸ The unique name for this cluster

❹ The Helm chart to use

❺ List all the pods created for the Pulsar cluster.

After Helm has completed the installation process, you can use the kubectl tool to list all of the pods created for the Pulsar cluster and validate that the necessary services are up and running, get the IP addresses, etc.


## 子目录

- [A.3.1 Administering Pulsar on Kubernetes](<a.3-using-the-pulsar-helm-chart/a.3.1-administering-pulsar-on-kubernetes.md>)
- [A.3.2 Configuring clients](<a.3-using-the-pulsar-helm-chart/a.3.2-configuring-clients.md>)
