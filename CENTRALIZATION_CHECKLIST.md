# Offshore AKHI Savant — Centralization Checklist

Use this checklist before calling the shared deployment complete.

## SharePoint/M365 setup

- [ ] Team-owned SharePoint site or approved shared OneDrive for Business location selected.
- [ ] Personal OneDrive is not the permanent production owner.
- [ ] End-user read group identified.
- [ ] Pipeline write identity identified.
- [ ] Read-only agent retrieval connection identified.
- [ ] Data owner/security approval recorded.

## Report setup

- [ ] `current_report.json` exists.
- [ ] `freshness.json` exists.
- [ ] Report includes source and effective data-through date.
- [ ] Dollar values are whole dollars.
- [ ] Invalid or incomplete source data fails closed.
- [ ] No credentials or secrets are stored in the shared folder.

## Agent setup

- [ ] Agent no longer references `C:\Users\Z0p008l\...` paths.
- [ ] Agent uses the approved central retrieval connection.
- [ ] Agent reports source and freshness.
- [ ] Agent does not fabricate data when the source is unavailable.
- [ ] Unnecessary shell and file-write tools are removed or restricted.
- [ ] Marketplace version is incremented.

## Testing

- [ ] Publisher test succeeds.
- [ ] Clean-user test succeeds.
- [ ] User without the publisher's local project files succeeds.
- [ ] Unauthorized access is denied.
- [ ] Stale or failed refresh behavior is understood.
- [ ] Rollback procedure is documented.

## Completion test

The deployment is complete only when an approved user can use Offshore AKHI Savant from a machine that does not contain the publisher's local project files and receive a current, sourced, freshness-labeled answer.
