# collider-bazel-extensions

Bazel rules for running real infrastructure in tests: hermetic, pinned and
sha256-verified tools, per-test service instances, and Kubernetes cluster
installs that compose with [`rules_kind`](https://github.com/collider-bazel-extensions/rules_kind)
and [`rules_itest`](https://github.com/dzbarsky/rules_itest).

**Missing something?** [Request a rules package](https://github.com/collider-bazel-extensions/.github/issues/new?template=request-a-rules-package.yml).
Bugs and feature requests for an existing package go in that package's repo.

## Clusters and Kubernetes tooling

| Package | What it does |
|---|---|
| [rules_kind](https://github.com/collider-bazel-extensions/rules_kind) | Full Kubernetes clusters in tests with kind (Docker or podman) |
| [rules_kubernetes](https://github.com/collider-bazel-extensions/rules_kubernetes) | Hermetic Kubernetes API server, no Docker or root |
| [rules_kubectl](https://github.com/collider-bazel-extensions/rules_kubectl) | `kubectl apply` as a rules_itest service |
| [rules_helm](https://github.com/collider-bazel-extensions/rules_helm) | Hermetic Helm: `helm_template` and `helm_lint` |

## Cluster installs

| Package | What it does |
|---|---|
| [rules_argocd](https://github.com/collider-bazel-extensions/rules_argocd) | Argo CD install, readiness and Application reconciliation |
| [rules_argo_rollouts](https://github.com/collider-bazel-extensions/rules_argo_rollouts) | Argo Rollouts install |
| [rules_backstage](https://github.com/collider-bazel-extensions/rules_backstage) | Backstage install |
| [rules_capsule](https://github.com/collider-bazel-extensions/rules_capsule) | Project Capsule (multi-tenancy) install |
| [rules_certmanager](https://github.com/collider-bazel-extensions/rules_certmanager) | cert-manager install, no helm required |
| [rules_cilium](https://github.com/collider-bazel-extensions/rules_cilium) | Cilium CNI install and NetworkPolicy testing |
| [rules_cloudnativepg](https://github.com/collider-bazel-extensions/rules_cloudnativepg) | CloudNativePG operator install |
| [rules_crossplane](https://github.com/collider-bazel-extensions/rules_crossplane) | Crossplane (`crank render` and the controller) |
| [rules_external_secrets](https://github.com/collider-bazel-extensions/rules_external_secrets) | External Secrets Operator install |
| [rules_harbor](https://github.com/collider-bazel-extensions/rules_harbor) | Harbor registry install |
| [rules_kafka](https://github.com/collider-bazel-extensions/rules_kafka) | Apache Kafka install |
| [rules_keda](https://github.com/collider-bazel-extensions/rules_keda) | KEDA install |
| [rules_tekton](https://github.com/collider-bazel-extensions/rules_tekton) | Tekton Pipelines install |
| [rules_zitadel](https://github.com/collider-bazel-extensions/rules_zitadel) | Zitadel install with OIDC round-trip smoke |

## Observability

| Package | What it does |
|---|---|
| [rules_prometheus](https://github.com/collider-bazel-extensions/rules_prometheus) | Config checks, promtool rule tests, per-test Prometheus, cluster install |
| [rules_alertmanager](https://github.com/collider-bazel-extensions/rules_alertmanager) | Config validation, routing tests, per-test Alertmanager |
| [rules_otel](https://github.com/collider-bazel-extensions/rules_otel) | OpenTelemetry Collector: config validation, per-test collector with OTLP sink |
| [rules_grafana](https://github.com/collider-bazel-extensions/rules_grafana) | Grafana install |
| [rules_loki](https://github.com/collider-bazel-extensions/rules_loki) | Grafana Loki install |
| [rules_mimir](https://github.com/collider-bazel-extensions/rules_mimir) | Grafana Mimir install |
| [rules_tempo](https://github.com/collider-bazel-extensions/rules_tempo) | Grafana Tempo install |

## Per-test services

| Package | What it does |
|---|---|
| [rules_pg](https://github.com/collider-bazel-extensions/rules_pg) | An isolated PostgreSQL cluster per test |
| [rules_valkey](https://github.com/collider-bazel-extensions/rules_valkey) | Per-test Valkey (standalone or cluster), config checks, cluster install |
| [rules_minio](https://github.com/collider-bazel-extensions/rules_minio) | Per-test MinIO, policy checks, cluster install |
| [rules_nats](https://github.com/collider-bazel-extensions/rules_nats) | Per-test NATS servers, cluster install |
| [rules_vault](https://github.com/collider-bazel-extensions/rules_vault) | Per-test dev-mode Vault, policy checks, HA cluster install |
| [rules_spicedb](https://github.com/collider-bazel-extensions/rules_spicedb) | Parallel-safe per-test SpiceDB |
| [rules_temporal](https://github.com/collider-bazel-extensions/rules_temporal) | Ephemeral Temporal cluster for integration tests |
| [rules_flagd](https://github.com/collider-bazel-extensions/rules_flagd) | flagd (OpenFeature): flag checks, evaluation tests, per-test flagd |

## Policy and security

| Package | What it does |
|---|---|
| [rules_opa](https://github.com/collider-bazel-extensions/rules_opa) | Hermetic OPA: `opa_test` and `opa_fmt_check` |
| [rules_kyverno](https://github.com/collider-bazel-extensions/rules_kyverno) | Kyverno policy checks, test suites, compliance tests, install |
| [rules_gitleaks](https://github.com/collider-bazel-extensions/rules_gitleaks) | gitleaks secret scans as tests, validation actions or an aspect |

## Code generation, schemas and languages

| Package | What it does |
|---|---|
| [rules_atlas](https://github.com/collider-bazel-extensions/rules_atlas) | Atlas declarative DB schema management and the Atlas Operator |
| [rules_oapi_codegen](https://github.com/collider-bazel-extensions/rules_oapi_codegen) | oapi-codegen (OpenAPI to Go), built from source |
| [rules_playwright](https://github.com/collider-bazel-extensions/rules_playwright) | Hermetic Playwright UI tests with Bazel-fetched browsers |
| [rules_ada](https://github.com/collider-bazel-extensions/rules_ada) | Ada with a hermetic FSF GNAT toolchain |

Note: `rules_playwright`, `rules_helm` and `rules_ada` share names with
unrelated modules in the Bazel Central Registry; each README explains how to
install the right one.
