# Decision Log

## ADR-001: Build rather than buy

**Status:** Accepted  
**Decision:** Build Cerberus from individually selected components.  
**Reason:** Available prebuilt systems forced unacceptable compromises in display capacity, expansion, cooling, power quality, component transparency, and upgradeability.

## ADR-002: Use Fedora KDE Plasma

**Status:** **Locked**  
**Decision:** Fedora KDE Plasma replaces the earlier Windows 11 host plan.  
**Reason:** Fedora supports the Linux engineering, cybersecurity, container, automation, Kubernetes, cloud, and learning objectives. KDE is well suited to the six-display workflow.

## ADR-003: Make Cerberus the engineering and COC control platform

**Status:** **Locked**  
**Decision:** Cerberus is the interactive Linux engineering workstation, trusted COC operator station, and Ansible/IaC control node.  
**Reason:** Permanent services already have dedicated systems. Cerberus should manage them without becoming another always-on server.

## ADR-004: Consolidate Project Hydra into Cerberus

**Status:** Accepted  
**Decision:** Discontinue Hydra as a standalone project and move its intended desktop/workspace scope into Cerberus.  
**Reason:** KDE desktop design, display topology, automation, hardening, and platform deployment must be engineered together. Hydra had not reached implementation, so no code migration is required.

## ADR-005: Keep Project Hermes separate

**Status:** Accepted  
**Decision:** Keep Hermes as the Windows 11 laptop automation project.  
**Reason:** Hermes remains appropriate for Windows and PowerShell. Cerberus requires Fedora-native configuration rather than a forced port.

## ADR-006: Repurpose the retired workstation as Ares V1

**Status:** Accepted direction  
**Decision:** After Cerberus is accepted, retire the current Windows 10 workstation from primary duty and reuse its hardware as Ares V1.  
**Reason:** This extends the hardware lifecycle and separates specialized or isolated workloads from Cerberus.

## ADR-007: Use the AMD Ryzen 9 9900X

**Status:** **Locked**  
**Reason:** Twelve cores and twenty-four threads suit demanding concurrent engineering, security, AI, encoding, and content-creation workloads.

## ADR-008: Use the MSI MAG B850 Tomahawk MAX WiFi

**Status:** **Locked; owned and arrived**  
**Reason:** The board provides the AM5 platform and expansion foundation. The exact owned board can be used for slot, lane, header, and M.2-sharing validation.

## ADR-009: Use a 360 mm MSI liquid cooler

**Status:** **Locked, pending clearance validation**  
**Decision:** MSI MAG CORELIQUID A15 360.  
**Reason:** Sustained workloads and the showcase chassis benefit from the cooling capacity; physical fit must still be proven.

## ADR-010: Lock 64 GB DDR5-6000 EXPO

**Status:** Specification locked; exact kit selecting  
**Decision:** Use 64 GB as a two-DIMM 2x32 GB DDR5-6000 EXPO kit.  
**Reason:** It provides strong workstation capacity while preserving a practical AM5 memory configuration.

## ADR-011: Lock a two-NVIDIA-GPU display architecture

**Status:** **Locked architecture**  
**Decision:** Use an RTX 5060 Ti 16 GB primary GPU and a compact, low-power NVIDIA secondary display GPU. Prefer an NVIDIA T400; retain the P620 as fallback.  
**Reason:** Six direct displays require two GPUs. One NVIDIA driver ecosystem reduces avoidable Fedora complexity, while a workstation-class secondary card preserves clearance and airflow.

## ADR-012: Keep the RTX 5060 Ti model flexible

**Status:** Exact model selecting  
**Decision:** Preserve the RTX 5060 Ti 16 GB requirement without requiring the unavailable/overpriced MSI Ventus model.  
**Reason:** VRAM, Fedora support, CUDA, NVENC, physical dimensions, outputs, cooling, and price matter more than manufacturer branding.

## ADR-013: Use one 2 TB NVMe SSD initially

**Status:** Specification locked; exact model selecting  
**Decision:** Start with one 2 TB M.2 NVMe SSD and preserve non-conflicting M.2 expansion paths.  
**Reason:** Storage can be expanded later. The initial layout must not unnecessarily reduce the secondary GPU's lower-slot bandwidth.

## ADR-014: Use the Corsair RM850e (2025)

**Status:** **Locked; purchase pending**  
**Reason:** 850 W, ATX 3.1, modular cabling, and appropriate GPU connectivity provide suitable capacity and headroom. Only the modular cables supplied or explicitly approved for this PSU may be used.

## ADR-015: Use dedicated power protection

**Status:** **Locked; purchase pending**  
**Decision:** CyberPower CP1500PFCLCD, 1500 VA / 1000 W.  
**Reason:** Pure-sine-wave output, AVR, monitoring, and controlled shutdown suit the workstation. Cerberus, essential displays, and selected networking—not the entire lab—will use its battery-backed outlets.

## ADR-016: Make virtualization optional

**Status:** Accepted  
**Decision:** Install KVM/QEMU and virt-manager only when a defined temporary workstation use case exists.  
**Reason:** Ares and other dedicated systems own specialized workloads; Cerberus is not the primary VM host.

## ADR-017: Configure streaming last

**Status:** **Locked deployment order**  
**Decision:** Install and validate OBS, PS5 capture, Stream Deck alternatives, scenes, audio, and streaming only after the engineering/COC platform is stable.  
**Reason:** Streaming must not dictate or destabilize the core workstation architecture.
