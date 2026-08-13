# Six-Display Plan

The former standalone Project Hydra scope is now the Cerberus Desktop & Workflow Environment.

## Target topology

| Display | Intended role | Planned GPU | Connection |
|---|---|---|---|
| 49-inch ultrawide | Primary engineering workspace | RTX 5060 Ti 16 GB | DisplayPort preferred |
| Left 27-inch | Development/research | RTX 5060 Ti 16 GB | DisplayPort preferred |
| Right 27-inch | COC/communications | RTX 5060 Ti 16 GB | DisplayPort preferred |
| 24-inch portrait | Logs, terminals, documentation | T400 preferred / P620 fallback | Mini DisplayPort adapter |
| 15.6-inch utility 1 | Auxiliary dashboard | T400 preferred / P620 fallback | Verify exact input/adapter |
| 15.6-inch utility 2 | Auxiliary dashboard | T400 preferred / P620 fallback | Verify exact input/adapter |

The final port assignment depends on exact GPU outputs and the recorded inputs, resolutions, refresh rates, orientation, and scaling of every display.

## KDE workflow requirements

- Give every display a stable documented identity.
- Record physical order, coordinates, primary display, scaling, orientation, and refresh.
- Define engineering, cybersecurity, infrastructure, research, and streaming workspaces.
- Prefer KDE-native activities, virtual desktops, shortcuts, and window rules.
- Version-control sanitized configuration and restoration instructions.
- Test layout persistence after reboot, driver/kernel updates, logout/login, and sleep/wake.
- Document a reduced-display recovery mode.
- Avoid publishing screenshots containing private dashboards, addresses, alerts, or credentials.

Portable displays may need separate USB power even when video uses HDMI or Mini HDMI.
