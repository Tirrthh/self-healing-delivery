# Self-Healing Delivery Platform

A production-grade delivery platform for a Python service on Azure Kubernetes Service (AKS).

**The problem it solves:** getting code from a developer's laptop to production safely and automatically.

When a developer pushes code:
- Tests run automatically and a Docker image is built
- The app is deployed to AKS with no stored secrets (OIDC)
- If the smoke test fails, it rolls back to the previous version automatically
- If traffic grows, it scales itself (HPA)
- If something goes wrong, an alert fires (Prometheus + Grafana)

## Tech Stack
Python (FastAPI, pytest) · GitHub Actions · Docker · Terraform · AKS · Helm · Azure Key Vault · Prometheus · Grafana

## Status
🚧 In progress. Built step by step, with progress tracked below.

- [ ] Python app + tests
- [ ] CI with GitHub Actions
- [ ] Infrastructure with Terraform
- [ ] Helm deploy + auto-rollback
- [ ] Probes, limits, autoscaling, Key Vault
- [ ] Monitoring + alerts
