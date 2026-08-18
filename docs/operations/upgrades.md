# Platform Evolution Roadmap

Changes are driven by measured need and compatibility, not novelty.

## Storage

Add NVMe storage when capacity, project separation, AI data, containers, or disposable VM use justifies it. Preserve documented PCIe/M.2 lane allocation and avoid M2_3 if it reduces required secondary-GPU bandwidth.

## Memory

Consider 128 GB only when measured engineering, container, AI, or optional VM workloads regularly approach 64 GB. Four-DIMM operation may require lower memory speed.

## Graphics and displays

Replace the primary GPU only when measured CUDA, AI, encoding, creative, or display needs exceed the RTX 5060 Ti 16 GB. Preserve the compact secondary-display strategy unless a simpler supported solution can reliably drive all six displays.

## Networking

Use the onboard 2.5 Gb Ethernet initially. Upgrade only when Olympus, switching, cabling, servers, and actual transfers benefit.

## Expansion

Add USB or capture expansion only after proving physical slot access, lane allocation, Linux Mint support, and power requirements.

## Linux Mint lifecycle

Track supported Linux Mint releases, kernel/NVIDIA compatibility, configuration changes, recovery procedures, and upgrade validation. Test major platform upgrades before treating them as accepted.

## Automation maturity

Gradually move repeatable authorized infrastructure work into Git, Ansible, and IaC. Avoid automating poorly understood processes or committing secrets.

## Power protection

Validate the CP1500PFCLCD using measured load, USB monitoring, desired runtime, and controlled-shutdown testing. Give always-on infrastructure separate protection rather than overloading the Cerberus UPS.
