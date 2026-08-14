# NVIDIA and Display Recovery

**Status:** Planned  
**Owner:** Cerberus Operations  
**Version:** 0.1  
**Last reviewed:** 2026-08-14

## Purpose

Recover the Fedora graphical environment after a kernel, NVIDIA-driver, Secure Boot module-signing, KDE, or multi-display failure without disabling security controls as a shortcut.

## Initial checks

1. Preserve the prior working kernel, driver version, display layout, and change record.
2. Attempt a text console before changing packages.
3. Record Secure Boot, kernel, loaded modules, GPU discovery, and relevant boot logs.

```bash
uname -r
mokutil --sb-state
lsmod | grep -E '^nvidia'
nvidia-smi
systemctl --failed
sudo journalctl -b -p warning --no-pager
sudo journalctl -b -1 -p warning --no-pager
```

## Recovery sequence

1. If the failure followed a kernel or driver update, boot the last known-good kernel from the boot menu.
2. Confirm whether the NVIDIA modules load and whether Secure Boot rejected an unsigned module.
3. Use the documented Fedora-supported NVIDIA packaging and module-signing method selected during deployment.
4. Do not disable Secure Boot or SELinux merely to make the desktop start.
5. Rebuild only the affected driver/module path using current publisher instructions.
6. Restore the documented KDE display layout after the graphics stack is stable.
7. Test every GPU, display, required resolution/refresh rate, CUDA/NVENC workflow, sleep/wake behavior, and reboot persistence.
8. Record the accepted kernel/driver combination and follow-up action.

## Stop conditions

Stop for firmware uncertainty, repeated GPU resets, signs of hardware damage, required package removal not understood, unsigned modules with no approved signing path, or any instruction that risks losing the known-good kernel.

## Validation gate

This runbook remains Planned until a controlled graphical failure is recovered through the text console and known-good kernel path with all six displays and required acceleration validated.
