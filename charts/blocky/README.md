# Blocky

DNS proxy / ad-blocker for the local network ([Blocky](https://github.com/0xERR0R/blocky)).

Deploys Blocky plus an optional Redis sidecar. See [values.yaml](values.yaml) for all options.

## Install from GHCR

<!-- x-release-please-start-version -->
```bash
helm install blocky oci://ghcr.io/tobiasgoetz/helm-charts/blocky --version 1.0.0 \
  -n blocky --create-namespace \
  -f values.yaml
```
<!-- x-release-please-end -->
