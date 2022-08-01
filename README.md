# IPv8 Deployment Manifests

## To Deploy Nightly Release
```yaml
---
apiVersion: v1
kind: Namespace
metadata:
  name: ipv8-nightly
---
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
namespace: ipv8-nightly
bases:
  - raw.githubusercontent.com/realliance/ipv8-k8s/main/overlays/nightly
```
