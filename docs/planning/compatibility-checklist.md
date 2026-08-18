# Compatibility Checklist

## Owned foundation

- [x] MUSETEX K2 owned and arrived.
- [x] MSI MAG B850 Tomahawk MAX WiFi owned and arrived.
- [ ] Inspect both components and retain hardware, accessories, packaging, and documentation.
- [ ] Add sanitized arrival photos without serial numbers, labels, addresses, or account details.

## Case and cooling

- [ ] MSI MAG CORELIQUID A15 360 radiator, fans, tubes, pump cable, and headers fit the selected layout.
- [ ] Cooler does not obstruct memory or the primary PCIe slot.
- [ ] Exact RTX 5060 Ti 16 GB dimensions fit.
- [ ] Compact secondary NVIDIA GPU fits and preserves airflow.
- [ ] Bottom intake is not blocked.
- [ ] Slot-mounted anti-sag support, if needed, does not obstruct the lower GPU.

## Motherboard, PCIe, and storage

- [ ] Current BIOS supports the Ryzen 9 9900X.
- [ ] M-FLASH and Flash BIOS recovery procedures documented.
- [ ] Primary GPU assigned to the CPU-connected primary slot.
- [ ] Lower slot supplies acceptable bandwidth for the secondary display GPU.
- [ ] M2_3 sharing behavior verified; leave it unused if required.
- [ ] Primary Linux Mint SSD assigned to a non-conflicting M.2 slot.
- [ ] Optional USB expansion can coexist with both GPUs.
- [ ] Front-panel USB/audio, pump, fan, ARGB, and power headers mapped.

## Linux Mint and peripherals

- [ ] Exact primary and secondary GPUs supported by the selected NVIDIA driver.
- [ ] Secure Boot approach compatible with NVIDIA modules.
- [ ] Capture card supports Linux/UVC and required resolution/frame rate.
- [ ] Stream Deck workflow has an acceptable Linux solution.
- [ ] AIO, fans, sensors, and RGB have acceptable firmware/Linux control or safe firmware defaults.
- [ ] Audio interface, microphone, webcam, Bluetooth, and other required devices have Linux support.
- [ ] Sleep/wake expectations documented for the final hardware.

## Power

- [ ] RM850e meets final GPU requirements and has every connector.
- [ ] Use only supplied or explicitly compatible modular cables.
- [ ] Sustained and transient estimates leave reasonable headroom.
- [ ] PSU dimensions and cable routing fit.
- [ ] CP1500PFCLCD load, USB monitoring, shutdown integration, and target runtime verified.
- [ ] High-draw devices such as printers remain off battery-backed outlets.

## Six displays

- [ ] Model, resolution, refresh, scale, orientation, input, and power recorded for each display.
- [ ] Exact GPU outputs support all six.
- [ ] Mini DisplayPort and other required adapters are active/passive as appropriate.
- [ ] Cable standards and lengths documented.
- [ ] Portable-monitor power documented.
- [ ] Cinnamon mixed-scale and mixed-refresh behavior validated.
