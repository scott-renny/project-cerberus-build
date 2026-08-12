# Upgrade Roadmap

Upgrades are need-driven rather than date-driven. This roadmap applies after the future Cerberus rebuild is operational; Version 1 remains the existing Windows 10 dual-monitor baseline.

## Storage

Add a second 2 TB or 4 TB NVMe SSD when free space, VM activity, or project separation justifies it. Confirm lane and port sharing on the owned MSI MAG B850 Tomahawk MAX WiFi before installation.

## Memory

Consider 128 GB only when measured VM and container workloads regularly approach the planned 64 GB. Four-DIMM operation may require a lower memory speed.

## Networking

Consider faster-than-2.5 Gb Ethernet only when the switch, server, cabling, and actual transfer workloads can benefit.

## Graphics

Select the initial RTX 5060 Ti 16 GB model and secondary display GPU only after physical and electrical slot validation. After the build is operational, replace the primary GPU only when measured gaming, AI, encoding, or editing requirements exceed it. Preserve the auxiliary display strategy unless a simpler single-card solution can drive all required displays.

## Expansion cards

Add a USB expansion card only if the final primary and secondary GPU layout leaves a suitable accessible slot with acceptable lane allocation.

## Power protection

The CyberPower CP1500PFCLCD 1500 VA / 1000 W is the current UPS choice. Confirm load percentage, desired runtime, USB monitoring, and graceful-shutdown behavior using measured final-system power before treating it as validated.
