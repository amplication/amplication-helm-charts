# Amplication-helm-charts

This is a mono-repository for all amplication related helm charts. It is used to version amplication helm charts so that we can differ between helm chart - i.e. kubernetes manifest - related changes in the different environments. In that way changes are in development could be tested in isolation.

## Publishing charts
To add the option to lint and publish/release a version of a helm chart, two workflows were introduced. The `lint helm charts` workflow (called lint.yaml) is either triggered manual or through merge a pull request to the main branch. It makes sure the chart is able to be rendered.

When the workflow finishes succesfully, this in turn triggers the workflow for releasing the helm charts, i.e., `release helm charts` (called release.yaml). This workflows releases the changed charts to the github releases of the repository and updates the branch `gh-pages` index.yaml with the metadata about those releases.

## Consuming the charts
Because the charts are versioned they can be consumed accordingly on the side of the `amplication-cluster-configuration` repository. This repository provides additional values per environment against the versioned charts, to be able to determine the desired/rendered-out helm charts.