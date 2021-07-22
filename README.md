# tranql

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: develop-0.0.62](https://img.shields.io/badge/AppVersion-develop--0.0.62-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | redis | 13.0.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| existingRedis.host | string | `""` |  |
| existingRedis.password | string | `""` |  |
| existingRedis.port | string | `""` |  |
| existingRedis.secret | string | `""` |  |
| existingRedis.secretPasswordKey | string | `""` |  |
| gunicorn.workerCount | int | `4` |  |
| gunicorn.workerTimeout | int | `300` |  |
| image | string | `"helxplatform/tranql-app"` |  |
| imageTagOverride | string | `""` | Overrides image tag. default is Chart.appversion |
| ingress.class | string | `nil` |  |
| ingress.enable | bool | `false` |  |
| ingress.host | string | `nil` |  |
| ingress.tls.secretName | string | `nil` |  |
| port | int | `8081` |  |
| redis.cluster.slaveCount | int | `1` |  |
| redis.clusterDomain | string | `"blackbalsam-cluster"` |  |
| redis.configmap | string | `"# Disables appendonly , this instance is readonly. And needs to be\n# seeded from RDB files if needed.\nappendonly no\n# Disable RDB persistence, AOF persistence already enabled.\nsave \"\""` |  |
| redis.enabled | bool | `true` |  |
| redis.image.repository | string | `"redislabs/redisgraph"` |  |
| redis.image.tag | string | `"2.2.14"` |  |
| redis.master.command | string | `""` |  |
| redis.master.extraFlags[0] | string | `"--loadmodule /usr/lib/redis/modules/redisgraph.so"` |  |
| redis.master.livenessProbe.enabled | bool | `false` |  |
| redis.master.readinessProbe.enabled | bool | `false` |  |
| redis.master.resources.requests.cpu | int | `2` |  |
| redis.master.resources.requests.memory | string | `"16Gi"` |  |
| redis.master.service.port | int | `6379` |  |
| redis.persistence.existingClaim | string | `"tranql-redis-pvc"` |  |
| redis.redis.command | string | `"redis-server"` |  |
| redis.slave.command | string | `""` |  |
| redis.slave.extraFlags[0] | string | `"--loadmodule /usr/lib/redis/modules/redisgraph.so"` |  |
| redis.slave.livenessProbe.enabled | bool | `false` |  |
| redis.slave.readinessProbe.enabled | bool | `false` |  |
| redis.slave.resources.requests.cpu | int | `2` |  |
| redis.slave.resources.requests.memory | string | `"16Gi"` |  |
| redis.slave.service.port | int | `6379` |  |
| redis.usePassword | bool | `false` |  |
| redisDumpUri | string | `""` |  |
| replicas | int | `1` |  |
| service.type | string | `"ClusterIP"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
