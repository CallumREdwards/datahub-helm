datahub-mce-consumer
====================
A Helm chart for datahub-mce-consumer

Current chart version is `0.2.0`

## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| exporters.jmx.enabled | boolean | false |  |
| extraEnvs | Extra [environment variables][] which will be appended to the `env:` definition for the container | `[]` |
| extraVolumes | Templatable string of additional `volumes` to be passed to the `tpl` function | "" |
| extraVolumeMounts | Templatable string of additional `volumeMounts` to be passed to the `tpl` function | "" |
| fullnameOverride | string | `""` |  |
| global.kafka.bootstrap.server | string | `"broker:9092"` |  |
| global.kafka.schemaregistry.url | string | `"http://schema-registry:8081"` |  |
| global.datahub.gms.port | string | `"8080"` |  |
| global.hostAliases[0].hostnames[0] | string | `"broker"` |  |
| global.hostAliases[0].hostnames[1] | string | `"mysql"` |  |
| global.hostAliases[0].hostnames[2] | string | `"elasticsearch"` |  |
| global.hostAliases[0].hostnames[3] | string | `"neo4j"` |  |
| global.hostAliases[0].ip | string | `"192.168.0.104"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"linkedin/datahub-mce-consumer"` |  |
| image.tag | string | `"head"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.initialDelaySeconds | int | `60` |  |
| livenessProbe.periodSeconds | int | `30` |  |
| livenessProbe.failureThreshold | int | `4` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| readinessProbe.initialDelaySeconds | int | `60` |  |
| readinessProbe.periodSeconds | int | `30` |  |
| readinessProbe.failureThreshold | int | `4` |  |
| replicaCount | int | `1` |  |
| revisionHistoryLimit | int | `10` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| serviceMonitoring.create | bool | `false` | If set true and `global.datahub.monitoring.enablePrometheus` is set `true` it will create a ServiceMonitor resource |
| tolerations | list | `[]` |  |
| datahub.metadata_service_authentication.enabled | bool | `false` | Whether Metadata Service Authentication is enabled. |
| global.datahub.metadata_service_authentication.systemClientId | string | `"__datahub_system"` | The internal system id that is used to communicate with DataHub GMS. Required if metadata_service_authentication is 'true'. |
| global.datahub.metadata_service_authentication.systemClientSecret.secretRef | string | `nil` | The reference to a secret containing the internal system secret that is used to communicate with DataHub GMS. Required if metadata_service_authentication is 'true'. |
| global.datahub.metadata_service_authentication.systemClientSecret.secretKey | string | `nil` | The key of a secret containing the internal system secret that is used to communicate with DataHub GMS. Required if metadata_service_authentication is 'true'. |
