<p align="center">
  <a href="https://amplication.com" target="_blank">
    <img alt="amplication-logo" height="70" alt="Amplication Logo" src="https://amplication.com/images/amplication-logo-purple.svg"/>
  </a>
</p>

---

## Parameters

### miscellaneous parameters

These parameters only apply to the miscellaneous component.

| Name                                                      | Description                                                                                                                        | Value            |
| --------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------- |
| `namespace.names`                                         | List of namespaces which to create and possibly annotate with istio-injection                                                      | `[]`             |
| `imagePullSecretSetup.enabled`                            | Boolean for enabling the cronjob that creates a dockercfg secret for ecr authentication                                            | `false`          |
| `imagePullSecretSetup.cronJob.schedule`                   | The cronjob timer on which to run the image pull secret creation job                                                               | `*/10 * * * *`   |
| `imagePullSecretSetup.cronJob.history.successful`         | The amount of succesful jobs to keep                                                                                               | `2`              |
| `imagePullSecretSetup.cronJob.history.failed`             | The amount of failed jobs to keep                                                                                                  | `2`              |
| `imagePullSecretSetup.cronJob.annotations`                | The annotations to add to the job template                                                                                         | `{}`             |
| `imagePullSecretSetup.variables.secret`                   | A mapping of key:value to be add to the secret object (to be used as environment variables on the deployment)                      | `{}`             |
| `imagePullSecretSetup.variables.externalSecret`           | A mapping of key:values to be added to the external secrets object (turned into a regular secret by the external secrets operator) | `{}`             |
| `imagePullSecretSetup.variables.secretStoreConfiguration` | When using external secrets this part of the configuration is used to point to the secret store or cluster secret store            | `{}`             |
| `storageClass.main.enabled`                               | Boolean to enable or disable the main storage class                                                                                | `true`           |
| `storageClass.main.name`                                  | String the name for the main efs based storage class                                                                               | `efs-main-sc`    |
| `storageClass.main.provisioningMode`                      | String the provisiong mode for the main efs                                                                                        | `efs-ap`         |
| `storageClass.main.id`                                    | String the provisiong id for the main efs                                                                                          | `<provising-id>` |
| `storageClass.main.directoryPerms`                        |                                                                                                                                    | `755`            |
| `storageClass.main.gidRangeStart`                         | String group id range start for the permissions on the main storage class                                                          | `1000`           |
| `storageClass.main.gidRangeEnd`                           | String group id range end for the permissions on the main storage class                                                            | `2000`           |
| `storageClass.dsg.enabled`                                | Boolean to enable or disable the dsg storage class                                                                                 | `true`           |
| `storageClass.dsg.name`                                   | String the name for the dsg efs based storage class                                                                                | `efs-dsg-sc`     |
| `storageClass.dsg.provisioningMode`                       | String the provisiong mode for the dsg efs                                                                                         | `efs-ap`         |
| `storageClass.dsg.id`                                     | String the provisiong id for the dsg efs                                                                                           | `<provising-id>` |
| `storageClass.dsg.directoryPerms`                         | String unix style permissions on the dsg storage class                                                                             | `755`            |
| `storageClass.dsg.gidRangeStart`                          | String group id range start for the permissions on the dsg storage class                                                           | `1000`           |
| `storageClass.dsg.gidRangeEnd`                            | String group id range end for the permissions on the dsg storage class                                                             | `2000`           |
| `nameOverride`                                            | String to fully override chart name (will maintain the release name)                                                               | `""`             |
| `fullnameOverride`                                        | String to fully override chart name                                                                                                | `""`             |
| `serviceAccount.create`                                   | Specifies whether a service account should be created                                                                              | `true`           |
| `serviceAccount.annotations`                              | Annotations to add to the service account                                                                                          | `{}`             |
| `serviceAccount.name`                                     | The name of the service account to use. If not set and create is true, a name is generated using the fullname template             | `""`             |
| `rbac.enabled`                                            | Boolean for adding the role & role-binding setup required for creating ecr dockercfg secrets                                       | `true`           |
