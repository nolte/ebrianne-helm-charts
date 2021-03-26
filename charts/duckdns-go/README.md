# duckdns-go

[duckdns-go](https://github.com/ebrianne/duckdns-go) is a go-based client to to update, clear ip and records for [DuckDNS](https://www.duckdns.org/) domains.

## TL;DR

```console
$ helm repo add ebrianne.github.io https://ebrianne.github.io/helm-charts
$ helm repo update
$ helm install duckdns-go \
            --namespace default \
            --set duckdns.domains='<domains>' \
            --set duckdns.token='<token>' \
            ebrianne.github.io/duckdns-go
```

## Introduction

This chart bootstraps a duckdns-go deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.18+
- Helm 3.0+

## Installing the Chart

To install the chart with the release name `duckdns-go`:

```console
$ helm install duckdns-go \
            --namespace default \
            --set duckdns.domains='<domains>' \
            --set duckdns.token='<token>' \
            ebrianne.github.io/duckdns-go
```

The command deploys duckdns-go on the Kubernetes cluster in the default configuration. The [Parameters](#parameters) section lists the parameters that can be configured during installation.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `duckdns-go` deployment:

```console
$ helm uninstall duckdns-go
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Parameters

The following table lists the configurable parameters of the duckdns-go chart and their default values.

| Parameter                          | Description                                     | Default                                                 |
|------------------------------------|-------------------------------------------------|---------------------------------------------------------|
| `duckdns.domains`                  | DuckDNS domains (comma separated)               | `""`                                                    |
| `duckdns.token`                    | DuckDNS token                                   | `""`                                                    |
| `image.repository`                 | Docker image repository                         | `ebrianne/duckdns-go`                                   |
| `image.tag`                        | Docker image tag                                | `v1.0.2`                                                |
| `image.pullPolicy`                 | Docker image pull policy                        | `IfNotPresent`                                          |
| `image.pullSecret`                 | Docker image pull secret                        | `nil`                                                   |
| `secret.existingSecret`            | Existing secret                                 | `false`                                                 |
| `secret.existingSecretName`        | Existing secret name                            | `""`                                                    |
| `nameOverride`                     | Name override for the chart                     | `""`                                                    |
| `fullnameOverride`                 | Full name override for the chart                | `""`                                                    |
| `resources`                        | Pod resources                                   | `nil`                                                   |
| `nodeSelector`                     | Node selector                                   | `nil`                                                   |
| `tolerations`                      | Node tolerations                                | `nil`                                                   |
| `affinity`                         | Node affinity                                   | `nil`                                                   |