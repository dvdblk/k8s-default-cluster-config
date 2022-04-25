# K8s cluster config

Helmfiles that configure a single node k8s cluster.

Apps used:
  * NGINX Ingress Controller
  * Cert Manager
  * OAuth2 Proxy
  * Prometheus
  * Argo CD
  * Ingress for k8s dashboard

## Install

Create an `.env` file with valid environment variables. Then:

```
# Install helmfile
$ brew install helmfile

# Add helm diff plugin
$ helm plugin install https://github.com/databus23/helm-diff

# Export all ENV variables
$ export $(xargs <.env)

# Apply helmfile
$ helmfile apply --suppress-diff
```