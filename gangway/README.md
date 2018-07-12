# Gangway Helm Chart

Installs Heptio's Gangway to easily enable authentication flows via OIDC for a kubernetes cluster.

## Installing the Chart

To install the chart with the release name `my-release`:

```bash
$ helm install --name my-release .
```

## Configuration

The following tables lists the configurable parameters of the Gangway chart and their default values.

| Parameter                  | Description                        | Default                                                    |
| -----------------------    | ---------------------------------- | ---------------------------------------------------------- |
| `replicaCount`             | Number of replicas                 | `1`                                                        | 
| `sessionKey`               | Gangway session key                | `set-manually`                                             |
| `config`                   | Gangway configuration              | `host: 0.0.0.0`                                            |
| `image.repository`         | Image repository                   | `gcr.io/heptio-images/gangway`                             |
| `image.tag`                | Image tag                          | `v2.0.0`                                                   |
| `image.pullPolicy`         | Image pull policy                  | `IfNotPresent`                                             |
| `service.type`             | Service type                       | `ClusterIP`                                                |
| `service.port`             | Service port                       | `80`                                                       |
| `ingress.enabled`          | Use Ingress to expose the service  | `false`                                                    |
| `ingress.annotations`      | Ingress annotations                | `{}`                                                       |
| `ingress.path`             | Ingress path                       | `/`                                                        |
| `ingress.hosts`            | Ingress hosts                      | `[]`                                                       |
| `ingress.tls`              | Ingress tls                        | `[]`                                                       |
| `resources`                | Container resources                | Requests: 100m 128Mi Limits: 200m 512Mi                    |
| `nodeSelector`             | NodeSelector                       | `{}`                                                       |
| `tolerations`              | Tolerations                        | `[]`                                                       |
| `affinity`                 | Affinity                           | `{}`                                                       |

## Example configuration

Take a look at other directories in this repo starting with `gangway-` for how to integrate gangway with various OIDC providers.

