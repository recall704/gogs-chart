# Helm Chart for Gogs

## Introduction
This [Helm](https://github.com/kubernetes/helm) chart installs [gogs](https://github.com/gogs/gogs) in a Kubernetes cluster. Currently this chart supports Gogs v0.11.53 release. Welcome to contribute to Helm Chart for Gogs.

## Prerequisites

- Kubernetes cluster 1.9+
- Kubernetes Ingress Controller is enabled
- kubectl CLI 1.9+
- Helm CLI 2.8.2+


## Usage

```bash
git clone https://github.com/recall704/gogs-chart.git
cd gogs-chart
helm install --name=gogs-test --set ingress.enabled=true .
```

## Uninstalling the Chart

```bash
helm delete gogs-test
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

You can use NodePort or ingress for Gogs.

| Parameter                  | Description                        | Default                 |
| -----------------------    | ---------------------------------- | ----------------------- |
|              |   |
| `service.svcType`          | gogs service type, `NodePort`/`ClusterIP` | `NodePort`       |
| `service.svcPort`          | gogs service port                  |      `3000`             |
|              |   |
| `ingress.enable`           | enable gogs ingress                | false                   |
| `ingress.hosts`            | gogs ingress hosts                 |  ["gogs.win7.com"]      |

