# Secure DevOps Labs

Index repository for my hands-on DevOps / DevSecOps labs. It links two smaller labs as
**git submodules** so they can be cloned together; every other project lives in its own
repository (listed below).

## Included as Submodules

| Path | Repository | What it covers |
| --- | --- | --- |
| [`components/lab-bootstrap`](components/lab-bootstrap) | [linux-hardening-baseline](https://github.com/Aditya-Rafi/linux-hardening-baseline) | Secure Ubuntu/Debian baseline: idempotent user provisioning, SSH key-only access, `ufw` firewall, config backup with SHA256 checksums and retention, post-deploy validation script |
| [`components/Lab-DevopsApp`](components/Lab-DevopsApp) | [fastapi-devops-lab](https://github.com/Aditya-Rafi/fastapi-devops-lab) | FastAPI service behind Nginx with PostgreSQL and Redis: multi-stage non-root image, Docker Compose, unit and integration tests, Ruff, GitHub Actions CI/CD, Trivy scan, Dependabot |

## Related Projects

| Repository | Focus |
| --- | --- |
| [devsecops-cicd-pipeline](https://github.com/Aditya-Rafi/devsecops-cicd-pipeline) | GitHub Actions pipeline with Gitleaks, Semgrep, Trivy and semantic-versioned releases to GHCR |
| [wazuh-threat-mitigation](https://github.com/Aditya-Rafi/wazuh-threat-mitigation) | Wazuh + Suricata detection with custom rules and automated active response |
| [observability-stack](https://github.com/Aditya-Rafi/observability-stack) | Grafana, Alloy, Mimir, Loki, Tempo and Blackbox monitoring with Telegram alerting |
| [ansible-mysql-backup-teleport](https://github.com/Aditya-Rafi/ansible-mysql-backup-teleport) | Ansible MySQL backup/restore over Teleport, run from Semaphore |

## Clone

```bash
git clone --recurse-submodules https://github.com/Aditya-Rafi/Secure-Devops-Labs.git

# already cloned without submodules?
git submodule update --init --recursive
```
