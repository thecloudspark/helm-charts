# vote-app

![Version: 1.0.4](https://img.shields.io/badge/Version-1.0.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

Helm chart for Vote App

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Romar Cablao | <romarcablao@gmail.com> |  |

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| oci://registry-1.docker.io/bitnamicharts | postgresql | 15.5.4 |
| oci://registry-1.docker.io/bitnamicharts | redis | 19.5.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `"nginx"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hostname | string | `""` |  |
| ingress.tlsEnabled | bool | `false` |  |
| postgresql.auth.password | string | `"postgres"` |  |
| postgresql.auth.username | string | `"postgres"` |  |
| postgresql.primary.resources.limits.cpu | string | `"200m"` |  |
| postgresql.primary.resources.limits.memory | string | `"512Mi"` |  |
| postgresql.primary.resources.requests.cpu | string | `"100m"` |  |
| postgresql.primary.resources.requests.memory | string | `"256Mi"` |  |
| redis.auth.enabled | bool | `false` |  |
| redis.master.count | int | `1` |  |
| redis.master.resources.limits.cpu | string | `"200m"` |  |
| redis.master.resources.limits.memory | string | `"512Mi"` |  |
| redis.master.resources.requests.cpu | string | `"100m"` |  |
| redis.master.resources.requests.memory | string | `"256Mi"` |  |
| redis.replica.replicaCount | int | `0` |  |
| result.enabled | bool | `true` |  |
| result.hpa.enabled | bool | `false` |  |
| result.image | string | `"thecloudspark/app-result:1.0"` |  |
| result.replicas | int | `1` |  |
| result.resources.limits.cpu | string | `"100m"` |  |
| result.resources.limits.memory | string | `"256Mi"` |  |
| result.resources.requests.cpu | string | `"50m"` |  |
| result.resources.requests.memory | string | `"128Mi"` |  |
| result.service.port | int | `80` |  |
| result.service.targetPort | int | `5000` |  |
| result.service.type | string | `"ClusterIP"` |  |
| secret.data.dbPassword | string | `"postgres"` |  |
| secret.data.dbUsername | string | `"postgres"` |  |
| secret.enabled | bool | `true` |  |
| serviceAccount.automount | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `"vote-app"` |  |
| vote.enabled | bool | `true` |  |
| vote.hpa.enabled | bool | `true` |  |
| vote.hpa.maxReplicas | int | `5` |  |
| vote.hpa.minReplicas | int | `1` |  |
| vote.hpa.targetCPUUtilizationPercentage | int | `80` |  |
| vote.image | string | `"thecloudspark/app-vote:1.0"` |  |
| vote.replicas | int | `1` |  |
| vote.resources.limits.cpu | string | `"100m"` |  |
| vote.resources.limits.memory | string | `"128Mi"` |  |
| vote.resources.requests.cpu | string | `"50m"` |  |
| vote.resources.requests.memory | string | `"64Mi"` |  |
| vote.service.port | int | `80` |  |
| vote.service.targetPort | int | `5001` |  |
| vote.service.type | string | `"ClusterIP"` |  |
| worker.enabled | bool | `true` |  |
| worker.hpa.enabled | bool | `false` |  |
| worker.image | string | `"thecloudspark/app-worker:1.0"` |  |
| worker.replicas | int | `1` |  |
| worker.resources.limits.cpu | string | `"100m"` |  |
| worker.resources.limits.memory | string | `"256Mi"` |  |
| worker.resources.requests.cpu | string | `"50m"` |  |
| worker.resources.requests.memory | string | `"128Mi"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
