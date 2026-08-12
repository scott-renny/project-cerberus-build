# Decision Log

## ADR-001: Keep the Ryzen 9 9900X

**Status:** Accepted direction  
**Decision:** Plan the Cerberus rebuild around the AMD Ryzen 9 9900X.  
**Reason:** Twelve cores and twenty-four threads suit demanding concurrent cybersecurity, development, analysis, AI, encoding, and content-creation workloads.

## ADR-002: Use two GPUs

**Status:** Accepted  
**Decision:** Use an NVIDIA RTX 5060 Ti 16 GB as the primary GPU and a small, low-power secondary GPU for additional direct display outputs. The exact models remain under selection.  
**Reason:** Six monitors exceed the typical four-display limit of one consumer GPU, and direct connections are preferred over an MST or USB display hub.

## ADR-003: Begin with one SSD

**Status:** Accepted  
**Decision:** Install one 2 TB NVMe SSD initially.  
**Reason:** Storage is easy to expand later, while the initial budget is more valuable for CPU, memory, graphics, and a quality power supply.

## ADR-004: Prefer wired networking

**Status:** Accepted  
**Decision:** Use 2.5 Gb Ethernet as the primary network connection.  
**Reason:** The workstation will connect to existing network infrastructure; Wi-Fi is available on the selected motherboard but is not the purchasing driver.

## ADR-005: Use a 360 mm liquid cooler

**Status:** Current choice  
**Decision:** Use the MSI MAG CORELIQUID A15 360, subject to final case-clearance validation.  
**Reason:** This replaces the earlier proposed air-cooling direction.

## ADR-006: Select the MSI MAG B850 Tomahawk MAX WiFi

**Status:** Purchased / owned — arrived  
**Decision:** The Cerberus motherboard is the MSI MAG B850 Tomahawk MAX WiFi.  
**Reason:** The exact owned board can now be inspected and its manual used to validate PCIe slot allocation, physical spacing, headers, and resource sharing.

## ADR-007: Re-select the primary GPU model

**Status:** In progress  
**Decision:** Preserve the RTX 5060 Ti 16 GB requirement while selecting a replacement model.  
**Reason:** The original MSI Ventus model became unavailable. No exact replacement is final yet.

## ADR-008: Keep Version 1 separate from Cerberus

**Status:** Accepted  
**Decision:** Version 1 remains the existing Windows 10 dual-monitor baseline. The Cerberus rebuild is the planned future physical workstation.  
**Reason:** Separating current-state documentation from future-build decisions prevents planned hardware from being mistaken for installed hardware.

## ADR-009: Build Cerberus instead of buying a prebuilt workstation

**Status:** Accepted  
**Decision:** Build the Cerberus workstation from individually selected components rather than purchase a complete prebuilt system.  
**Reason:** It was too difficult to find a purchasable system that combined the required concurrent-workload performance, 64 GB memory direction, NVIDIA compute and encoding, six-monitor dual-GPU layout, usable PCIe expansion, cooling, power quality, and upgrade flexibility without unacceptable compromises. A custom build provides control over the exact motherboard, slot layout, clearances, cooling, power supply, and future expansion.

## ADR-010: Separate Cerberus from Project Ares

**Status:** Accepted  
**Decision:** Use Cerberus as the primary cybersecurity workstation and command center. Develop Project Ares as a separate physical system for specialized, isolated, or infrastructure workloads.  
**Reason:** Separating these roles keeps Cerberus focused on interactive workstation work and avoids presenting it as the primary virtualization host. Cerberus may still support occasional local VMs, WSL, or containers when useful.

## ADR-011: Repurpose the retired Windows 10 workstation as Ares V1

**Status:** Accepted direction  
**Decision:** After Cerberus is validated and becomes the primary workstation, retire the existing Version 1 Windows 10 system from that role and repurpose its hardware as Ares V1.  
**Reason:** Reusing the existing system gives Ares a physical platform without purchasing an entirely new machine, extends the useful life of the hardware, and preserves the separation between Cerberus interactive workloads and Ares specialized or isolated workloads. The Ares operating system, final responsibilities, and upgrade needs remain separate decisions.
