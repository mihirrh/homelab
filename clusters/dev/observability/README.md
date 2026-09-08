# Observability

Planned stack:

| Component  | Purpose                        |
|------------|-------------------------------|
| Prometheus | Metrics collection & alerting  |
| Grafana    | Dashboards                     |
| Loki       | Log aggregation                |

Each will get its own subdirectory with a `flux-kustomization.yaml` that
`dependsOn: infra-gateway-api` so it can publish dashboards via the Gateway.

Add a `flux-kustomization.yaml` here and reference it from
`clusters/dev/kustomization.yaml` when ready.
