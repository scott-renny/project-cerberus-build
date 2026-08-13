# Cerberus Platform Architecture

## Mission

Cerberus is a Fedora KDE Linux engineering workstation and Cyber Operations Center command platform. It is the trusted interactive point from which infrastructure is built, administered, observed, documented, and improved.

## Workstreams

### Hardware platform

Custom dual-GPU, six-display workstation; firmware; cooling; power; storage; expansion; UPS; and validation.

### Fedora foundation

Encrypted Fedora KDE deployment, updates, firmware, NVIDIA drivers, recovery, and lifecycle management.

### Desktop & Workflow Environment

The scope formerly planned as Project Hydra: KDE activities, virtual desktops, window rules, launchers, hotkeys, monitor roles, workspace restoration, and command-center workflows.

### Security

SELinux, firewall, encryption, Secure Boot strategy, hardware-key integration, least privilege, backup, recovery, and secrets boundaries.

### Engineering toolchain

Git, GitHub CLI, Bash, Python with isolated environments, VS Code/VSCodium, Podman, Podman Desktop, Distrobox, and documentation tooling.

### Automation & control node

Ansible, IaC, SSH configuration, Kubernetes clients, AWS tooling, and authorized management of the broader COC environment.

### Optional compatibility

KVM/QEMU, virt-manager, or alternate Distrobox userspaces only for defined temporary needs. This is not a permanent-hosting role.

### Creative and streaming

Native Linux creative tools and OBS. Streaming is deliberately the final deployment phase.

## External boundaries

- Hermes: separate Windows 11 laptop automation.
- Ares V1: repurposed retired workstation for specialized or isolated work.
- Atlas, Hestia, Olympus, Kubernetes, Wazuh, Grafana, UniFi, and related systems: remotely administered; their permanent services are not duplicated on Cerberus.
- Athena: future integration and development interfaces, not absorbed into Cerberus.

## Configuration principle

Prefer documented, repeatable, version-controlled configuration. Keep secrets and machine-specific sensitive data outside the public repository. Use automation only where it improves reliability and understanding; preserve clear manual recovery paths.
