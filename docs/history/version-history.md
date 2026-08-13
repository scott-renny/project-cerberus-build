# Version and Lifecycle History

## Existing workstation — current operational baseline

The current system remains in service until Cerberus is fully accepted:

- Windows 10
- Dual-monitor operation
- Existing hardware
- Current primary workstation role

It is not Cerberus and must not be described as containing planned Cerberus hardware or Fedora configuration.

## Ares V1 — future repurposing

After Cerberus takes over, the current Windows 10 workstation will be retired from primary duty and its hardware will be repurposed as Ares V1. Ares will document its own operating system, upgrades, specialized role, and validation. Windows 10 is not assumed to remain installed.

## Cerberus 0.x — platform design and acquisition

Current Cerberus work includes:

- custom hardware architecture and purchasing;
- Fedora KDE platform design;
- consolidation of Hydra's desktop/workflow scope;
- Fedora-native automation and control-node planning;
- six-display dual-GPU engineering;
- hardening, recovery, COC, Kubernetes, cloud, and development planning.

### Acquired foundation

- MUSETEX K2 — owned and arrived
- MSI MAG B850 Tomahawk MAX WiFi — owned and arrived

### Locked but not fully acquired

- AMD Ryzen 9 9900X
- MSI MAG CORELIQUID A15 360, pending clearance validation
- 64 GB (2x32 GB) DDR5-6000 EXPO; exact kit open
- 2 TB NVMe primary storage; exact model open
- RTX 5060 Ti 16 GB; exact model open
- Compact NVIDIA secondary GPU; T400 preferred, P620 fallback
- Corsair RM850e (2025)
- CyberPower CP1500PFCLCD

## Cerberus 1.0 — acceptance target

Cerberus reaches its first operational release only when:

- hardware assembly and firmware configuration are complete;
- Fedora KDE is installed, updated, and recoverable;
- encryption, SELinux, firewall, and security controls are validated;
- two NVIDIA GPUs reliably drive all six displays;
- the Desktop & Workflow Environment is documented;
- development, container, Ansible/IaC, Kubernetes, cloud, and COC tooling are validated;
- backups and recovery procedures pass testing;
- OBS and the streaming workflow are configured last;
- Cerberus is promoted to primary-workstation duty.

## Project consolidation history

- **Project Hydra:** discontinued before implementation; scope absorbed into Cerberus.
- **Project Hermes:** remains separate for the Windows 11 laptop.
- **Project Ares:** separate project; Ares V1 will reuse the retired workstation hardware.
