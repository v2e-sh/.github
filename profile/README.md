<div align="center">

# v2e

**A self-hosted DevOps lab you can reach from anywhere —<br>a sandbox where AI agents run it.**

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=flat&logo=proxmox&logoColor=white)
![OpenTofu](https://img.shields.io/badge/OpenTofu-FFDA18?style=flat&logo=opentofu&logoColor=black)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat&logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

</div>

An isolated [Proxmox](https://www.proxmox.com/) environment defined as code: a
VyOS router fronting a small mesh of Linux nodes. Reach it securely from any
station, use it as a gateway to your homelab, and hand the DevOps flow to AI
coding agents (Claude Code, Codex, …) on a dedicated node. **The VyOS router is
the boundary** — keep the agents sandboxed, or let them loose.

## Repositories

| Repo | What it is |
|------|------------|
| **[v2e-tf](https://github.com/v2e-sh/v2e-tf)** | Infrastructure as code that provisions the environment from the ground up. |
| **[v2e-ansible](https://github.com/v2e-sh/v2e-ansible)** | Configuration & automation: initialization playbooks and ongoing setup. |
| **[v2e-compose](https://github.com/v2e-sh/v2e-compose)** | Containerized application stacks for the services running inside the lab. |
| **[v2e-docs](https://github.com/v2e-sh/v2e-docs)** | Guides, runbooks, and reference. **Start here.** |

## The machines

| Machine | Role |
|---------|------|
| `vyos` | VyOS router — routes, NATs, and gates what the agents reach |
| `control` | SSH-mesh hub + Ansible automation |
| `services` | Docker host |
| `agent` | AI agents, behind the router |

> [!WARNING]
> **Early & evolving** — actively under construction, with plenty still on the roadmap.
