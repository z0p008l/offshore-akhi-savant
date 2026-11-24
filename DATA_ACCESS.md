# Offshore AKHI Savant — Data Access Requirements

## Intended design

The report is stored in an approved team-owned SharePoint or OneDrive for Business document library. The agent retrieves it through an approved read-only Microsoft Graph, SharePoint, MCP, API, or equivalent connector.

A local synced folder is not the production source.

## Required access

| Actor | Required access |
|---|---|
| End users | Read access to the approved report location and permission to invoke the agent |
| Report pipeline | Write/replace access to the report output only |
| Report owner | Manage pipeline and report contract |
| Agent connection | Approved read-only retrieval permission |
| Data owner/security owner | Approval of source, audience, and retention |

## Complete before production

- SharePoint site: `[APPROVED SITE URL]`
- Document library: `[LIBRARY NAME]`
- Folder: `[FOLDER PATH]`
- End-user group: `[AD/M365 GROUP]`
- Pipeline identity: `[AUTOMATION IDENTITY]`
- Agent retrieval connection: `[GRAPH/API/MCP NAME]`
- Data classification: `[CLASSIFICATION]`
- Retention requirement: `[RETENTION RULE]`
- Approval ticket: `[TICKET OR REQUEST ID]`

## Access request template

> Please grant the approved end-user group read-only access to the Offshore AKHI Savant Buyer Morning Report folder in the team-owned SharePoint document library. Please grant the scheduled report pipeline identity write access only to the report output folder. The marketplace agent requires an approved read-only Graph/SharePoint/API/MCP retrieval connection. No user should need access to a publisher's local Windows workspace.

## Troubleshooting

### User cannot open the shared file

Check SharePoint permissions, group membership, sign-in state, and whether the user has refreshed access.

### Agent says the file is unavailable

Check the agent's retrieval connection and the exact SharePoint site, library, and folder configuration. Do not add a personal local path as a workaround.

### User can open the file but the agent cannot

The agent connection or tool configuration is incomplete. Direct SharePoint access does not automatically give the agent a retrieval capability.

### User sees stale data

Check `freshness.json`, pipeline status, source run date, and the report's effective data-through date.
