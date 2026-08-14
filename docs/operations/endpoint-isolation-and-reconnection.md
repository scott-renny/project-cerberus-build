# Endpoint Isolation and Reconnection

**Status:** Planned  
**Owner:** COC Incident Lead and Cerberus Operations  
**Version:** 0.1  
**Last reviewed:** 2026-08-14

## Purpose

Isolate Cerberus during suspected compromise without destroying evidence, then reconnect it only after an approved integrity and recovery decision.

## Isolation

1. Open an incident record and preserve the triggering alert.
2. If harmful activity is continuing, isolate at the managed switch or network controller when possible.
3. If local isolation is required and console access is available, disconnect the cable or disable networking deliberately.
4. Do not run a local network-disable command through the only remote administration session.
5. Preserve Wazuh, journal, authentication, process, network, and backup evidence available before isolation.
6. Protect backup destinations and management credentials from the affected host.
7. Record the isolation time, method, operator, and remaining paths such as Bluetooth, Wi-Fi, VPN, or containers.

A local console option, used only after confirming it will not strand required access, is:

```bash
nmcli networking off
```

## Triage and recovery decision

- Treat isolation as containment, not eradication.
- Determine whether the system can be trusted after investigation.
- Rebuild from verified media when integrity cannot be established.
- Rotate credentials and security keys whose use or storage may have been exposed.
- Select recovery data through the approved backup and rebuild runbook.

## Reconnection gate

Before reconnecting, require:

- incident-lead approval;
- malware and persistence disposition;
- current Fedora and application updates;
- SELinux Enforcing and firewalld active;
- reviewed listening services;
- valid Wazuh telemetry;
- backup and representative restore success;
- credential rotation where required;
- documented residual risk.

Reconnect first to the least-privileged approved network segment and monitor closely. Local re-enablement, when approved, is:

```bash
nmcli networking on
```

## Validation gate

This runbook remains Planned until isolation from local and network controls, evidence preservation, and a monitored reconnection are exercised safely.
