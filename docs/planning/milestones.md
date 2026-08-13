# Milestones

## 1. Architecture and consolidation

- [x] Define Cerberus as more than a hardware build.
- [x] Lock Fedora KDE Plasma as the host operating system.
- [x] Define Cerberus as the Linux engineering workstation and COC control node.
- [x] Consolidate Project Hydra into Cerberus.
- [x] Preserve Project Hermes for the Windows 11 laptop.
- [x] Define the current Windows 10 system's future as Ares V1.
- [x] Make streaming the final deployment phase.

## 2. Hardware decisions and acquisition

- [x] Lock the MUSETEX K2 case.
- [x] Receive the MUSETEX K2.
- [x] Lock the MSI MAG B850 Tomahawk MAX WiFi.
- [x] Receive the motherboard.
- [x] Lock the AMD Ryzen 9 9900X.
- [x] Lock the MSI MAG CORELIQUID A15 360, subject to clearance.
- [x] Lock 64 GB (2x32 GB) DDR5-6000 EXPO; exact kit remains open.
- [x] Lock a 2 TB primary NVMe SSD; exact model remains open.
- [x] Lock RTX 5060 Ti 16 GB as the primary GPU specification.
- [x] Lock a compact NVIDIA secondary-GPU direction; T400 preferred, P620 fallback.
- [x] Lock the Corsair RM850e (2025).
- [x] Lock the CyberPower CP1500PFCLCD.
- [ ] Purchase the remaining locked components.
- [ ] Record tax-inclusive invoices and revise the final budget ceiling.

## 3. Compatibility validation

- [ ] Inspect and inventory the arrived case and motherboard.
- [ ] Add sanitized arrival photography.
- [ ] Validate A15 360 radiator/tube clearance.
- [ ] Select the exact primary GPU and confirm dimensions/outputs.
- [ ] Validate PCIe slot allocation for both GPUs and optional USB expansion.
- [ ] Confirm M.2 placement and lane-sharing behavior.
- [ ] Confirm Mini DisplayPort adapters and six-display cable plan.
- [ ] Confirm Linux compatibility for capture card, Stream Deck workflow, RGB, AIO, and peripherals.

## 4. Assembly and firmware

- [ ] Bench-build CPU, cooler, memory, and NVMe.
- [ ] Complete first POST and baseline temperature inspection.
- [ ] Update the MSI BIOS using M-FLASH.
- [ ] Configure UEFI, Secure Boot strategy, TPM, SVM, EXPO after baseline testing, Resizable BAR, and fan curves.
- [ ] Install hardware in the MUSETEX K2.
- [ ] Install both GPUs without obstructing airflow or required slots.
- [ ] Complete cable management and repeat cold-boot tests.

## 5. Fedora foundation

- [ ] Create and verify Fedora KDE installation media.
- [ ] Install Fedora with encryption and documented storage layout.
- [ ] Apply updates and firmware through supported Fedora mechanisms.
- [ ] Install and validate NVIDIA drivers.
- [ ] Validate all six displays.
- [ ] Configure backups and recovery media.

## 6. Security and workstation platform

- [ ] Validate SELinux enforcing and firewall policy.
- [ ] Integrate the hardware security key where supported.
- [ ] Build the Desktop & Workflow Environment.
- [ ] Install Git, Python, Podman, Distrobox, and development tooling.
- [ ] Configure Ansible/IaC control-node functions.
- [ ] Configure Kubernetes, AWS, and COC management tooling.
- [ ] Add optional local virtualization only if required.
- [ ] Complete Athena integration groundwork.

## 7. Validation, cutover, and streaming

- [ ] Complete hardware, Fedora, security, workflow, COC, and recovery testing.
- [ ] Document the accepted platform baseline.
- [ ] Configure OBS and the PS5 streaming workflow last.
- [ ] Promote Cerberus to primary workstation.
- [ ] Retire the Windows 10 workstation from primary duty.
- [ ] Hand the retired hardware to the Ares V1 project.
