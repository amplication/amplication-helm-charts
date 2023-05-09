# amplication-helm-charts

<p align="center">
  <a href="https://amplication.com" target="_blank">
    <img alt="amplication-logo" height="70" alt="Amplication Logo" src="https://amplication.com/images/amplication-logo-purple.svg"/>
  </a>
</p>

This is a mono-repository for all amplication related helm charts. It is used to version amplication helm charts so that we can differ between helm chart - i.e. kubernetes manifest - related changes in the different environments. In that way changes are in development could be tested in isolation.

## Usage

[Helm](https://helm.sh) must be installed to use the charts. Please refer to the [documentation](https://helm.sh/docs) to get started with Helm. Once Helm has been set up correctly, add the repo as follows:

```shell
helm repo add amplication https://amplication.github.io/amplication-helm-charts
```

If you had already added this repo earlier, run `helm repo update` to retrieve the latest versions of the packages. You can then run `helm search repo <alias>` to see the charts that exist for the different components.

To install the <chart-name> chart:

```shell
helm install <chart-name> <alias>/<chart-name>
```

To uninstall the <chart-name> chart:

```shell
helm delete <chart-name>
```

## Publishing charts
To add the option to lint and publish/release a version of a helm chart, a workflows was introduced. It makes sure the chart is able to be rendered, the second part of the workflow releases the changed charts to the github releases of the repository and updates the branch `gh-pages` index.yaml with the metadata about those releases.

## Consuming the charts
Because the charts are versioned they can be consumed accordingly on the side of the `amplication-cluster-configuration` repository. This repository provides additional values per environment against the versioned charts, to be able to determine the desired/rendered-out helm charts.

## Charts

List of the different Amplication component charts that are availale through this repository:

- build-manager
- client
- data-service-generator
- git-pull-request-service
- git-pull-service
- git-push-webhook-service
- miscellaneous
- plugin-api
- server
- storage-gateway
