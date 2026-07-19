# Grafana Observability Stack (Docker Compose)

A Docker Compose setup for a self-hosted Grafana observability stack, providing metrics, logs, traces, and profiling in a single deployment.

## Contents

This stack includes the following containers:

- **Grafana** – visualization and dashboarding UI
- **Loki** (read, write, ruler, backend, gateway) – log aggregation, deployed in [simple scalable mode](https://grafana.com/docs/loki/latest/get-started/deployment-modes/) with an Nginx gateway for request routing
- **Alloy** – telemetry collector for shipping logs, metrics, and traces
- **Tempo** – distributed tracing backend
- **Mimir** – long-term metrics storage, Prometheus-compatible
- **Pyroscope** – continuous profiling backend

## Project Structure

This repository contains only the deployment configuration:

- `docker-compose.yml` – the stack definition
- `.gitlab-ci.yml` – GitLab CI pipeline for deployment
- `renovate.json` – Renovate bot configuration for automated dependency/image updates
- `.gitignore`

## Deployment

The stack is intended to be deployed via **GitLab CI**. Image updates (Grafana, Loki, Alloy, Tempo, Mimir, Pyroscope, Nginx) are kept current automatically using **[Renovate](https://docs.renovatebot.com/)**, which opens merge requests whenever new versions or digests are available.

## Documentation

For configuration details, environment variables, and administration guides, refer to the official Grafana documentation:

- [Grafana](https://grafana.com/docs/grafana/latest/)
- [Loki](https://grafana.com/docs/loki/latest/)
- [Alloy](https://grafana.com/docs/alloy/latest/)
- [Tempo](https://grafana.com/docs/tempo/latest/)
- [Mimir](https://grafana.com/docs/mimir/latest/)
- [Pyroscope](https://grafana.com/docs/pyroscope/latest/)

## License

See the [LICENSE](./LICENSE) file for details.