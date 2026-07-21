# Project Cerberus Build

[![Project status: Planning](https://img.shields.io/badge/status-planning-f0ad4e)](docs/planning/requirements.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Documentation](https://img.shields.io/badge/documentation-in%20progress-6f42c1)](docs/planning/parts-list.md)

Designing, building, and documenting a dual-GPU cybersecurity workstation for virtualization, streaming, development, and a six-monitor command center.

> **Status:** Planning  
> **Version:** 0.1.0  
> **Budget target:** CA$2,000–2,200, excluding the case

## Purpose

Project Cerberus is a purpose-built workstation designed to support:

- Cybersecurity labs and blue-team workflows
- Multiple concurrent virtual machines
- Docker, WSL, and development workloads
- OBS capture and hardware encoding
- Six directly connected displays across two GPUs
- Straightforward storage and memory expansion

## Planned hardware

| Component | Selection | Status |
|---|---|---|
| Case | MUSETEX K2 | Purchased |
| CPU | AMD Ryzen 9 9900X | Planned |
| Cooler | Thermalright Phantom Spirit 120 SE | Planned |
| Motherboard | B850 ATX board with two full-length PCIe slots | Under review |
| Memory | 64 GB (2x32 GB) DDR5-6000 CL30 | Planned |
| Storage | 2 TB PCIe 4.0 NVMe SSD | Planned |
| Primary GPU | NVIDIA GeForce RTX 5060 Ti 16 GB | Planned |
| Display GPU | Intel Arc A310 | Planned |
| Power supply | 850–1000 W, 80 Plus Gold, ATX 3.x | Under review |

Specific models and current pricing are tracked in [Parts List](docs/planning/parts-list.md) and [Budget](docs/planning/budget.md). No component is considered final until physical clearance, PCIe layout, display outputs, and power requirements are verified.

## Design priorities

1. Preserve the Ryzen 9 9900X and 64 GB memory within the target budget.
2. Keep the second GPU in the initial build for direct monitor connections.
3. Start with one 2 TB SSD and expand only when capacity requires it.
4. Prefer wired 2.5 Gb Ethernet; onboard Wi-Fi is optional.
5. Maintain safe airflow and slot clearance for both GPUs.
6. Document decisions, testing, changes, and lessons learned.

## Display plan

The intended topology is four displays on the NVIDIA GPU and two auxiliary displays on the Intel GPU. The final assignment depends on the exact ports, resolutions, refresh rates, and inputs of all six monitors. See [Display Plan](docs/displays/display-plan.md).

## Documentation

- [Requirements](docs/planning/requirements.md)
- [Parts List](docs/planning/parts-list.md)
- [Budget](docs/planning/budget.md)
- [Compatibility Checklist](docs/planning/compatibility-checklist.md)
- [Decision Log](docs/planning/decision-log.md)
- [Build Day](docs/build/build-day.md)
- [BIOS Configuration](docs/configuration/bios.md)
- [Windows Installation](docs/configuration/windows.md)
- [System Hardening](docs/configuration/hardening.md)
- [Display Plan](docs/displays/display-plan.md)
- [Dual-GPU Setup](docs/displays/dual-gpu.md)
- [Test Plan](docs/testing/test-plan.md)
- [Benchmarks and Thermals](docs/testing/benchmarks.md)
- [Maintenance](docs/operations/maintenance.md)
- [Upgrade Roadmap](docs/operations/upgrades.md)

## Project phases

- **Planning:** select parts, confirm compatibility, and record costs.
- **Assembly:** build the system and document installation details.
- **Configuration:** update firmware, install Windows and drivers, and configure both GPUs.
- **Validation:** test memory, storage, thermals, stability, displays, virtualization, and streaming.
- **Operations:** record maintenance, firmware changes, and upgrades.

## Security and privacy

This public repository must not contain credentials, product keys, serial numbers, public IP addresses, private network details, exported configuration secrets, or unsanitized screenshots. See [SECURITY.md](SECURITY.md).

## License

Documentation is provided under the [MIT License](LICENSE).
