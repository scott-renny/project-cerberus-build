# Fedora System Hardening

## Trust baseline

- [ ] Install Fedora from verified official media.
- [ ] Use full-disk encryption and store recovery material securely offline.
- [ ] Keep SELinux enforcing.
- [ ] Enable and validate the host firewall.
- [ ] Use a standard user for routine work and elevation only when required.
- [ ] Configure Secure Boot using a documented approach compatible with the selected NVIDIA driver installation.
- [ ] Confirm TPM visibility and use where it adds recoverable security value.
- [ ] Integrate the dedicated hardware security key where supported.
- [ ] Apply operating-system, kernel, driver, Flatpak, and firmware updates deliberately.
- [ ] Disable unnecessary listening services and remote access.
- [ ] Restrict SSH server installation to a defined need; the SSH client is expected.
- [ ] Separate administrative browser profiles and credentials from normal browsing.
- [ ] Keep secrets outside Git and use an approved password/secrets workflow.

## Workload isolation

- [ ] Use rootless Podman where practical.
- [ ] Treat Distrobox environments as convenience containers, not security boundaries.
- [ ] Use disposable KVM/QEMU VMs for local isolation only when appropriate.
- [ ] Keep specialized or untrusted workloads on Ares or other dedicated infrastructure when required.
- [ ] Do not place production secrets in disposable labs or screenshots.

## Network position

Cerberus is a stationary trusted operator workstation connected through Olympus/UniFi. It does not require WireGuard by default. VLAN placement, DHCP reservation, and least-required firewall policy define its access to management and security networks.

## Recovery

- [ ] Create and verify recovery media.
- [ ] Document encrypted-disk recovery.
- [ ] Back up user data, configuration, and infrastructure code.
- [ ] Test restoration of representative data.
- [ ] Document NVIDIA-driver and kernel rollback/recovery.
- [ ] Preserve a path to a text console if the graphical session fails.

Document the approach without publishing keys, addresses, host aliases, or sensitive exports.
