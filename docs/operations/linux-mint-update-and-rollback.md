# Linux Mint Update and Rollback

## Purpose

Apply Linux Mint, Ubuntu-base, kernel, Flatpak, firmware, and approved third-party updates with a verified backup, an explicit recovery path, and post-reboot security validation.

## Preconditions

- The installed Linux Mint release is supported.
- A recent backup has passed integrity checks.
- Encryption recovery material is available offline.
- The recommended NVIDIA driver and current kernel are recorded.
- No unresolved storage, package-manager, or security-control failure exists.

## Update procedure

1. Record the Linux Mint release, Ubuntu base, kernel, free space, failed services, AppArmor state, UFW state, and graphics health.
2. Review available updates in Update Manager.
3. Apply normal package updates through Update Manager or the supported `apt` workflow.
4. Apply Flatpak and firmware updates separately so failures remain attributable.
5. Reboot when the kernel, NVIDIA driver, firmware, or security updates require it.
6. Validate login, all displays, networking, audio, encryption, AppArmor, UFW, Wazuh, Docker, backups, and representative engineering tools.
7. Record the update and validation result.

## Recovery

- Use an earlier kernel from GRUB when a new kernel prevents a normal boot.
- Use a text console or recovery mode when the graphical session fails.
- Re-select the recommended NVIDIA driver through Driver Manager if driver packaging is the confirmed cause.
- Restore configuration or data only from the verified backup.
- For an unsuccessful major Linux Mint upgrade, stop and follow current official Linux Mint recovery guidance; do not improvise destructive package removal.

## References

- [Linux Mint documentation](https://linuxmint.com/documentation.php)
- [Ubuntu security notices](https://ubuntu.com/security/notices)
