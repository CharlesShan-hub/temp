## A.2 The Pulsar Helm chart

Now that we have a Kubernetes cluster up and running, we can deploy containerized applications on top of it. This can be accomplished with a deployment configuration file that contains all the information needed to create all the containers required by your application. These deployment configuration files are simple YAML files that conform to a specific structure, as shown in the following listing, which shows the configuration for a single Ngnix-based web server that listens on port 80 for incoming requests.

Listing A.4 A Kubernetes deployment configuration file

apiVersion: apps/v1              ❶\
kind: Deployment                 ❷\
metadata:\
  name: mysite                   ❸\
  labels:\
    name: mysite\
spec:\
  replicas: 1                    ❹\
  template:\
    metadata:\
      labels:\
        app: mysite\
    spec:\
      containers:                ❺\
        - name: mysite\
          image: ngnix           ❻\
          resources:             ❼\
            limits: \
              memory: “128Mi”\
              cpu: “500m”\
          ports:\
            - containerPort: 80  ❽

❶ Specifies the API version of the configuration file

❷ Specifies the resource type defined in the configuration file

❸ The application name

❹ The number of pods to create

❺ Specifies all of the containers inside each pod

❻ The Docker image name to use

❼ The resources required for the nginx container

❽ The exposed port for the container

Once you have created this file, you can then use the kubectl apply -f filename command to deploy it to your Kubernetes cluster. While this approach is relatively straightforward, it is a bit tedious to have to create and edit all of these verbose files manually. As you can see, the deployment file for a simple, single-container application requires 22 lines of YAML. You can just image how big and complex the deployment file is going to be for an application as complex as Pulsar, which requires multiple instances of multiple containers (brokers, bookies, ZooKeeper, etc.).

Kubernetes-orchestrated container applications can be complex to deploy. Developers can use incorrect inputs for configuration files or not have the expertise to roll out these apps from YAML templates. Therefore, a deployment tool known as Helm was created to simplify the deployment of containerized applications to Kubernetes.


## 子目录

- [A.2.1 What is Helm?](<a.2-the-pulsar-helm-chart/a.2.1-what-is-helm_.md>)
- [A.2.2 The Pulsar Helm chart](<a.2-the-pulsar-helm-chart/a.2.2-the-pulsar-helm-chart.md>)
