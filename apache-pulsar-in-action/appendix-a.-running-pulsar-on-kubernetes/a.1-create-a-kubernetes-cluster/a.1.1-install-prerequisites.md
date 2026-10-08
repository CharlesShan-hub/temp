### A.1.1 Install prerequisites

As a prerequisite for working with Kubernetes, you will need to install the Kubernetes command-line tool called kubectl, which allows you to run commands against Kubernetes clusters. You will need this tool to deploy applications, inspect and manage cluster resources, and view logs. If you don’t already have kubectl installed, you should download it (https://kubernetes.io/docs/tasks/tools/#before-you-begin) and follow the instructions for your operating system.

Listing A.1 Installing kubectl on a MacBook

brew install kubectl                                       ❶\
. . .\
==\> Downloading https://homebrew.bintray.com/bottles/\
    ➥ kubernetes-cli-1.19.1.catalina.bottle.tar.gz        ❷\
==\> Pouring kubernetes-cli-1.19.1.catalina.bottle.tar.gz\
==\> Caveats\
Bash completion has been installed to:\
  /usr/local/etc/bash_completion.d\
 \
zsh completions have been installed to:\
  /usr/local/share/zsh/site-functions\
==\> Summary\
    /usr/local/Cellar/kubernetes-cli/1.19.1: 231 files, 49MB

❶ Using Homebrew to install kubectl

❷ Downloading and installing version 1.19.1

If you have a Mac, you can use the Homebrew package manager to install it using a single line, as shown in listing A.1. If you are using a different operating system, please consult the online documentation for installation instructions specific to your OS. You must use a kubectl version that is within one minor version difference of your cluster. Therefore, it is best to use the latest version of kubectl to avoid any compatibility issues.
