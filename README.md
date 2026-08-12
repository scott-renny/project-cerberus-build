# Project Cerberus Build

[![Project status: Planning](https://img.shields.io/badge/status-planning-f0ad4e)](docs/planning/requirements.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Documentation](https://img.shields.io/badge/documentation-in%20progress-6f42c1)](docs/planning/parts-list.md)

Designing, building, and documenting Cerberus: a physical dual-GPU cybersecurity workstation for operations, development, AI experimentation, content creation, and a six-monitor command center.

> **Status:** Planning and component acquisition  
> **Documentation version:** 0.2.0  
> **Current operational baseline:** Version 1 — existing Windows 10 dual-monitor workstation  
> **Future build:** Cerberus rebuild  
> **Preliminary core budget:** CA$3,000+, excluding the case; final ceiling TBD

## Version scope

Version 1 is the existing Windows 10 dual-monitor workstation and remains the operational baseline. It is not the Cerberus rebuild.

The future Cerberus rebuild is a separate physical workstation build now in planning and component acquisition. Its target is Windows 11 Pro, two GPUs, and six directly connected displays. See [Version History](docs/history/version-history.md).

## Why build it

Cerberus became a custom build because it was too difficult to buy a complete off-the-shelf system that provided everything required in one machine. The project needs a specific balance of strong concurrent-workload performance, 64 GB of fast memory, NVIDIA encoding and compute, direct support for six monitors through two GPUs, usable PCIe expansion, strong cooling, reliable power, and a clear upgrade path.

Prebuilt systems generally forced compromises in one or more of those areas and offered less control over exact motherboard layout, GPU clearance, power-supply quality, cooling, and future expansion. Building Cerberus component by component makes those constraints explicit and allows every part to be selected and validated against the real workload.

## Confirmed hardware status

| Component | Selection | Status |
|---|---|---|
| Case | MUSETEX K2 | **Owned — arrived** |
| Motherboard | MSI MAG B850 Tomahawk MAX WiFi | **Owned — arrived** |
| CPU | AMD Ryzen 9 9900X | Planned / locked direction |
| Cooler | MSI MAG CORELIQUID A15 360 | Current choice |
| Memory | 64 GB (2x32 GB) DDR5-6000 EXPO | Selecting |
| Storage | 2 TB PCIe 4.0 NVMe SSD | Planned |
| Primary GPU | NVIDIA GeForce RTX 5060 Ti 16 GB | Required; exact replacement model selecting |
| Secondary GPU | Low-power display GPU | Selecting |
| Power supply | Corsair RM850e (2025) | Current choice |
| UPS | CyberPower CP1500PFCLCD, 1500 VA / 1000 W | Current choice |

The original MSI Ventus RTX 5060 Ti model became unavailable, so it must not be treated as the selected card. The replacement must still provide 16 GB VRAM and fit the final dual-GPU layout.

Because the exact motherboard is now owned, its physical slot spacing and documented lane allocation can be used to validate coexistence of the primary GPU, secondary display GPU, and any USB expansion card before those cards are purchased.

## Relationship to Project Ares

Cerberus is the primary workstation and command center. Project Ares is a separate physical system intended for specialized, isolated, or infrastructure workloads. Cerberus may retain optional local virtualization capability for occasional testing, but it is not being designed as the primary VM host.

Specific models and current pricing are tracked in [Parts List](docs/planning/parts-list.md) and [Budget](docs/planning/budget.md). A current choice is not purchased unless explicitly marked owned.

## Purpose

Project Cerberus is designed to support:

- Cybersecurity labs and blue-team workflows
- Software development, WSL, containers, and technical research
- AI experimentation and GPU-accelerated workloads
- OBS capture and NVIDIA hardware encoding
- Six directly connected displays across two GPUs
- Straightforward storage and memory expansion

## Design priorities

1. Preserve the Ryzen 9 9900X and 64 GB memory direction while refining the preliminary CA$3,000+ core budget.
2. Keep a secondary, low-power display GPU in the initial Cerberus build.
3. Validate motherboard slot allocation and physical clearance before selecting expansion cards.
4. Start with one 2 TB SSD and expand only when capacity requires it.
5. Prefer wired 2.5 Gb Ethernet.
6. Maintain safe airflow and slot clearance for both GPUs.
7. Document decisions, testing, changes, and lessons learned.

## Documentation

- [Requirements](docs/planning/requirements.md)
- [Parts List](docs/planning/parts-list.md)
- [Milestones](docs/planning/milestones.md)
- [Compatibility Checklist](docs/planning/compatibility-checklist.md)
- [Decision Log](docs/planning/decision-log.md)
- [Version History](docs/history/version-history.md)
- [Build Day](docs/build/build-day.md)
- [Display Plan](docs/displays/display-plan.md)
- [Dual-GPU Setup](docs/displays/dual-gpu.md)
- [Test Plan](docs/testing/test-plan.md)
- [Upgrade Roadmap](docs/operations/upgrades.md)

## Project phases

- **Version 1 baseline:** existing Windows 10 dual-monitor system.
- **Planning and acquisition:** select Cerberus parts, confirm compatibility, and record purchases.
- **Assembly:** build the physical workstation and document installation details.
- **Configuration:** update firmware, install Windows 11 and drivers, and configure both GPUs.
- **Validation:** test memory, storage, thermals, stability, displays, GPU acceleration, and streaming.
- **Operations:** record maintenance, firmware changes, and upgrades.

## Security and privacy

This public repository must not contain credentials, product keys, serial numbers, public IP addresses, private network details, exported configuration secrets, or unsanitized screenshots. See [SECURITY.md](SECURITY.md).

## License

Documentation is provided under the [MIT License](LICENSE).
