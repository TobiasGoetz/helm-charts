# Uptime Kuma

[Uptime Kuma](https://github.com/louislam/uptime-kuma) on Kubernetes.

Uptime Kuma has no native OIDC. This chart uses Traefik forward-auth via Authentik. Follow the [Authentik Uptime Kuma guide](https://integrations.goauthentik.io/monitoring/uptime-kuma/) for the Proxy Provider, outpost, unauthenticated paths, and disabling built-in auth (plus Trust Proxy).

See [values.yaml](values.yaml) for all options.

## Install from GHCR

<!-- x-release-please-start-version -->
```bash
helm install uptime-kuma oci://ghcr.io/tobiasgoetz/helm-charts/uptime-kuma --version 1.1.1 \
  -n uptime-kuma --create-namespace \
  -f values.yaml
```
<!-- x-release-please-end -->
