# Fedora Update and Rollback

**Status:** Planned  
**Owner:** Cerberus Operations  
**Version:** 0.1  
**Last reviewed:** 2026-08-14

## Purpose

Apply Fedora, kernel, Flatpak, firmware, and approved third-party updates with a verified backup, an explicit rollback path, and post-reboot security validation.

## Preconditions

- Approved maintenance window and change record
- Current successful backup and representative restore evidence
- Fedora release is supported
- Critical workflows are closed or safely paused
- Recovery media and LUKS recovery material are available privately
- Current kernel and NVIDIA state are recorded without publishing identifiers

## Preflight

1. Record Fedora release, kernel, Secure Boot state, free space, failed services, and current graphical/compute health.
2. Review pending RPM, Flatpak, firmware, and third-party repository updates.
3. Read release notes for kernel, NVIDIA, Secure Boot, SELinux, bootloader, and filesystem changes.
4. Stop if dependencies would be removed unexpectedly or a required third-party repository is not ready.

Useful read-only checks:

```bash
cat /etc/fedora-release
uname -r
mokutil --sb-state
systemctl --failed
df -h /
dnf check-update
flatpak remote-ls --updates
fwupdmgr get-updates
nvidia-smi
```

`dnf check-update` may return a nonzero status when updates are available; interpret its documented result rather than treating every nonzero status as failure.

## Routine update

1. Refresh metadata and review the transaction before accepting it.
2. Apply Fedora package updates using the supported DNF workflow.
3. Apply reviewed Flatpak updates.
4. Apply firmware only after confirming vendor guidance, power stability, and rollback limitations.
5. Reboot when the kernel, firmware, graphics stack, system libraries, or security controls changed.

```bash
sudo dnf upgrade --refresh
flatpak update
```

Do not add automatic confirmation flags until the proposed transaction has been reviewed.

## Validation

After reboot, verify:

- expected kernel and Fedora release;
- Secure Boot state;
- encrypted filesystems mounted as designed;
- SELinux Enforcing;
- firewalld active with the approved zone;
- no unexpected listening services;
- Wazuh connected and producing telemetry;
- backup job healthy;
- NVIDIA, CUDA/NVENC where required, and all displays functional;
- representative engineering and authentication workflows.

## Rollback and recovery

- For a kernel or graphics regression, boot the previously known-good kernel from the boot menu and use the NVIDIA recovery runbook.
- Review `dnf history` before considering a package transaction reversal. Do not reverse a broad transaction without understanding its dependencies.
- Restore configuration or user data only from the approved recovery point.
- For an unsuccessful Fedora release upgrade, stop and use current Fedora recovery guidance; do not improvise destructive package removal.
- Record the failed validation, rollback action, remaining risk, and follow-up owner.

## Validation gate

This runbook remains Planned until a routine update and a controlled previous-kernel recovery both pass with sanitized evidence.

## Official references

- [Fedora system upgrade documentation](https://docs.fedoraproject.org/en-US/quick-docs/upgrading-fedora-offline/)
- [Fedora security information](https://fedoraproject.org/security)
