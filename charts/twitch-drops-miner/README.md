# Twitch Drops Miner

[Twitch Drops Miner](https://github.com/DevilXD/TwitchDropsMiner) (Docker image: [dungfu/twitch-drops-miner](https://github.com/fireph/docker-twitch-drops-miner)) on Kubernetes.

See [values.yaml](values.yaml) for all options.

## Install from GHCR

<!-- x-release-please-start-version -->
```bash
helm install twitch-drops-miner oci://ghcr.io/tobiasgoetz/helm-charts/twitch-drops-miner --version 1.2.10 \
  -n twitch-drops-miner --create-namespace \
  -f values.yaml
```
<!-- x-release-please-end -->
