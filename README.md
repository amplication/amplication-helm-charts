# Amplication-helm-charts

This is a mono-repository for all amplication related helm charts. It is used to version amplication helm charts so that we can differ between helm chart - i.e. kubernetes manifest - related changes in the different environments. In that way changes are in development could be tested in isolation.

Versioning of the helm charts are published to GitHub Packages in the form of OCI images. Additional information on publishing to and consuming from an `oci://` repository can be found [here](https://helm.sh/docs/topics/registries/).
