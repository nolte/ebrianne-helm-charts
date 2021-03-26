# A Helm Library for Kubernetes

[![Artifact HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/ebrianne)](https://artifacthub.io/packages/search?repo=ebrianne)

Popular applications, provided by [ebrianne](https://ebrianne.github.io), ready to launch on Kubernetes using [Kubernetes Helm](https://github.com/helm/helm).

## TL;DR

```bash
$ helm repo add ebrianne.github.io https://ebrianne.github.io/helm-charts
$ helm search repo ebrianne.github.io
$ helm install my-release ebrianne.github.io/<chart>
```

## Before you begin

### Prerequisites
- Kubernetes 1.12+
- Helm 3.0+

### Setup a Kubernetes Cluster

For setting up Kubernetes on other cloud platforms or bare-metal servers refer to the Kubernetes [getting started guide](http://kubernetes.io/docs/getting-started-guides/) or using [k3s](https://k3s.io/).

### Install Helm

Helm is a tool for managing Kubernetes charts. Charts are packages of pre-configured Kubernetes resources.

To install Helm, refer to the [Helm install guide](https://github.com/helm/helm#install) and ensure that the `helm` binary is in the `PATH` of your shell.

### Add Repo

The following command allows you to download and install all the charts from this repository:

```bash
$ helm repo add ebrianne.github.io https://ebrianne.github.io/helm-charts
```

### Using Helm

Once you have installed the Helm client, you can deploy a Helm Chart into a Kubernetes cluster.

Please refer to the [Quick Start guide](https://helm.sh/docs/intro/quickstart/) if you wish to get running in just a few commands, otherwise the [Using Helm Guide](https://helm.sh/docs/intro/using_helm/) provides detailed instructions on how to use the Helm client to manage packages on your Kubernetes cluster.

Useful Helm Client Commands:
* View available charts: `helm search repo`
* Install a chart: `helm install my-release ebrianne.github.io/<package-name>`
* Upgrade your application: `helm upgrade`