# helm-charts

Homelab Helm charts (wrappers and small app charts).

Published two ways:

- **Classic Helm repo** (GitHub Pages): `https://tobiasgoetz.github.io/helm-charts`
- **OCI** (GHCR): `oci://ghcr.io/tobiasgoetz/helm-charts/<chart>`

## Charts

| Chart | Description |
|-------|-------------|
| [`blocky`](charts/blocky) | Blocky DNS |
| [`home-assistant`](charts/home-assistant) | Home Assistant + Matter + Authentik OIDC |
| [`twitch-drops-miner`](charts/twitch-drops-miner) | Twitch Drops Miner |
| [`uptime-kuma`](charts/uptime-kuma) | Uptime Kuma |

## Install

### Classic repo (`helm repo add`)

```bash
helm repo add tobiasgoetz https://tobiasgoetz.github.io/helm-charts
helm repo update
helm upgrade --install blocky tobiasgoetz/blocky \
  --version <version> \
  -n blocky --create-namespace \
  -f ../homelab/helm/values/blocky.yaml
```

### OCI (GHCR)

```bash
helm install <release> oci://ghcr.io/tobiasgoetz/helm-charts/<chart> --version <version>
```

Example:

```bash
helm upgrade --install blocky oci://ghcr.io/tobiasgoetz/helm-charts/blocky \
  --version <version> \
  -n blocky --create-namespace \
  -f ../homelab/helm/values/blocky.yaml
```

### Local path (dev)

```bash
helm upgrade --install blocky ./charts/blocky -n blocky --create-namespace \
  -f ../homelab/helm/values/blocky.yaml
```
