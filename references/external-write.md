# External document and spreadsheet writes

Use this reference only when the user requests publication or modification of an external document or spreadsheet.

## Before writing

1. Read the current target with the appropriate connector or CLI.
2. Record the current revision/version, document block structure, workbook/sheet IDs, effective data range, headers, and relevant formatting/merges.
3. Confirm whether the user wants append, replacement, or a bounded edit.
4. Preserve the target's current headers. Do not restore fields deleted by the user or add fields merely because they would help analysis.
5. Prepare a local payload and, for structural changes, a dry run or equivalent preview.

## During writing

- Write only the authorized range or block.
- Avoid whole-document overwrite when a bounded edit is sufficient.
- Avoid whole-sheet clearing. If stale content must be removed, target only the confirmed stale range.
- Refresh block IDs after structural document changes.
- Keep secrets out of payloads and logs.

## After writing

Read the target again and check:

- title and revision;
- current headers and column count;
- effective range and row count;
- ordering and key rows;
- risk totals and source-page references;
- absence of stale or duplicated content;
- requested formatting and no unrequested formatting changes.

A successful API response is only evidence that the request was accepted; it is not proof that the intended content is present.
