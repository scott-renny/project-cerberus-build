# Project Cerberus

[![Status: Planning and acquisition](https://img.shields.io/badge/status-planning%20%26%20acquisition-f0ad4e)](docs/planning/milestones.md)
[![Platform: Fedora KDE](https://img.shields.io/badge/platform-Fedora%20KDE-51A2DA?logo=fedora&logoColor=white)](docs/platform/architecture.md)
[![Hardware: Two components arrived](https://img.shields.io/badge/hardware-2%20components%20arrived-success)](docs/planning/parts-list.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Project Cerberus is the design, construction, deployment, hardening, and ongoing development of a purpose-built Fedora KDE Linux engineering workstation and Cyber Operations Center command platform.

> **Status:** Platform design, hardware acquisition, and deployment planning  
> **Current baseline:** Existing Windows 10 dual-monitor workstation  
> **Successor platform:** Cerberus on Fedora KDE Plasma  
> **Preliminary core budget:** CA$3,000+ before tax, excluding the case; final ceiling TBD
>
> **Program relationship:** Cerberus is the workstation-delivery project for [COC Phase 8.5](https://github.com/scott-renny/cyber-operations-center-engineering-program/tree/main/phases/phase-08-5-workstation-migration).

## More than a system build

Cerberus began as an attempt to buy a workstation with the right performance, display capacity, expansion, cooling, power quality, and upgrade path. Suitable prebuilt systems required too many compromises, so the workstation became a custom build.

The decision to replace Windows with Fedora KDE expanded Cerberus beyond hardware. It now includes:

- Hardware architecture, acquisition, assembly, firmware, and validation
- Fedora KDE installation, security hardening, recovery, and lifecycle management
- A six-display, dual-NVIDIA-GPU command environment
- Desktop and workflow engineering previously planned as Project Hydra
- Linux development, Podman, Distrobox, and optional disposable KVM/QEMU virtual machines
- Git, GitHub, Python, Ansible, OpenTofu/Terraform, AWS, and Kubernetes tooling
- Ansible/IaC control-node duties for the wider environment
- COC access and management for Atlas, Hestia, Ares, Olympus, Kubernetes, Wazuh, Grafana, UniFi, and related systems
- Athena integration groundwork
- OBS and streaming as the final deployment phase

Cerberus is an interactive operator and engineering platform. Permanent services and specialized isolated workloads remain on dedicated systems.

## Locked platform direction

| Area | Decision | State |
|---|---|---|
| Host operating system | **Fedora KDE Plasma** | **Locked** |
| Platform role | Linux engineering workstation and COC control node | **Locked** |
| Desktop scope | Six-display KDE workflow environment | **Consolidated from Hydra** |
| Automation | Ansible/IaC, shell tooling, Git-managed configuration | **Locked direction** |
| Containers | Podman, Podman Desktop, and Distrobox | **Locked direction** |
| Local virtualization | KVM/QEMU and virt-manager when a real temporary use case exists | Optional |
| Streaming | OBS and PS5 capture workflow | Final deployment phase |
| Windows laptop automation | Project Hermes | Separate project |
| Specialized system | Ares V1, repurposed from the retired Windows 10 workstation | Separate project |

## Hardware decision matrix

“Locked” means the design decision is settled; it does not mean purchased. Only items marked owned have been acquired.

| Component | Locked selection or specification | Acquisition state |
|---|---|---|
| Case | MUSETEX K2 | **Owned — arrived** |
| Motherboard | MSI MAG B850 Tomahawk MAX WiFi | **Owned — arrived** |
| CPU | AMD Ryzen 9 9900X | Locked; purchase pending |
| Cooler | MSI MAG CORELIQUID A15 360 | Locked; purchase pending; clearance validation required |
| Memory | 64 GB (2x32 GB) DDR5-6000 EXPO | Specification locked; exact kit selecting |
| Primary storage | 2 TB M.2 NVMe SSD | Specification locked; exact model selecting |
| Primary GPU | NVIDIA GeForce RTX 5060 Ti 16 GB | Specification locked; exact manufacturer/model selecting |
| Secondary GPU | Compact, low-power NVIDIA display GPU | Direction locked; NVIDIA T400 preferred, P620 fallback |
| Power supply | Corsair RM850e (2025), 850 W | Locked; purchase pending |
| UPS | CyberPower CP1500PFCLCD, 1500 VA / 1000 W | Locked; purchase pending |
| USB expansion | Add only if final PCIe layout permits | Optional |

The original MSI Ventus RTX 5060 Ti became unavailable at a sensible price. The locked requirement is therefore the GPU class and 16 GB VRAM, not that exact cooler or manufacturer.

## PCIe and storage strategy

The owned motherboard enables validation against the real board and manual:

- Primary RTX 5060 Ti in the CPU-connected primary slot
- Compact secondary NVIDIA display GPU in the usable lower slot
- M2_3 left unused if required to preserve lower-slot bandwidth
- Primary Fedora SSD placed in a non-conflicting M.2 slot
- USB expansion card added only if both GPUs leave a suitable slot
- Slot-mounted GPU support considered only after the final card dimensions are known

## Project consolidation

Project Hydra is discontinued as a standalone project. Its planned multi-monitor responsibilities now form Cerberus's **Desktop & Workflow Environment** workstream.

Project Hermes remains separate for the Windows 11 laptop. Its Windows/PowerShell implementation is not being ported wholesale into Fedora, although its repeatability, validation, recovery, and documentation principles inform Cerberus.

## System transition

The existing Windows 10 dual-monitor workstation remains operational until Cerberus is assembled, deployed, hardened, tested, and accepted. It will then be retired from primary-workstation duty and repurposed as **Ares V1**.

## Deployment sequence

1. Hardware assembly and first POST
2. BIOS/UEFI and firmware updates
3. Baseline hardware and thermal validation
4. Fedora KDE installation with encryption
5. Updates, firmware, NVIDIA drivers, and six-display validation
6. Security hardening
7. Desktop & Workflow Environment
8. Development and container toolchain
9. COC, Ansible/IaC, Kubernetes, cloud, and infrastructure integration
10. Optional compatibility and disposable-VM layer
11. Athena integration groundwork
12. Full testing, recovery validation, and documentation
13. OBS and streaming configuration **last**
14. Primary-workstation cutover and Ares V1 transition

## Documentation

- [Platform Architecture](docs/platform/architecture.md)
- [Requirements](docs/planning/requirements.md)
- [Parts List](docs/planning/parts-list.md)
- [Budget](docs/planning/budget.md)
- [Milestones](docs/planning/milestones.md)
- [Decision Log](docs/planning/decision-log.md)
- [Compatibility Checklist](docs/planning/compatibility-checklist.md)
- [Build Day](docs/build/build-day.md)
- [Fedora Deployment](docs/configuration/fedora.md)
- [BIOS Configuration](docs/configuration/bios.md)
- [System Hardening](docs/configuration/hardening.md)
- [Desktop & Workflow Environment](docs/platform/desktop-workflows.md)
- [Automation & Control Node](docs/platform/automation-control-node.md)
- [Display Plan](docs/displays/display-plan.md)
- [Dual-GPU Configuration](docs/displays/dual-gpu.md)
- [Validation Test Plan](docs/testing/test-plan.md)
- [Version History](docs/history/version-history.md)

## Security and privacy

This public repository must not contain credentials, recovery keys, serial numbers, order numbers, public IP addresses, private network details, exported secrets, or unsanitized screenshots. See [SECURITY.md](SECURITY.md).

## License

Documentation is provided under the [MIT License](LICENSE).
