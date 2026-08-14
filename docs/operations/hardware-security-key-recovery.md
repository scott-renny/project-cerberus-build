# Hardware Security-Key Recovery

**Status:** Planned  
**Owner:** Cerberus Identity Owner  
**Version:** 0.1  
**Last reviewed:** 2026-08-14

## Purpose

Enroll and recover phishing-resistant authentication on Cerberus without creating a single-key lockout or publishing account-registration details.

## Enrollment baseline

1. Confirm the service supports FIDO2/WebAuthn and review its recovery model.
2. Enroll the assigned primary workstation key.
3. Enroll an approved backup key or independent recovery factor.
4. Name registrations using a private inventory convention.
5. Test sign-in with each factor in a separate browser session.
6. Confirm recovery codes or administrative recovery are stored securely offline.
7. Record only sanitized completion evidence publicly.

## Recovery

1. Verify the requester and affected account through an independent factor.
2. Use the tested backup key or approved service recovery path.
3. Revoke the missing, stolen, or failed key registration.
4. Review recent authentication activity.
5. Enroll and test a replacement key.
6. Rotate related credentials when compromise cannot be excluded.
7. Update the private registration inventory and incident/change record.

## Guardrails

- Never expose PINs, recovery codes, credential IDs, attestation details, account lists, or serial numbers.
- Do not remove the last working factor before its replacement is tested.
- Do not make one portable key the only recovery path for multiple critical accounts.
- Keep workstation, mobile, and administrative-key roles separated where practical.
- Treat a lost key as a security event until account activity and possession risk are assessed.

## Validation gate

This runbook remains Planned until loss of the primary key is simulated and the backup-factor, revocation, replacement, and audit steps succeed.
