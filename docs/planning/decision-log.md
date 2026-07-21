# Decision Log

## ADR-001: Keep the Ryzen 9 9900X

**Status:** Proposed  
**Reason:** Twelve cores and twenty-four threads suit concurrent virtual machines, containers, development, and streaming workloads.

## ADR-002: Use two GPUs

**Status:** Accepted  
**Decision:** Use an NVIDIA primary GPU and a low-power Intel GPU for additional direct display outputs.  
**Reason:** Six monitors exceed the typical four-display limit of one consumer GPU, and direct connections are preferred over an MST or USB display hub.

## ADR-003: Begin with one SSD

**Status:** Accepted  
**Decision:** Install one 2 TB NVMe SSD initially.  
**Reason:** Storage is easy to expand later, while the initial budget is more valuable for CPU, memory, graphics, and a quality power supply.

## ADR-004: Prefer wired networking

**Status:** Accepted  
**Decision:** Use 2.5 Gb Ethernet as the primary network connection.  
**Reason:** The workstation will connect to an existing switch and access-point infrastructure; Wi-Fi 7 is not a purchasing priority.

## ADR-005: Use air cooling

**Status:** Proposed  
**Reason:** A high-quality dual-tower air cooler offers strong value, low maintenance, and adequate performance when case clearance is verified.

