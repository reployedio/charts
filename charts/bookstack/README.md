# bookstack

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: version-v22.11.1](https://img.shields.io/badge/AppVersion-version--v22.11.1-informational?style=flat-square)

A simple, self-hosted, easy-to-use platform for organising and storing information.

**This chart is not maintained by the upstream project and any issues with the chart should be raised [here](https://github.com/reployedio/charts/issues/new)**

## Source Code

* <https://bookstackapp.com>
* <https://github.com/BookStackApp/BookStack>
* <https://ghcr.io/linuxserver/bookstack>

## Requirements

Kubernetes: `>=1.22.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://bjw-s.github.io/helm-charts | common | 1.2.1 |
| https://charts.bitnami.com/bitnami | mariadb | 11.4.2 |

## TL;DR

```console
helm repo add reployedio https://charts.reployed.io
helm repo update
helm install bookstack reployedio/bookstack
```

## Installing the Chart

To install the chart with the release name `bookstack`

```console
helm install bookstack reployedio/bookstack
```

## Uninstalling the Chart

To uninstall the `bookstack` deployment

```console
helm uninstall bookstack
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

## Configuration

Read through the [values.yaml](./values.yaml) file. It has several commented out suggested values.
Other values may be used from the [values.yaml](https://github.com/bjw-s/helm-charts/tree/main/charts/library/common/values.yaml) from the [bjw-s common library](https://github.com/bjw-s/helm-charts/tree/main/charts/library/common).

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

```console
helm install bookstack \
  --set env.TZ="Europe/Berlin" \
    reployedio/bookstack
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart.

```console
helm install bookstack reployedio/bookstack -f values.yaml
```

## Custom configuration

N/A

## Values

**Important**: When deploying an application Helm chart you can add more values from the bjw-s common library chart [here](https://github.com/bjw-s/helm-charts/tree/main/charts/library/common)

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | See values.yaml | environment variables.    For more options see [BookStack .env.example](https://github.com/BookStackApp/BookStack/blob/release/.env.example.complete). |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"ghcr.io/linuxserver/bookstack"` | image repository |
| image.tag | string | `"version-v22.11.1"` | image tag |
| ingress.main | object | See values.yaml | Enable and configure ingress settings for the chart under this key. |
| mariadb | object | See values.yaml | Enable and configure mariadb database subchart under this key.    For more options see [mariadb chart documentation](https://github.com/bitnami/charts/tree/master/bitnami/mariadb) |
| persistence.config | object | See values.yaml | Configure persistence settings for the chart under this key. |
| service | object | See values.yaml | Configures service settings for the chart. |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)