# Dual-GPU Configuration

## Intended roles

- **NVIDIA GPU:** primary desktop, high-resolution displays, OBS encoding, CUDA, AI, editing, and gaming.
- **Intel GPU:** auxiliary displays only unless a later workload is deliberately assigned to it.

## Setup checklist

- [ ] Install current AMD chipset drivers.
- [ ] Install the NVIDIA driver from the official source.
- [ ] Install the Intel Arc driver from the official source.
- [ ] Confirm both adapters appear without errors in Device Manager.
- [ ] Connect and identify one display at a time.
- [ ] Set resolution, refresh rate, scaling, orientation, and primary display.
- [ ] Assign performance-sensitive applications to the NVIDIA GPU in Windows graphics settings.
- [ ] Verify OBS uses the NVIDIA encoder.
- [ ] Reboot and confirm the layout persists.
- [ ] Test sleep, wake, driver updates, and mixed refresh rates.

Document exact driver versions when a stable configuration is established.

