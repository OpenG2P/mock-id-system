# mock-id-system

Helm chart for the **MOSIP Mock Identity System**, packaged for OpenG2P deployments.

This repo builds **no images**. The chart deploys upstream third-party images
(`mosipid/mock-identity-system`, `mosipid/postgres-init`, `bitnami/bitnami-shell`)
at the versions MOSIP publishes, consumed as-is — so their tags in `values.yaml` are
left exactly as upstream set them.

## What CI does

`.github/workflows/build-publish.yml` calls the central pipeline in
[`openg2p-packaging@v1`](https://github.com/OpenG2P/openg2p-packaging). On every
push it derives one version for the commit, packages the chart at that version,
publishes it to [`openg2p-helm`](https://openg2p.github.io/openg2p-helm), and writes
a page to the [versions catalogue](https://openg2p.github.io/versions/).

| | |
| --- | --- |
| **Chart** | `mock-identity-system` |
| **Chart source** | `helm/mock-identity-system` |
| **Published to** | [`openg2p-helm`](https://openg2p.github.io/openg2p-helm) |
| **Versioning** | [Helm & Docker Versioning Strategy and CI](https://docs.openg2p.org/operations/deployment/helm-docker-versioning-and-ci) |
