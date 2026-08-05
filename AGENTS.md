# Agent notes

## Chart versioning

Do **not** manually bump `version` in `charts/*/Chart.yaml`.

Release Please (`release-type: helm` in `release-please-config.json`) owns chart versions, changelogs, and README version badges. It bumps `Chart.yaml` `version` on release from conventional commits.

## Image versions

Pin the app image with `image.tag` in `charts/*/values.yaml`. That is the source of truth; Renovate’s `helm-values` manager updates it.

Do not set `appVersion` in `Chart.yaml` — it would duplicate the pin and drift from Renovate updates.
