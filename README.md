# Aleksandr Letunov

**Platform Engineering Lead · IaC, DevSecOps & AI for infrastructure.** I build the platform other
engineers ship on, make it secure by default, and make it work with AI agents.

- **Platform.** Largest contributor to an organisation-wide IaC platform behind ~680 repositories:
  21 GitLab CI/CD components I created, 18 containerised CI execution environments, ~25
  config-driven Terraform modules, ~80 Ansible roles (~47 with Molecule tests), golden images, and
  ~20,000 lines of Go tooling. A shared CI base image cut builds from ~15–20 min to ~7–10 min.
- **Security by default.** Rolling out least-privilege CI identity in HashiCorp Vault: short-lived
  per-role tokens and read-only twins for merge-request runs, proven by a deny-matrix harness.
  Images, Helm charts and GitOps artifacts are signed with cosign through Vault transit, with SBOMs.
- **AI-operable infrastructure.** I built my team's Claude Code plugin marketplace (11 plugins,
  58 eval suites gating every release) and drove a shared knowledge corpus that lets agents work
  to our conventions. Terraform modules now take days instead of weeks.

## Public work

| Repository | What |
|---|---|
| [docker](https://github.com/flyoverhead/docker) | Ansible collection for Docker services |
| [server](https://github.com/flyoverhead/server) | Ansible collection for server baseline: SSH, firewall, systemd, fail2ban |
| [k3s](https://github.com/flyoverhead/k3s) | Ansible collection for k3s clusters |
| [macos](https://github.com/flyoverhead/macos) | Workstation as code, including Claude Code configuration |
| [terraform-proxmox-compute](https://github.com/flyoverhead/terraform-proxmox-compute) | Config-driven Terraform module for Proxmox VE |
| [video-summary](https://github.com/flyoverhead/video-summary) | Claude Code plugin with agents that turns camera footage into a summary video |

Stack: Terraform / OpenTofu · Ansible · Kubernetes · Helm · Flux · GitLab CI · HashiCorp Vault ·
cosign · Go · Python · OpenStack · VMware · AWS · Prometheus / Grafana · Claude Code · MCP

[flyoverhead.github.io](https://flyoverhead.github.io) ·
[LinkedIn](https://www.linkedin.com/in/aleksandr-letunov-89427314b/)
