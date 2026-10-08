### A.2.1 What is Helm?

Helm is a package manager for Kubernetes that allows developers to easily package, configure, and deploy applications and services onto Kubernetes clusters. It is analogous to Linux package managers such as *YUM* or *APT* because they all allow you to deploy a software package, along with all its dependencies, with a simple command.

We will be using Helm to install our Pulsar cluster, so if you don’t already have Helm installed, you should install it now. If you have a Mac, you can use the Homebrew package manager to install it using a single line, as shown in the following listing. If you are using a different operating system, please consult the online documentation (https://helm.sh/docs/intro/install/) for installation instructions specific to your OS.

Listing A.5 Installing Helm on a MacBook

brew install helm                                        ❶\
. . .\
==\> Downloading https://homebrew.bintray.com/bottles/\
    ➥ helm-3.3.1.catalina.bottle.tar.gz                 ❷\
Already downloaded: /Users/david/Library/Caches/Homebrew/downloads/\
➥ 77e13146a8989356ceaba3a19f6ee6a342427d88975394c91a263ae1c35a3eb6--helm-\
➥ 3.3.1.catalina.bottle.tar.gz\
==\> Pouring helm-3.3.1.catalina.bottle.tar.gz\
==\> Caveats\
Bash completion has been installed to:\
  /usr/local/etc/bash_completion.d\
 \
zsh completions have been installed to:\
  /usr/local/share/zsh/site-functions\
==\> Summary\
![](assets/cup1.png)  /usr/local/Cellar/helm/3.3.1: 56 files, 40.3MB

❶ Using Homebrew to install Helm

❷ Downloading and installing version 3.3.1

Helm allows us to package Kubernetes applications into packages of preconfigured Kubernetes resources, known as *charts*. Helm charts provide push button deployment and deletion of apps, making development and deployment of Kubernetes applications easier for those with little or no container or microservices experience.

Anatomy of a Helm chart

A Helm chart is basically a collection of files inside a directory. The directory name is used as the name of the chart. Within this directory, the Helm chart directory contains a self-descriptor file named chart.yaml, a values.yaml file, and one or more manifest files that are stored in the chart’s template folder, as shown in the following listing.

Listing A.6 The Helm chart directory layout

package-name/\
   charts/\
   templates/          ❶\
   Chart.yaml          ❷\
   values.yaml         ❸\
   requirements.yaml   ❹

❶ Folder of manifest files

❷ The self-descriptor file

❸ Default values used in the templates

❹ Optional list of dependencies

The Helm chart uses the YAML templates for application configuration with a separate value.yaml file to store all the values, which are injected into the template YAML at the time of installation. Essentially, Helm charts can be thought of as Kubernetes files that can be parameterized.

When your chart is ready for deployment, you can use the helm package \<chartname\> command to create a tar-gzipped file containing all the files. Once all this is packaged into a Helm chart, anyone can use it, using the helm install command and providing custom values to the configurations via an external values file or as an argument to the helm install command, and those values are used while creating the Kubernetes application by running the helm install \<chartname\> command.
