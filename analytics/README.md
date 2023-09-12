<p align="center">
  <a href="https://amplication.com" target="_blank">
    <img alt="amplication-logo" height="70" alt="Amplication Logo" src="https://amplication.com/images/amplication-logo-purple.svg"/>
  </a>
</p>

---

## Parameters

### analytics parameters

These parameters only apply to the analytics component.

| Name                                 | Description                                                                                                                        | Value                                                                |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `variables.configmap`                | A mapping of key:value to be add to the configmap object (to be used as environment variables on the deployment)                   | `{}`                                                                 |
| `variables.secret`                   | A mapping of key:value to be add to the secret object (to be used as environment variables on the deployment)                      | `{}`                                                                 |
| `variables.externalSecret`           | A mapping of key:values to be added to the external secrets object (turned into a regular secret by the external secrets operator) | `{}`                                                                 |
| `variables.secretStoreConfiguration` | When using external secrets this part of the configuration is used to point to the secret store or cluster secret store            | `{}`                                                                 |
| `cronJob.generic.enabled`            | Whether to enable the generic cronjob                                                                                              | `false`                                                              |
| `cronJob.generic.schedule`           | The unix style cronjob timer                                                                                                       | `*/10 * * * *`                                                       |
| `cronJob.generic.history.successful` | Determine how many successful jobs to keep                                                                                         | `2`                                                                  |
| `cronJob.generic.history.failed`     | Determine how many failed jobs to keep                                                                                             | `2`                                                                  |
| `cronJob.generic.annotations`        | Annotations to be added to the cronjob                                                                                             | `{}`                                                                 |
| `cronJob.generic.imagePullSecrets`   | Reference to Kubernetes secrets housing dockercfg to fetch images from private registries                                          | `[]`                                                                 |
| `cronJob.generic.image.repository`   | Determine from which container repository to pull the image for the generic cronjob                                                | `439403303254.dkr.ecr.us-east-1.amazonaws.com/amplication-analytics` |
| `cronJob.generic.image.pullPolicy`   | Determine when to pull an image for the generic cronjob                                                                            | `IfNotPresent`                                                       |
| `cronJob.generic.image.tag`          | Determine which version of the image to pull from the container repository for the generic cronjob                                 | `""`                                                                 |
| `nameOverride`                       | String to fully override chart name (will maintain the release name)                                                               | `""`                                                                 |
| `fullnameOverride`                   | String to fully override chart name                                                                                                | `""`                                                                 |
| `serviceAccount.create`              | Specifies whether a service account should be created                                                                              | `true`                                                               |
| `serviceAccount.annotations`         | Annotations to add to the service account                                                                                          | `{}`                                                                 |
| `serviceAccount.name`                | The name of the service account to use. If not set and create is true, a name is generated using the fullname template             | `""`                                                                 |
| `resources.requests`                 | The requested CPU & memory for the container                                                                                       | `{}`                                                                 |
| `resources.limits`                   | The CPU & memory limit for the container                                                                                           | `{}`                                                                 |
| `nodeSelector`                       | Node labels for pods assignment                                                                                                    | `{}`                                                                 |
| `tolerations`                        | Tolerations for pods assignment                                                                                                    | `[]`                                                                 |
| `affinity`                           | Affinity for pods assignment                                                                                                       | `{}`                                                                 |
