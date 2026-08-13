# Cerberus Validation Test Plan

## Hardware and firmware

| Area | Test | Pass condition | Result |
|---|---|---|---|
| POST | Repeated cold and warm boots | Reliable detection and boot | Pending |
| Memory | Extended test before and after EXPO | Zero errors | Pending |
| CPU | Sustained multicore load | Stable; acceptable temperatures | Pending |
| Cooler | Pump/fan monitoring and sustained load | Correct operation; no leak/noise concern | Pending |
| Primary GPU | Accelerated stress and compute test | Stable; no artifact or reset | Pending |
| Secondary GPU | Display load and power-state test | Stable and correctly detected | Pending |
| Storage | SMART/health and performance test | Healthy; expected range | Pending |
| UPS | Load, USB monitoring, outage simulation | Clean detection and controlled shutdown | Pending |

## Fedora platform

| Area | Test | Pass condition | Result |
|---|---|---|---|
| Boot | Encrypted Fedora boot and login | Reliable and recoverable | Pending |
| Updates | Kernel and package update/reboot | Returns to working desktop | Pending |
| Firmware | fwupd/LVFS discovery where supported | Results documented | Pending |
| NVIDIA | Driver, CUDA, and NVENC checks | Acceleration available | Pending |
| Security | SELinux, firewall, encryption, Secure Boot plan | Required controls active | Pending |
| Recovery | Media and documented rollback | Representative recovery succeeds | Pending |

## Six-display environment

| Area | Test | Pass condition | Result |
|---|---|---|---|
| Detection | All six displays connected | All detected with correct identities | Pending |
| Layout | Resolution, refresh, scale, orientation | Matches documented topology | Pending |
| Persistence | Reboot and logout/login | Layout restored | Pending |
| Power state | Sleep/wake where supported | Displays and devices recover | Pending |
| Mixed workload | Dashboards, terminals, video, development | Stable across both GPUs | Pending |

## Engineering and control node

| Area | Test | Pass condition | Result |
|---|---|---|---|
| Git/Python | Representative repository and environment | Works without global-package pollution | Pending |
| Podman | Rootless container build/run | Successful | Pending |
| Distrobox | Representative alternate userspace | Works and remains removable | Pending |
| Ansible | Check-mode against authorized test target | Expected, documented result | Pending |
| Kubernetes | kubectl/Helm access | Authorized cluster query succeeds | Pending |
| AWS/IaC | Identity/config validation without secrets in repo | Successful | Pending |
| Optional VM | Disposable KVM/QEMU guest, if required | Starts, networks, and removes cleanly | Pending |

## Streaming — final phase

| Area | Test | Pass condition | Result |
|---|---|---|---|
| Capture | PS5/capture-card session | Stable video and audio | Pending |
| OBS/NVENC | Representative stream/recording | No encoder overload or dropped frames | Pending |
| Controls | Selected Stream Deck/community workflow | Required actions work | Pending |
| Combined | Engineering dashboards plus streaming | Stable within thermal and power limits | Pending |

Record tools, versions, duration, ambient temperature, settings, and observations.
