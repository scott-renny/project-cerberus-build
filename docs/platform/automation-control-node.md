# Automation and Control Node

## Role

Cerberus will be the authorized interactive control node for infrastructure automation. It will not host the permanent services it manages.

## Core tooling

- Git and GitHub CLI
- Bash and tmux
- Python with uv and project-local environments
- Ansible
- OpenTofu or Terraform when required
- AWS CLI
- kubectl, Helm, and k9s
- SSH client configuration and key-based authentication
- Podman and Distrobox

## Managed environment

Subject to project-specific access policy, Cerberus may administer Atlas, Hestia, Ares, Olympus/UniFi, Kubernetes, Wazuh, Grafana, and other documented COC systems.

## Principles

- Infrastructure changes increasingly flow through Git and reviewed configuration.
- Use Ansible check mode and scoped inventories where practical.
- Keep inventories sanitized in public repositories; private values remain outside Git.
- Do not reuse production secrets in labs.
- Document manual recovery from automation errors.
- Do not turn Cerberus into Kubernetes Node 5 or a permanent application server.
- Prefer learning and understanding the CLI before relying on graphical abstractions.
