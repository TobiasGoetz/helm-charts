# helm-charts

Homelab Helm charts (wrappers and small app charts).

Published to GHCR as OCI artifacts: `oci://ghcr.io/tobiasgoetz/helm-charts/<chart>`.

## Charts

| Chart | Description |
|-------|-------------|
| [`blocky`](charts/blocky) | Blocky DNS |
| [`cloudflare-acme-issuer`](charts/cloudflare-acme-issuer) | cert-manager ClusterIssuer (Cloudflare DNS-01) |
| [`home-assistant`](charts/home-assistant) | Home Assistant + Matter + Authentik OIDC |
| [`twitch-drops-miner`](charts/twitch-drops-miner) | Twitch Drops Miner |

## Install

```bash
helm install <release> oci://ghcr.io/tobiasgoetz/helm-charts/<chart> --version <version>
```

Example with values from a sibling `homelab` checkout:

```bash
helm upgrade --install blocky oci://ghcr.io/tobiasgoetz/helm-charts/blocky \
  --version <version> \
  -n blocky --create-namespace \
  -f ../homelab/helm/values/blocky.yaml
```

Local path install (dev):

```bash
helm upgrade --install blocky ./charts/blocky -n blocky --create-namespace \
  -f ../homelab/helm/values/blocky.yaml
```

## Release

Releases use **Release Please** (conventional commits on `main`). Merging a release PR bumps each chart’s `Chart.yaml` and chart README version, creates a GitHub Release, and pushes the chart to GHCR via `.github/workflows/helm-publish.yml`.
