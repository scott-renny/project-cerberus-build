# Wazuh Agent Health and Re-enrollment

**Status:** Planned  
**Owner:** Cerberus Operations  
**Version:** 0.1  
**Last reviewed:** 2026-08-14

## Purpose

Detect and recover a failed Linux Mint Wazuh agent while protecting enrollment access, preserving the permanent asset identity, and avoiding duplicate registrations.

## Health checks

```bash
systemctl status wazuh-agent --no-pager
sudo journalctl -u wazuh-agent --since "1 hour ago" --no-pager
sudo ss -tpn
```

Validate on the manager that the expected Cerberus identity is active and recent events are arriving. Do not publish manager addresses, agent keys, enrollment credentials, or unredacted logs.

## Recovery sequence

1. Confirm system time, DNS, route, firewall state, and manager reachability through the approved network.
2. Review local agent logs and manager-side status.
3. Restart the service only after collecting relevant failure evidence.
4. Verify the configured manager, protocol, port, and certificate expectations without exposing secrets.
5. If the local key or manager record is invalid, approve re-enrollment and revoke the superseded record.
6. Open enrollment access only from the required trusted source and only for the enrollment window.
7. Install the current manager-compatible Linux package from the official Wazuh repository.
8. Enroll with the permanent Cerberus asset identity.
9. Close enrollment access immediately after a valid key is issued.
10. Validate connection, inventory, file-integrity monitoring, configuration assessment, vulnerability visibility, and relevant journal collection.

## Stop conditions

Stop for an unexpected manager identity, certificate failure, duplicate active agent, unknown enrollment request, unauthorized network path, or instructions requiring credentials in shell history or public evidence.

## Validation gate

This runbook remains Planned until a controlled disconnect, service failure, revoked-key re-enrollment, telemetry recovery, and enrollment-port closure are demonstrated.

## Official reference

- [Wazuh Linux agent deployment](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/wazuh-agent-package-linux.html)
