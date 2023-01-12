# Reployed Helm Charts

[![Release Charts](https://github.com/reployedio/charts/actions/workflows/release.yaml/badge.svg?branch=main)](https://github.com/reployedio/charts/actions/workflows/release.yaml)

A collection of Helm charts, based on the
[bjw-s common library chart](https://github.com/bjw-s/helm-charts/tree/main/charts/library/common).

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```shell
helm repo add reployed https://charts.reployed.io
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
reployed` to see the charts.

To install the <chart-name> chart:

```shell
helm install my-<chart-name> reployed/<chart-name>
```

To uninstall the chart:

```shell
helm delete my-<chart-name>
```

## Chart Overview

| Chart | Description |
| ----- | ----------- |
| [bookstack](charts/bookstack) | A simple, self-hosted, easy-to-use platform for organising and storing information. |
