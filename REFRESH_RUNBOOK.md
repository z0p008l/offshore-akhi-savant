# Offshore AKHI Savant — Refresh Runbook

## Goal

Keep the shared Buyer Morning Report artifact current, validated, and available to authorized users.

## Required flow

```text
Scheduled trigger
  -> authenticate using approved automation identity
  -> read approved source data
  -> validate source run date and required inputs
  -> generate report payload
  -> validate output schema and metric rules
  -> publish current_report.json
  -> publish optional current_report.csv
  -> publish freshness.json
  -> record success or failure
```

## Fail-closed behavior

The pipeline must not publish a new report when required source data, run dates, budget rows, or validation checks are missing.

On failure:

- Preserve the last known good report when policy allows.
- Mark the refresh status as failed.
- Record the failure timestamp and reason.
- Notify the report owner through the approved support channel.
- Do not replace valid data with an empty or fabricated report.

## `freshness.json` minimum fields

```json
{
  "report_name": "Buyer Morning Report",
  "status": "success",
  "generated_at": "[ISO-8601 TIMESTAMP]",
  "data_through_date": "[YYYY-MM-DD]",
  "source": "[APPROVED SOURCE NAME]",
  "pipeline_version": "[VERSION]",
  "error": null
}
```

For a failed run, use:

```json
{
  "report_name": "Buyer Morning Report",
  "status": "failed",
  "generated_at": "[ISO-8601 TIMESTAMP]",
  "data_through_date": "[LAST KNOWN GOOD DATE]",
  "source": "[APPROVED SOURCE NAME]",
  "pipeline_version": "[VERSION]",
  "error": "[SAFE ERROR SUMMARY]"
}
```

Do not include credentials, tokens, or sensitive stack traces in the shared freshness file.

## Manual verification

After a successful refresh, confirm:

- The report file exists.
- The report is valid JSON.
- Required fields are present.
- Sales and dollar values are whole dollars.
- The data-through date is correct.
- The source and refresh timestamp are present.
- The file can be opened by an authorized test user.
- The agent can retrieve the file through its approved connection.

## Rollback

If a new report is invalid:

1. Stop further publication.
2. Preserve the last known good artifact.
3. Mark the failed run clearly.
4. Notify the report owner.
5. Correct the pipeline.
6. Re-run validation.
7. Republish only after approval.
