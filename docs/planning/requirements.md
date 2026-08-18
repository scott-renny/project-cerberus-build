# Requirements

## Platform scope

Cerberus is a Linux Mint Cinnamon-based Linux engineering workstation and Cyber Operations Center command platform. It includes the physical build, operating-system deployment, desktop engineering, hardening, automation, infrastructure integration, testing, recovery, and lifecycle documentation.

Cerberus is not a permanent application server, Kubernetes node, or primary adversary-simulation host.

## Functional requirements

- Run Linux Mint Cinnamon as the host operating system.
- Provide a secure, encrypted, recoverable primary workstation.
- Drive six displays through two NVIDIA GPUs without an MST hub.
- Support cybersecurity operations, software development, technical research, AI experimentation, and content creation.
- Provide NVIDIA CUDA and NVENC capability for AI, GPU acceleration, and OBS.
- Support Bash, Git, Python, Docker, Distrobox, Ansible, Kubernetes, AWS, and IaC tooling.
- Operate as the Ansible/IaC control node for authorized infrastructure.
- Provide COC access to Atlas, Hestia, Ares, Olympus, Kubernetes, Wazuh, Grafana, UniFi, and related services.
- Support optional disposable KVM/QEMU virtual machines when a defined local use case exists.
- Support the PS5 capture and streaming workflow, configured only after the core platform is stable.
- Allow later NVMe and memory expansion.

## System boundaries

- Project Hydra is discontinued; its desktop and multi-monitor scope is consolidated into Cerberus.
- Project Hermes remains separate for the Windows 11 laptop.
- Ares V1 will reuse the retired Windows 10 workstation hardware for specialized or isolated workloads.
- Permanent infrastructure remains on its dedicated systems.
- Cerberus is a management client for Kubernetes, not an additional cluster node.
- WireGuard is not part of the default stationary-workstation configuration; network access is controlled through Olympus/UniFi placement and policy.

## Locked hardware direction

- MUSETEX K2 case — owned and arrived.
- MSI MAG B850 Tomahawk MAX WiFi — owned and arrived.
- AMD Ryzen 9 9900X.
- MSI MAG CORELIQUID A15 360, pending physical clearance validation.
- 64 GB (2x32 GB) DDR5-6000 EXPO; exact kit selecting.
- 2 TB M.2 NVMe primary SSD; exact model selecting.
- NVIDIA RTX 5060 Ti 16 GB; exact model selecting.
- Compact NVIDIA secondary display GPU; T400 preferred, P620 fallback.
- Corsair RM850e (2025), 850 W.
- CyberPower CP1500PFCLCD, 1500 VA / 1000 W.
- Optional USB expansion only if final PCIe allocation permits.

## Security requirements

- UEFI boot, Secure Boot where supported by the final NVIDIA/Linux Mint deployment, TPM visibility, and current firmware.
- Full-disk encryption with recovery material stored securely offline.
- AppArmor enabled and enforcing.
- Host firewall enabled with least-required exposure.
- Standard user for routine work; elevation only when required.
- Hardware security-key integration where supported.
- Version-controlled configuration without committed secrets.
- Tested backups, restoration, and documented recovery media.
- Specialized or untrusted workloads isolated on Ares or disposable local VMs as appropriate.

## Success criteria

- Linux Mint Cinnamon boots reliably and all hardware is detected.
- Six displays survive reboot, logout/login, sleep/wake where supported, and driver updates.
- NVIDIA acceleration, CUDA, and NVENC operate correctly.
- Memory, storage, CPU, GPUs, thermals, and combined load pass validation.
- Docker, Distrobox, Git, Python, Ansible, Kubernetes, and cloud tooling pass representative tests.
- Authorized COC systems are manageable without hosting their production services locally.
- Security controls and recovery procedures are validated.
- Streaming works after the engineering platform is stable.
- No sensitive information is published.
