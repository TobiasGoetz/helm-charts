# Home Assistant

[Home Assistant](https://www.home-assistant.io/) on Kubernetes, with optional Matter server, Authentik OIDC, and Prometheus scraping.

See [values.yaml](values.yaml) for all options.

## Install from GHCR

<!-- x-release-please-start-version -->
```bash
helm install home-assistant oci://ghcr.io/tobiasgoetz/helm-charts/home-assistant --version 1.2.11 \
  -n home-assistant --create-namespace \
  -f values.yaml
```
<!-- x-release-please-end -->
