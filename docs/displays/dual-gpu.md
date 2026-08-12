# Dual-GPU Configuration

## Intended roles

- **NVIDIA RTX 5060 Ti 16 GB:** primary desktop, high-resolution displays, OBS encoding, CUDA, AI, editing, and gaming. The exact replacement model is still being selected because the original MSI Ventus model became unavailable.
- **Secondary display GPU:** auxiliary displays only unless a later workload is deliberately assigned to it. The exact small, low-power model is still being selected.

## Hardware validation before purchase

Use the owned MSI MAG B850 Tomahawk MAX WiFi to confirm:

- which lower slot remains physically accessible with the selected primary GPU;
- the electrical lane allocation of that slot;
- whether any M.2 or port sharing affects the intended configuration;
- whether an optional USB expansion card can coexist;
- whether a slot-mounted anti-sag bracket is needed without obstructing the secondary GPU.

Do not assume Intel Arc A310 or any other specific secondary card is final until this validation is complete.

## Setup checklist

- [ ] Install current AMD chipset drivers.
- [ ] Install the NVIDIA driver from the official source.
- [ ] Install the secondary GPU driver from its official source.
- [ ] Confirm both adapters appear without errors in Device Manager.
- [ ] Connect and identify one display at a time.
- [ ] Set resolution, refresh rate, scaling, orientation, and primary display.
- [ ] Assign performance-sensitive applications to the NVIDIA GPU in Windows graphics settings.
- [ ] Verify OBS uses the NVIDIA encoder.
- [ ] Reboot and confirm the layout persists.
- [ ] Test sleep, wake, driver updates, and mixed refresh rates.

Document exact GPU models and driver versions when a stable configuration is established.
