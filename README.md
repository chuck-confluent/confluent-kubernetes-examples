# Confluent for Kubernetes Scenario Examples

This GitHub repository accompanies the official [Confluent for Kubernetes documentation](https://docs.confluent.io/operator/current/overview.html).

This repository contains scenario workflows to deploy and manage Confluent
on Kubernetes for various use cases.

## Prerequisites

The following prerequisites are assumed for each scenario workflow:

* A Kubernetes cluster - any CNCF conformant version
* Helm 3 installed on your local machine
* Kubectl installed on your local machine
* A namespace created in the Kubernetes cluster - `confluent`
* Kubectl configured to target the `confluent` namespace:
  ```
  kubectl config set-context --current --namespace=confluent
  ```
* This repo cloned to your workstation:
  ```
  git clone git@github.com:confluentinc/confluent-kubernetes-examples.git
  ```

To experiment locally, you can run 
  ```
  ./setup.sh && \       # install helm, k3d, and kubectl
  ./start-k8s.sh        # start kubernetes
  ```
Look at mykube.yml for the k3d configuration (1 API server and 6 worker nodes with labels for rack awareness).