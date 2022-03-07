# Kubernetees Helm Charts

In simple terms, Helm is a package manager for Kubernetes. Helm is the K8s equivalent of yum or apt. Helm deploys charts, which you can think of as a packaged application. It is a collection of all your versioned, pre-configured application resources which can be deployed as one unit.





To fully grasp helm, there are 3 concepts we need to get familiar with:

* **Chart**: A package of pre-configured Kubernetes resources.
* **Release**: A specific instance of a chart which has been deployed to the cluster using Helm.
* **Repository**: A group of published charts which can be made available to others.

Seldon can be installed via Kustomize and Helm

