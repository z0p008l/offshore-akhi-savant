# offshore-akhi-savant
AI-powered merchandising analyst for Alaska and Hawaii, providing sourced business performance insights and actionable recommendations.
Offshore AKHI Savant
════════════════════════

Offshore AKHI Savant is a buyer-ready Alaska and Hawaii merchandising analytics agent.

Purpose
───────

The agent supports approved analysis across:

• Alaska and Hawaii
• State and store
• Buyer and merchant
• Financial group and SBU
• Department, category, fineline, and item
• Buyer Morning Report time frames
• Digital penetration
• Seasonal and holiday workflows
• Approved modular-category workflows

Centralized data source
───────────────────────

The agent must use approved centralized data sources.

For the Buyer Morning Report, the current approved report artifacts are maintained in the team-owned SharePoint location:

 text ─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
Team AK/HI → Offshore AKHI Savant
───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

Primary files:

• current_report.json
• freshness.json

The agent must not depend on a publisher's personal computer, local Windows path, local OneDrive sync path, or local project workspace.

Freshness
─────────

The agent must report:

• Source
• Refresh timestamp
• Effective data-through date
• Scope
• Known limitations

If the centralized source is unavailable or stale, the agent must explain the problem and must not fabricate results.

Dollar formatting
─────────────────

Sales, budgets, and other dollar values must be represented as whole dollars without cents.

Access
──────

Access is restricted to approved Walmart users and data permissions. Marketplace visibility does not automatically grant access to SharePoint, BigQuery, or other source systems.

Ownership
─────────

• Business owner: Zoe Pangere / Team AK/HI
• Technical owner: [COMPLETE BEFORE PUBLISHING]
• Data owner: [COMPLETE BEFORE PUBLISHING]
• Support channel: [COMPLETE BEFORE PUBLISHING]

Repository contents
───────────────────

• agent/ — agent definition
• docs/ — operating and access documentation
• schemas/ — report output contracts

Live report data is intentionally not stored in this repository.

───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

Step 5: Copy your documentation files
═════════════════════════════════════════

Copy these files from your local folder into the repository’s docs/ folder:

 text ─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
OPERATING_CONTRACT.md
DATA_ACCESS.md
REFRESH_RUNBOOK.md
USER_GUIDE.md
SHAREPOINT_README.md
CENTRALIZATION_CHECKLIST.md
CHANGELOG.md
───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

Before uploading, replace placeholders such as:

 text ─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
[APPROVED SITE URL]
[AD/M365 GROUP]
[APPROVED AUTOMATION IDENTITY]
[NAME OR TEAM]
───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

with real values where known.

Do not put credentials in those files.
