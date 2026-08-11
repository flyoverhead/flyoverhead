# Aleksandr Letunov

**Platform / Infrastructure Engineer** — I build the platform other engineers ship on.

Currently the largest contributor across a 600-repository infrastructure estate, where I own
the internal developer platform end to end: reusable CI components, Ansible roles, Terraform
modules, and the Go services that tie them together.

## What I work on

### Internal developer platform

~20 reusable GitLab CI components, 100+ Ansible roles, Terraform modules, and containerised
CI execution environments. Standardising the build layer cut pipeline times from 15–20
minutes to 7–10.

### Go services for infrastructure

- **Artifactory / Nexus uploaders** — mirror external packages into internal artifact
  repositories. Worker-pool parallelism, SHA256 verification on download and upload, checksum
  dedup and drift detection, template expansion across versions × OS × arch, orphan cleanup,
  backoff retry, multi-platform images. Python → Go rewrite took a pipeline stage from 2–3 min
  to 30 s.
- **gitlab-deps** — CLI and web service detecting dependency drift estate-wide: resolve the
  latest tag per dependency repo, parse each project's `requirements.yml`, `.gitlab-ci.yml`
  and `*.tf`, diff used against available. Covers Ansible roles and collections, CI components
  and Terraform modules — each declared in a different format, sometimes across several
  registries. Cut ~1 hr/week per engineer of version-chasing to 5–10 min.
- **cihelper** — CI utility belt: git file and YAML-key diffing, Ansible tag filtering for
  targeted deploys, Terraform provider fetching, Vault secrets, artifact handling, MR
  discussions, cloud-platform detection.
- Also a load-balancer fleet-management API (day-long review workflow → one authenticated API
  call), a registry cleaner, a token rotator, and an L2 EVPN agent.

### AI-assisted infrastructure engineering

Internal Claude Code tooling — two plugin marketplaces and a workflow framework.

- **IaC toolkit** — 12 composable plugins, 18 skills, ~20 slash commands: Ansible roles,
  Terraform modules and providers, Go, API design (OpenAPI 3.1 / OWASP), GitLab CLI, project
  scaffolding, pre-commit, upgrade-safety analysis via MCP, container CVE auditing,
  environment bootstrap. A shared context layer loads first, a shared validation gate runs
  last.
- **Agent marketplace** — 131 specialised subagents across 11 domains.
- **Infra Powers** — agentic framework for infrastructure change, ported from
  [obra/superpowers](https://github.com/obra/superpowers). Inventory and declared config are
  the sources of truth; live systems are evidence, never a place to author change. 14 skills,
  tiered: recon computes three-way drift and classifies Standard / Normal / Emergency; Normal
  adds a design gate and adversarial fresh-context review; execution re-checks the diff per
  step; nothing closes until inventory, git and live agree. Enforced by hooks, with runbooks
  and tests.

Together: Terraform module delivery weeks → days, Ansible roles a week → a day.

## Stack

`Go` `TypeScript` `Python` `Bash` `PowerShell`

`Kubernetes` `Talos` `Helm` `Flux` `Docker` `Terraform / OpenTofu` `Ansible` `Packer`

`OpenStack` `Ceph` `Vault` `Harbor` `Keycloak` `PostgreSQL / Patroni` `HAProxy`

`Prometheus` `Grafana` `OpenSearch` `NetBox` `BGP / FRR` `OVN` `PowerDNS` `GitLab CI`

## Selected repositories

- **[ansible-openwrt](https://github.com/flyoverhead/ansible-openwrt)** — Ansible collection
  for configuring OpenWrt devices with no Python on the target.
- **[kubernetes-homelab](https://github.com/flyoverhead/kubernetes-homelab)** — multi-master
  Kubernetes built with kubeadm, Ansible, Helm and Terraform.
- **[docker](https://github.com/flyoverhead/docker)** — Ansible collection for deploying and
  configuring containerised services.
- **[homelab](https://github.com/flyoverhead/homelab)** — infrastructure-as-code Kubernetes
  deployment for microservices and network research.

Before infrastructure I spent a decade in analytics and management, including five years in
AML/CFT compliance and running two businesses of my own — which is why I think about platform
work in terms of the time it gives other people back.
