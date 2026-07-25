# Cloudflare ACME Issuer

cert-manager `ClusterIssuer` for Let's Encrypt DNS-01 via Cloudflare.

Creates the Cloudflare API token Secret and a ClusterIssuer. Requires [cert-manager](https://cert-manager.io/) already installed. See [values.yaml](values.yaml) for all options.

## Install from GHCR

<!-- x-release-please-start-version -->
```bash
helm install cloudflare-acme-issuer oci://ghcr.io/tobiasgoetz/helm-charts/cloudflare-acme-issuer --version 1.2.9 \
  --set issuerSecret.apiToken="CHANGEME" \
  --set issuer.acme.email="admin@example.com" \
  --set issuer.acme.solver.email="admin@example.com"
```
<!-- x-release-please-end -->
