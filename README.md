[![Test Helm Charts](https://github.com/timescale/helm-charts/actions/workflows/tests.yml/badge.svg)](https://github.com/timescale/helm-charts/actions/workflows/tests.yml)
[![Commit activity](https://img.shields.io/github/commit-activity/m/timescale/helm-charts)](https://github.com/timescale/helm-charts/pulse/monthly)
[![License](https://img.shields.io/github/license/timescale/helm-charts)](https://github.com/timescale/helm-charts/blob/main/LICENSE)
[![Slack](https://img.shields.io/badge/chat-join%20slack-brightgreen.svg)](https://timescaledb.slack.com/)

# About this fork

This is a fork of the official TimescaleDB chart repository. It contains
modifications to the official `timescaledb-single` chart and addresses several pain points in
it:

* Made it possible to specify affinity directly via `affinity`
* The SSL certificate is only generated/mounted if SSL is actually enabled (#284)
* Fixes recovery script claiming that it fetched a file when it didn't (#442)
* Removed default S3 env variables for pgbackrest to allow non-S3 repositories (#389)
* Added pod selector for the primary service (#394)
* ~~Removed the obsolete -pg-version 11 switch from the timescaledb-tune command (#294)~~

# Timescale Helm Charts

This repository contains Helm charts to help with the deployment of
[TimescaleDB](https://github.com/timescale/timescaledb/) and [Promscale](https://github.com/timescale/promscale) on Kubernetes. This
project is currently in active development.

## Repository

The Charts are available in a Helm Chart Repository hosted in Amazon S3 bucket.
The following command will make this repository ready for use:
```
helm repo add timescale 'https://charts.timescale.com/'
```
For more information, have a look at the [Using Helm](https://helm.sh/docs/intro/using_helm/#helm-repo-working-with-repositories) documentation.

## Additional documentation

- [Why use TimescaleDB?](https://docs.timescale.com/introduction)
- [Installing TimescaleDB](https://docs.timescale.com/getting-started/installation)
- [Migrating data to TimescaleDB](https://docs.timescale.com/getting-started/migrating-data)
- [Tutorials and sample data](https://docs.timescale.com/tutorials)
- [Installing Promscale](https://docs.timescale.com/promscale/latest/installation/kubernetes/)

# License

Resources in this repository are released under the [Apache 2.0 license](LICENSE).

# Contributing

If you wish to make contributions to this project, please refer to [Contributor Instructions](CONTRIBUTING.md) for more information.
