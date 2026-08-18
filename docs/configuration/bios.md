# BIOS and Firmware Configuration

Use only firmware published for the exact MSI MAG B850 Tomahawk MAX WiFi. Record the version, date, source, checksum where available, and outcome without publishing serial numbers.

## Deployment order

1. Complete the bench build and first POST.
2. Inspect temperatures and component detection.
3. Update the motherboard BIOS with MSI M-FLASH from a verified FAT32 USB drive.
4. Load optimized defaults after the update.
5. Reconfirm hardware detection.
6. Apply required settings one group at a time.
7. Install Linux Mint only after the firmware baseline is stable.

The motherboard Flash BIOS Button is a recovery option, not the default update method when normal UEFI access works.

## Baseline checklist

- [ ] CPU, cooler/pump, memory, NVMe, and both intended PCIe slots detected.
- [ ] Current stable BIOS installed successfully.
- [ ] UEFI boot enabled; legacy/CSM disabled unless a proven exception exists.
- [ ] TPM/fTPM visible.
- [ ] Secure Boot strategy documented for Linux Mint and the selected NVIDIA driver path.
- [ ] SVM enabled for optional KVM/QEMU use.
- [ ] IOMMU enabled if required for future testing.
- [ ] Resizable BAR enabled if supported by the final GPU configuration.
- [ ] EXPO enabled only after baseline memory testing.
- [ ] M.2 and PCIe lane-sharing configuration matches the documented slot map.
- [ ] Fan and pump headers assigned correctly.
- [ ] Fan curves reviewed after thermal testing.
- [ ] Restore-on-power-loss behavior selected deliberately.
- [ ] Sanitized configuration summary saved.

Change one performance-related setting at a time and retest stability.
