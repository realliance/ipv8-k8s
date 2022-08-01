# IPv8 Deployment Manifests

### Preset Overlays

**Nightly** uses all new builds, may outages during version propagation.

### To Deploy Nightly Release

**kustomization.yaml**
```yaml
---
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
namespace: ipv8-nightly
bases:
  - github.com/realliance/ipv8-k8s/overlays/nightly
resources:
  - namespace.yaml
```

**namespace.yaml**
```yaml
---
apiVersion: v1
kind: Namespace
metadata:
  name: ipv8-nightly
```

### Deployment Wishlist

- Sentry for Error Tracking
- Prometheus for Performance Monitoring and Usage Statistics
