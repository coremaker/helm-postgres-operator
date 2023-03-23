[![Maintained by coremaker.io](https://img.shields.io/badge/maintained%20by-coremaker.io-green)](https://coremaker.io/)
# Postgres Operator

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add postgres-operator https://coremaker.github.io/helm-postgres-operator

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
postgres-operator` to see the charts.

To install the postgres-operator chart:

    helm install my-postgres-operator postgres-operator/postgres-operator

To uninstall the chart:

    helm delete my-postgres-operator

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| controller.container.image.repository | string | `"europe-docker.pkg.dev/coremaker/eu.gcr.io/postgres-operator"` |  |
| controller.container.image.tag | string | `"v1.0.8"` |  |
| controller.container.logging.encoder | string | `"json"` |  |
| controller.container.logging.log_level | string | `"info"` |  |
| controller.container.logging.stacktrace_level | string | `"panic"` |  |
| controller.container.resources.limits.cpu | string | `"500m"` |  |
| controller.container.resources.limits.memory | string | `"128Mi"` |  |
| controller.container.resources.requests.cpu | string | `"10m"` |  |
| controller.container.resources.requests.memory | string | `"64Mi"` |  |
| controller.replicas | int | `1` |  |
| crds.install | bool | `true` |  |
| fullnameOverride | string | `nil` |  |
| nameOverride | string | `nil` |  |
| rbac.create | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |

----------------------------------------------
