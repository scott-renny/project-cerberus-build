# Fedora KDE Deployment

Fedora KDE Plasma is the locked Cerberus host operating system.

## Phase 1: Media and storage

- [ ] Download the current supported Fedora KDE image from the official source.
- [ ] Verify the image checksum/signature.
- [ ] Create and test installation media.
- [ ] Confirm the primary SSD and non-conflicting M.2 slot.
- [ ] Document the encryption and filesystem layout before installation.

## Phase 2: Installation

- [ ] Boot in UEFI mode.
- [ ] Install with full-disk encryption.
- [ ] Create the primary user without publishing identifying information.
- [ ] Apply initial updates.
- [ ] Confirm SELinux enforcing and firewall status.
- [ ] Create and store recovery information securely offline.

## Phase 3: Firmware and NVIDIA

- [ ] Use fwupd/LVFS where supported and document unsupported devices.
- [ ] Install NVIDIA drivers through the selected Fedora-supported approach.
- [ ] Document Secure Boot module-signing/enrolment if required.
- [ ] Confirm both GPUs, CUDA, NVENC, and all displays.
- [ ] Test recovery to a text console.

## Phase 4: Desktop foundation

- [ ] Configure KDE displays, scaling, orientation, activities, desktops, and shortcuts.
- [ ] Add Flatpak/Flathub selectively.
- [ ] Configure KDE Connect and LocalSend if approved.
- [ ] Configure backups before producing irreplaceable work.

## Phase 5: Engineering stack

- [ ] Git and GitHub CLI
- [ ] Bash, Konsole, and tmux
- [ ] VS Code or VSCodium
- [ ] Python and uv
- [ ] Podman and Podman Desktop
- [ ] Distrobox
- [ ] Wireshark, Nmap, and approved security tools
- [ ] Ansible
- [ ] kubectl, Helm, and k9s
- [ ] AWS CLI and IaC tooling when required
- [ ] Obsidian or selected technical-notes workflow
- [ ] Bitwarden/KeePassXC and security-key integration

## Phase 6: Optional compatibility

Install KVM/QEMU and virt-manager only when a concrete temporary VM requirement exists. Use Distrobox for alternate Linux userspaces where it is sufficient.

## Phase 7: COC and Athena

Configure authorized access to the broader environment, infrastructure repositories, dashboards, and Athena development interfaces.

## Phase 8: Streaming — last

After all other phases are stable, configure the Linux-compatible capture card, OBS, NVENC, audio, camera, controls, scenes, Twitch workflow, and Stream Deck alternative.
