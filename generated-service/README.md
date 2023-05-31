<p align="center">
  <a href="https://amplication.com" target="_blank">
    <img alt="amplication-logo" height="70" alt="Amplication Logo" src="https://amplication.com/images/amplication-logo-purple.svg"/>
  </a>
</p>

---

## Parameters

### generated-service parameters

These parameters only apply to the generated-service component.

| Name                                            | Description                                                                                                            | Value                                                                        |
| ----------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `replicaCount`                                  | Determines the amount of replicas to deploy (only consumed when autoscaling.enabled is set to false).                  | `1`                                                                          |
| `image.repository`                              | Determine from which container repository to pull the image                                                            | `439403303254.dkr.ecr.us-east-1.amazonaws.com/amplication-generated-service` |
| `image.pullPolicy`                              | Determine when to pull an image                                                                                        | `IfNotPresent`                                                               |
| `image.tag`                                     | Determine which version of the image to pull from the container repository                                             | `""`                                                                         |
| `imagePullSecrets`                              | Reference to Kubernetes secrets housing dockercfg to fetch images from private registries                              | `[]`                                                                         |
| `variables.configmap`                           | A mapping of key:value to be add to the configmap object (to be used as environment variables on the deployment)       | `{}`                                                                         |
| `variables.secret`                              | A mapping of key:value to be add to the secret object (to be used as environment variables on the deployment)          | `{}`                                                                         |
| `healthCheck.enabled`                           | Whether to enable the healthcheck on the deployment                                                                    | `false`                                                                      |
| `healthCheck.readinessProbe`                    | A mapping of enabled & path to optionally execute readiness probes                                                     | `{}`                                                                         |
| `healthCheck.livenessProbe`                     | A mapping of enabled & path to optionally execute liveness probes                                                      | `{}`                                                                         |
| `containerPort`                                 | The port number which is exposed on the container image                                                                | `3000`                                                                       |
| `service.type`                                  | The kubernetes service type to be used                                                                                 | `ClusterIP`                                                                  |
| `service.port.http`                             | The port exposed on the service to be used for http traffic                                                            | `80`                                                                         |
| `service.port.https`                            | The port exposed on the service to be used for https traffic                                                           | `443`                                                                        |
| `nameOverride`                                  | String to fully override chart name (will maintain the release name)                                                   | `""`                                                                         |
| `fullnameOverride`                              | String to fully override chart name                                                                                    | `""`                                                                         |
| `serviceAccount.create`                         | Specifies whether a service account should be created                                                                  | `true`                                                                       |
| `serviceAccount.annotations`                    | Annotations to add to the service account                                                                              | `{}`                                                                         |
| `serviceAccount.name`                           | The name of the service account to use. If not set and create is true, a name is generated using the fullname template | `""`                                                                         |
| `podAnnotations`                                | Map of annotations to add to the pods                                                                                  | `{}`                                                                         |
| `podSecurityContext`                            | Security context to add to the pod (overwritten by container-level settings)                                           | `{}`                                                                         |
| `securityContext`                               | Security context to add to the container                                                                               | `{}`                                                                         |
| `ingress.enabled`                               | Enable Kubernetes ingress for ingress traffic                                                                          | `false`                                                                      |
| `ingress.className`                             | Name of the ingress class to use                                                                                       | `""`                                                                         |
| `ingress.annotations`                           | Annotations to add on the ingress object                                                                               | `{}`                                                                         |
| `ingress.hosts`                                 | Hosts configuration for ingress object                                                                                 | `[]`                                                                         |
| `ingress.tls`                                   | TLS configuration for ingress object                                                                                   | `[]`                                                                         |
| `resources.requests`                            | The requested CPU & memory for the container                                                                           | `{}`                                                                         |
| `resources.limits`                              | The CPU & memory limit for the container                                                                               | `{}`                                                                         |
| `autoscaling.enabled`                           | Enable auto scaling (fallback to replicaCount if equals false)                                                         | `false`                                                                      |
| `autoscaling.minReplicas`                       | Minimal amount of replicas to scale down to                                                                            | `1`                                                                          |
| `autoscaling.maxReplicas`                       | Maximum amount of replicas to scale up to                                                                              | `10`                                                                         |
| `autoscaling.targetCPUUtilizationPercentage`    | Increase and decrease the number of replicas to maintain an average % of CPU utilization                               | `80`                                                                         |
| `autoscaling.targetMemoryUtilizationPercentage` | Increase and decrease the number of replicas to maintain an average % of memory utilization                            | `80`                                                                         |
| `nodeSelector`                                  | Node labels for pods assignment                                                                                        | `{}`                                                                         |
| `tolerations`                                   | Tolerations for pods assignment                                                                                        | `[]`                                                                         |
| `affinity`                                      | Affinity for pods assignment                                                                                           | `{}`                                                                         |
