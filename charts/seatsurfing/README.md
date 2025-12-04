# seatsurfing

Seatsurfing is a cloud native solution for free seating and co-working in your organisation.

## Usage

Please take a look at the default Values.

In particular, the Seatsurfing specific configuration and the init password should be adjusted.

Please also consider activating cert-manager to create the JWT.

### Install Helm chart

```bash
helm install my-release oci://ghcr.io/credativ/charts/seatsurfing
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| fullnameOverride | string | `""` |  |
| images.name | string | `"backend"` |  |
| images.openssl.name | string | `"openssl"` |  |
| images.openssl.repository | string | `"alpine"` |  |
| images.openssl.tag | string | `"3.5.4"` |  |
| images.pullPolicy | string | `"IfNotPresent"` |  |
| images.repository | string | `"seatsurfing"` |  |
| images.tag | string | `""` |  |
| imagesPullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.httpGet.path | string | `"/"` |  |
| livenessProbe.httpGet.port | string | `"http"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| readinessProbe.httpGet.path | string | `"/"` |  |
| readinessProbe.httpGet.port | string | `"http"` |  |
| resources.limits.cpu | string | `"200m"` |  |
| resources.limits.memory | string | `"512Mi"` |  |
| resources.requests.cpu | string | `"100m"` |  |
| resources.requests.memory | string | `"256Mi"` |  |
| seatsurfing.cryptKey.existingSecret | bool | `false` |  |
| seatsurfing.cryptKey.secretKey | string | `""` |  |
| seatsurfing.cryptKey.secretName | string | `""` |  |
| seatsurfing.cryptKey.value | string | `""` |  |
| seatsurfing.jwt.certManager.duration | string | `"8760h"` |  |
| seatsurfing.jwt.certManager.enabled | bool | `false` |  |
| seatsurfing.jwt.certManager.privateKey.algorithm | string | `"RSA"` |  |
| seatsurfing.jwt.certManager.privateKey.size | int | `4096` |  |
| seatsurfing.jwt.existingSecret.enabled | bool | `false` |  |
| seatsurfing.jwt.existingSecret.secretName | string | `""` |  |
| seatsurfing.jwt.existingSecret.secretPrivateKey | string | `""` |  |
| seatsurfing.jwt.existingSecret.secretPublicKey | string | `""` |  |
| seatsurfing.loginProtection.banMinutes | string | `"5"` |  |
| seatsurfing.loginProtection.maxFails | string | `"10"` |  |
| seatsurfing.loginProtection.slidingWindowSeconds | string | `"600"` |  |
| seatsurfing.organisation.init.domain | string | `"seatsurfing.local"` |  |
| seatsurfing.organisation.init.language | string | `"en"` |  |
| seatsurfing.organisation.init.name | string | `"Sample Company"` |  |
| seatsurfing.organisation.init.password | string | `"12345678"` |  |
| seatsurfing.organisation.init.username | string | `"admin"` |  |
| seatsurfing.organisation.signup.admin | string | `"admin"` |  |
| seatsurfing.organisation.signup.delete | string | `"0"` |  |
| seatsurfing.organisation.signup.domain | string | `".on.seatsurfing.local"` |  |
| seatsurfing.organisation.signup.enabled | string | `"0"` |  |
| seatsurfing.organisation.signup.maxUsers | string | `"50"` |  |
| seatsurfing.postgresql.connectionString.existingSecret | bool | `false` |  |
| seatsurfing.postgresql.connectionString.secretKey | string | `""` |  |
| seatsurfing.postgresql.connectionString.secretName | string | `""` |  |
| seatsurfing.postgresql.database | string | `""` |  |
| seatsurfing.postgresql.hostname | string | `""` |  |
| seatsurfing.postgresql.password.existingSecret | bool | `false` |  |
| seatsurfing.postgresql.password.secretKey | string | `""` |  |
| seatsurfing.postgresql.password.secretName | string | `""` |  |
| seatsurfing.postgresql.password.value | string | `""` |  |
| seatsurfing.postgresql.username | string | `""` |  |
| seatsurfing.smtp.auth | string | `"0"` |  |
| seatsurfing.smtp.enabled | bool | `false` |  |
| seatsurfing.smtp.host | string | `""` |  |
| seatsurfing.smtp.password.existingSecret | bool | `false` |  |
| seatsurfing.smtp.password.secretKey | string | `""` |  |
| seatsurfing.smtp.password.secretName | string | `""` |  |
| seatsurfing.smtp.password.value | string | `""` |  |
| seatsurfing.smtp.port | string | `"0"` |  |
| seatsurfing.smtp.sender_address | string | `""` |  |
| seatsurfing.smtp.starttls | string | `"0"` |  |
| seatsurfing.smtp.username | string | `""` |  |
| securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| securityContext.readOnlyRootFilesystem | bool | `true` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `1000` |  |
| service.annotations | object | `{}` |  |
| service.containerPort | int | `8080` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automount | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| volumeMounts | list | `[]` |  |
| volumes | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
