# IAM Authenticator Helm Chart

Installs Heptio's IAM Authenticator (server components) to easily enable authentication with IAM on an existing Kubernetes cluster.

## Installing the Chart

To install the chart with the release name `my-release`:

```bash
$ helm install --name my-release .
```

## Configuration

The following tables lists the configurable parameters of the Gangway chart and their default values.

| Parameter                  | Description                        | Default                                                    |
| -----------------------    | ---------------------------------- | ---------------------------------------------------------- |
| `clusterID`                | Unique identifier of the cluster   | **REQUIRED**                                               |
| `image.repository`         | Image repository                   | `gcr.io/heptio-images/authenticator`                       |
| `image.tag`                | Image tag                          | `v0.3.0`                                                   |
| `resources`                | Container resources                | Requests: 10m 20Mi Limits: 100m 20Mi                       |
| `nodeSelector`             | NodeSelector                       | `node-role.kubernetes.io/master: ""`                       |
| `tolerations`              | Tolerations                        | Attached to masters                                        |
| `mapRoles`                 | The role mappings                  | `{}`                                                       |

## Initial Installation Instructions

