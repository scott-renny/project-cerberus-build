# Backup, Encrypted Recovery, and Rebuild

**Status:** Planned  
**Owner:** Cerberus Operations  
**Version:** 0.1  
**Last reviewed:** 2026-08-14

## Purpose

Protect approved Cerberus data, validate isolated restoration, recover access to LUKS-protected storage, and rebuild the workstation from a trusted baseline when integrity cannot be established.

## Scope

Protect reviewed user data, infrastructure repositories, documentation, selected configuration, and required application data. Exclude caches, reproducible packages, unreviewed downloads, secrets without an approved storage design, and disposable lab environments.

Repository locations, passwords, encryption material, private hostnames, addresses, and snapshot identifiers remain outside the public repository.

## Routine backup validation

1. Confirm the expected source categories and exclusions.
2. Confirm the backup destination is mounted and belongs to the approved repository.
3. Run the approved Linux Mint backup job with least privilege.
4. Review completion status, warnings, duration, and new-data volume.
5. Restore a representative file into an isolated temporary directory.
6. Compare its hash or content with the trusted source.
7. Remove the temporary restored copy after evidence is recorded.
8. Confirm backup-age monitoring and Wazuh visibility.

## LUKS recovery readiness

Use only read-only discovery until the target device is positively identified:

```bash
lsblk -f
findmnt
sudo cryptsetup luksDump /dev/<verified-device>
```

- Never guess a block-device path.
- Never publish LUKS headers, key material, passphrases, recovery records, or unredacted storage output.
- Keep recovery material offline and test it through an approved controlled method.
- Back up a LUKS header only to an encrypted, access-controlled location using current cryptsetup guidance.
- Stop if storage identity, RAID/LVM relationships, or the effect of a repair command is uncertain.

## Selective restore

1. Choose a recovery point approved for the incident or change.
2. Restore into an isolated destination.
3. Scan restored data and inspect ownership, permissions, links, and executable content.
4. Compare representative hashes.
5. Move only approved data into the production profile.
6. Rebuild applications from trusted Linux Mint or verified publisher sources.
7. Rotate credentials when exposure cannot be excluded.

## Full trusted rebuild

1. Preserve evidence when compromise is possible.
2. Confirm the rebuild decision and positively identify the destination disk.
3. Verify current Linux Mint installation media using official signing material and checksums.
4. Install in UEFI mode with the approved LUKS-backed layout and standard daily user.
5. Apply updates and validate Secure Boot, AppArmor, firewalld, and listening services.
6. Re-enroll Wazuh using a new approved identity and close temporary enrollment access.
7. Restore only reviewed data through the selective-restore procedure.
8. Rebuild hardware-key registrations and applications deliberately.
9. Complete a new backup and isolated restore.
10. Obtain acceptance before sanitizing or repurposing prior media.

## Stop conditions

Stop for uncertain target storage, failed media verification, unavailable recovery material, malware detection, untrusted snapshots, missing Wazuh telemetry, failed restore comparison, or pressure to restore an entire legacy profile.

## Validation gate

This runbook remains Planned until a backup, isolated restore, recovery-material test, and controlled rebuild exercise pass with sanitized evidence.
