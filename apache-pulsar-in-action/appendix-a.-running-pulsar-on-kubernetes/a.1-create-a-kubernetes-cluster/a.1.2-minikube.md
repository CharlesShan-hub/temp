### A.1.2 Minikube

Once kubectl has been installed, the next step is to create a Kubernetes cluster to host the Pulsar cluster. While all of the major cloud vendors provide Kubernetes environments that are well-suited for production use, in this appendix I will use a more cost-effective alternative known as minikube, which allows me to run a Kubernetes cluster on my development machine.

minikube is a tool that runs a single-node Kubernetes cluster on your personal computer. It is well suited for day-to-day development tasks that require access to a containerized application, such as Pulsar. It is a good choice if you want to develop and test your application inside a Kubernetes environment to familiarize yourself with the Kubernetes API.

Listing A.2 Installing minikube on a MacBook

brew install minikube                                                 ❶\
. . .\
==\> Downloading https://homebrew.bintray.com/bottles/minikube-\
    ➥ 1.13.0.catalina.bottle.tar.gz                                  ❷\
Already downloaded: /Users/david/Library/Caches/Homebrew/downloads/\
➥ b4e7b1579cd54deea3070d595b60b315ff7244ada9358412c87ecfd061819d9b--\
➥ minikube-1.13.0.catalina.bottle.tar.gz\
==\> Pouring minikube-1.13.0.catalina.bottle.tar.gz\
==\> Caveats\
Bash completion has been installed to:\
  /usr/local/etc/bash_completion.d\
 \
zsh completions have been installed to:\
  /usr/local/share/zsh/site-functions\
==\> Summary\
![](assets/cup1.png)  /usr/local/Cellar/minikube/1.13.0: 8 files, 62.2MB

❶ Using Homebrew to install minikube

❷ Downloading and installing version 1.13.0

If you don’t already have minikube installed, you should download it (https://minikube.sigs.k8s.io/docs/start/) and follow the instructions for your operating system. If you have a Mac, you can use the Homebrew package manager to install it using a single line, as shown in listing A.2. If you are using a different operating system, please consult the online documentation for installation instructions specific to your OS. After minikube has been installed, the next step is to create a Kubernetes cluster using the commands shown in the following listing. The first command creates the cluster itself and specifies the resources it will claim from my laptop for its resource pool.

Listing A.3 Creating a Kubernetes cluster using minikube

    minikube start \\\
  --memory=8192 \\                       ❶\
  --cpus=4 \\                            ❷\
  --kubernetes-version=v1.19.0           ❸\
 \
kubectl config use-context minikube      ❹

❶ Reserve 8 GB of RAM for the cluster.

❷ Reserve four cores for the cluster.

❸ Specify the version of Kubernetes we will be using.

❹ Set kubectl to use minikube.

In order for the kubectl tool to find and access a Kubernetes cluster, it must first be configured to point to the Kubernetes cluster you wish to interact with. This association is controlled by a kubeconfig file, which is created automatically when you deploy a minikube cluster and is located at ~/.kube/config. You can use the kubectl config use-context \<cluster-name\> command, as shown in listing A.3, to configure the kubectl tool to point to the newly created minikube cluster. You can confirm that the kubectl is properly configured by running the kubectl cluster-info command, which will return basic information about the Kubernetes cluster.
