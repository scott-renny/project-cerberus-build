# Maintenance Log

| Date | Change or maintenance | Reason | Verification | Rollback notes |
|---|---|---|---|---|
| TBD | Initial build | Deployment | Validation plan | N/A |

## Routine schedule

- Weekly: verify Wazuh connectivity, backup completion, failed services, storage alerts, and unexpected listening services.
- Monthly: review storage health, representative restore evidence, Fedora package and kernel updates, Flatpak updates, firmware availability, and NVIDIA-driver compatibility.
- Quarterly: inspect dust, filters, fans, temperatures, cable condition, UPS health, recovery media, and offline recovery-material access.
- Before package, kernel, driver, or firmware changes: confirm a current backup, record the current state, review the transaction, and identify the rollback path.
- After every material change: rerun the relevant validation-plan section and update this log.

## Procedures

Use the [Cerberus Operations Runbooks](README.md) for governed update, recovery, monitoring, containment, graphics, and identity procedures. Entries remain Planned until their stated validation gates pass.
