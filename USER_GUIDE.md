# Offshore AKHI Savant — User Guide

## What this agent does

Offshore AKHI Savant answers approved Alaska and Hawaii merchandising questions using the centralized Buyer Morning Report and other approved sources.

## Before using it

You must:

1. Be in the approved user group.
2. Have access to the shared report source.
3. Install the current marketplace version.
4. Restart Code Puppy after installation or update.
5. Start a new session after an agent update.

## Example questions

```text
Give me the current AK/HI Buyer Morning Report summary.
```

```text
Compare Alaska and Hawaii WTD sales and units, including the data-through date and source.
```

```text
Show the available MTD performance by SBU and explain any source limitations.
```

```text
Which report source supports this answer, and how fresh is it?
```

## What a good answer includes

A good answer includes:

- Executive summary
- Metrics
- Time frame and scope
- Source
- Effective data-through date
- Refresh timestamp when available
- Limitations

## If it does not work

### The agent is missing

Restart Code Puppy and confirm that the latest marketplace version is installed.

### The agent starts but cannot retrieve the report

Confirm that you can open the shared report directly and that you are in the approved access group. If direct access works, report the issue as an agent retrieval-connection problem.

### The report is stale

Check `freshness.json` and report the data-through date to the report owner.

### The agent asks for a local Windows path

That is a deployment defect. Do not copy files into a personal path as the permanent fix. Report the defect to the technical owner.

### The agent gives an unsupported answer

Ask it to identify the source, data-through date, and limitation. Save the response and send it to the support channel.

## Support information

- Business owner: `[NAME OR TEAM]`
- Technical owner: `[NAME OR TEAM]`
- Support channel: `[APPROVED SUPPORT CHANNEL]`
- Current marketplace version: `[VERSION]`
