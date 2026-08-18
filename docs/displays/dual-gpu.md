# Linux Mint Dual-GPU Configuration

## Locked architecture

- **Primary:** NVIDIA RTX 5060 Ti 16 GB. Exact reputable model remains open.
- **Secondary:** compact low-power NVIDIA workstation/display GPU. T400 preferred; P620 fallback.

Both cards remain in one NVIDIA Linux driver ecosystem.

## Roles

### RTX 5060 Ti 16 GB

- Primary Cinnamon desktop displays
- CUDA and local AI experimentation
- GPU-accelerated creative/development work
- NVENC for OBS
- High-resolution/high-refresh outputs

### T400/P620-class secondary

- Auxiliary displays only
- Minimal slot width and power
- Preserve lower-case airflow
- No default GPU passthrough plan

## Motherboard and storage validation

Use the owned MSI MAG B850 Tomahawk MAX WiFi and current manual to confirm:

- primary GPU in the CPU-connected primary slot;
- lower-slot physical clearance and chipset lane allocation;
- M2_3 sharing behavior and whether it must remain unused;
- primary SSD placement in a non-conflicting M.2 slot;
- optional USB expansion only after both GPUs are mapped;
- slot-mounted anti-sag support only if it does not obstruct the secondary card.

## Linux Mint deployment checklist

- [ ] Install the supported Linux Mint NVIDIA driver path deliberately.
- [ ] Document Secure Boot handling for third-party NVIDIA modules.
- [ ] Confirm both GPUs appear in Linux hardware and NVIDIA tooling.
- [ ] Confirm Cinnamon detects every display.
- [ ] Configure resolution, refresh, scaling, orientation, and primary output.
- [ ] Confirm CUDA on the primary GPU.
- [ ] Confirm OBS NVENC.
- [ ] Validate reboot, logout/login, kernel/driver update, and sleep/wake.
- [ ] Validate mixed-refresh and mixed-scaling behavior.
- [ ] Preserve a text-console recovery procedure if the graphical stack fails.

Do not describe the secondary GPU as Intel or AMD. Do not purchase it until exact outputs, adapters, slot clearance, and price are verified.
