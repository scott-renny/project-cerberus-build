# Linux Mint Cinnamon Deployment

Linux Mint Cinnamon is the locked Cerberus host operating system.

## Phase 1: Media and storage

- [ ] Download the current supported Linux Mint Cinnamon image from the official source.
- [ ] Verify the published SHA256 checksum and signing information.
- [ ] Create and test installation media.
- [ ] Confirm the primary SSD and non-conflicting M.2 slot.
- [ ] Document the encryption and filesystem layout before installation.

## Phase 2: Installation

- [ ] Boot in UEFI mode.
- [ ] Install with full-disk encryption.
- [ ] Create the primary user without publishing identifying information.
- [ ] Apply initial updates with Update Manager or supported `apt` commands.
- [ ] Confirm AppArmor and UFW status.
- [ ] Create and store recovery information securely offline.

## Phase 3: Firmware and NVIDIA

- [ ] Use fwupd/LVFS where supported and document unsupported devices.
- [ ] Install the recommended NVIDIA driver through Linux Mint Driver Manager.
- [ ] Document Secure Boot module signing or MOK enrollment if required.
- [ ] Confirm both GPUs, CUDA, NVENC, and all displays.
- [ ] Test recovery to a text console.

## Phase 4: Desktop foundation

- [ ] Configure Cinnamon displays, scaling, orientation, workspaces, and shortcuts.
- [ ] Add Flatpak applications selectively.
- [ ] Configure LocalSend if approved.
- [ ] Configure backups before producing irreplaceable work.

## Phase 5: Engineering stack

- [ ] Git and GitHub CLI
- [ ] Bash, terminal, and tmux
- [ ] VS Code or VSCodium
- [ ] Python and uv
- [ ] Docker Engine and Docker Compose
- [ ] Wireshark, Nmap, and approved security tools
- [ ] Ansible
- [ ] kubectl, Helm, and k9s
- [ ] AWS CLI and IaC tooling when required
- [ ] Selected technical-notes workflow
- [ ] Bitwarden or KeePassXC and security-key integration

## Phase 6: Optional compatibility

Install KVM/QEMU and virt-manager only when a concrete temporary VM requirement exists. Use containers for isolated development environments where appropriate.

## Phase 7: COC and Athena

Configure authorized access to the broader environment, infrastructure repositories, dashboards, and Athena development interfaces.

## Phase 8: Streaming — last

After all other phases are stable, configure the Linux-compatible capture card, OBS, NVENC, audio, camera, controls, scenes, Twitch workflow, and Stream Deck alternative.
