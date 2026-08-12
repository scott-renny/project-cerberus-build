# Requirements

## Scope

- Preserve Version 1 as the existing Windows 10 dual-monitor operational baseline.
- Treat Cerberus as a separate, future physical workstation rebuild.
- Do not describe planned or merely selected Cerberus hardware as installed.

## Functional requirements for the Cerberus rebuild

- Run Windows 11 Pro as the primary operating system.
- Support multiple concurrent Windows and Linux virtual machines.
- Support WSL, Docker, development tools, and cybersecurity applications.
- Drive six monitors through direct GPU connections without an MST hub.
- Provide NVIDIA hardware encoding for OBS and streaming.
- Connect to the local network through wired Ethernet.
- Allow later expansion to additional NVMe storage and 128 GB memory.

## Constraints and confirmed direction

- Use the owned, arrived MUSETEX K2 case.
- Use the owned, arrived MSI MAG B850 Tomahawk MAX WiFi motherboard.
- Use a preliminary core budget of CA$3,000 or more before tax, excluding the case; set the final ceiling after exact parts and contingency are priced.
- Retain the AMD Ryzen 9 9900X direction.
- Use 64 GB (2x32 GB) DDR5-6000 EXPO memory; exact kit selecting.
- Require an RTX 5060 Ti with 16 GB VRAM; exact replacement model selecting.
- Include a small, low-power secondary display GPU; exact model selecting.
- Validate both GPUs and any USB expansion card against the exact motherboard slot layout.
- Begin with one 2 TB NVMe SSD.
- Treat the MSI MAG CORELIQUID A15 360, Corsair RM850e (2025), and CyberPower CP1500PFCLCD as current choices until purchased.

## Success criteria

- All six displays operate concurrently at their intended resolutions and refresh rates.
- The system completes stability, memory, storage, and thermal tests without errors.
- Virtualization and NVIDIA hardware encoding function correctly.
- Temperatures and noise remain acceptable under sustained combined load.
- PCIe devices coexist without obstructed slots or unacceptable resource sharing.
- No sensitive system or network information is published in this repository.
