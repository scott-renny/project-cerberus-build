# Cerberus Operations Runbooks

These procedures govern recurring maintenance, recovery, monitoring, and incident actions for the Linux Mint Cinnamon workstation. They are planning baselines until Cerberus is installed and each procedure passes its validation gate.

## Status model

| Status | Meaning |
|---|---|
| Planned | Procedure is documented before the platform is available |
| Draft | Platform exists and the procedure is ready for a controlled test |
| Lab Validated | Positive, failure, and recovery paths passed with sanitized evidence |
| Operational | Approved for routine Cerberus use |
| Retired | Superseded or no longer applicable |

## Runbooks

| Procedure | Status | Validation gate |
|---|---|---|
| [Linux Mint Update and Rollback](linux-mint-update-and-rollback.md) | Planned | package, Flatpak, firmware, kernel, reboot, and rollback paths tested |
| [Backup, Encrypted Recovery, and Rebuild](backup-encrypted-recovery-and-rebuild.md) | Planned | backup, isolated restore, LUKS recovery, and trusted rebuild exercised |
| [Wazuh Agent Health and Re-enrollment](wazuh-agent-health.md) | Planned | telemetry interruption detected and restored |
| [Endpoint Isolation and Reconnection](endpoint-isolation-and-reconnection.md) | Planned | isolation and approved reconnection tested without losing evidence |
| [NVIDIA and Display Recovery](nvidia-display-recovery.md) | Planned | graphical failure recovered through a prior kernel or validated driver path |
| [Hardware Security-Key Recovery](hardware-security-key-recovery.md) | Planned | primary-key loss simulated with a tested backup factor |

## Operating rules

- Record a change or incident identifier, operator, start time, expected outcome, and rollback point.
- Use current official Linux Mint, Wazuh, hardware-vendor, and application documentation at execution time.
- Never publish credentials, recovery material, serial numbers, private addresses, enrollment secrets, or raw system exports.
- Stop when the target device, storage device, package transaction, or recovery point is uncertain.
- Preserve evidence before destructive repair when compromise is possible.
- Keep Cerberus-specific commands here and link to them from the wider COC incident playbooks.
