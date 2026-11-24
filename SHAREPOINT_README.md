# Offshore AKHI Savant — Shared Report Home

## Purpose

This folder is the central team location for the current Buyer Morning Report artifacts used by Offshore AKHI Savant.

The agent must read the approved shared report source. It must not depend on a publisher's personal computer, local Windows path, or OneDrive sync folder.

## Recommended location

Use a Walmart-approved SharePoint team site or shared OneDrive for Business document library owned by the team or business unit.

Do not use a personal OneDrive folder as the permanent production owner unless the platform owner explicitly approves that design.

## Files

| File | Purpose |
|---|---|
| `current_report.json` | Current machine-readable report payload for approved agent retrieval |
| `current_report.csv` | Optional tabular export for human review |
| `freshness.json` | Refresh status and effective data-through date |
| `README.md` | Description of the shared report location |
| `OPERATING_CONTRACT.md` | Metric, source, freshness, and limitation rules |
| `DATA_ACCESS.md` | Required permissions and access request information |
| `REFRESH_RUNBOOK.md` | How the scheduled report refresh must work |
| `USER_GUIDE.md` | How end users use and troubleshoot the agent |
| `CHANGELOG.md` | Changes to the shared report contract and deployment |

## Ownership

Complete these fields before production use:

- Business owner: `[NAME OR TEAM]`
- Technical owner: `[NAME OR TEAM]`
- Data owner: `[NAME OR TEAM]`
- SharePoint site: `[APPROVED SITE URL]`
- Document library: `[LIBRARY NAME]`
- Report folder: `[FOLDER PATH]`
- User access group: `[APPROVED AD/M365 GROUP]`
- Pipeline identity: `[APPROVED AUTOMATION IDENTITY]`
- Support channel: `[APPROVED SUPPORT CHANNEL]`

## Security rules

- Keep the location private and access-controlled.
- Grant end users read-only access whenever possible.
- Do not store passwords, tokens, PATs, cookies, service-account keys, or certificates here.
- Do not store raw sensitive extracts unless the data owner explicitly approves them.
- Do not use a local synced path as the agent's source.
- Do not manually edit `current_report.json` to change business results.

## Success condition

A user who does not have the publisher's local project files can use Offshore AKHI Savant and receive a current report with a source, refresh timestamp, effective data-through date, and documented limitations.
