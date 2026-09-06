---
name: contract-review-workflow
description: Review contract PDFs, extract and verify required capabilities, compare them with a designated baseline or live product evidence, and produce an evidence-based risk report. Use when a user asks to audit contract deliverables, validate PDF-derived feature lists, or assess contract-to-product coverage.
---

# Contract Review Workflow

Use this skill for contract-function auditing. Keep three conclusions separate throughout the task:

1. **Contract extraction** — what the authoritative contract actually requires.
2. **Baseline comparison** — whether those requirements are covered by the user-designated comparison group, such as an existing feature list, specification, or product capability inventory.
3. **Product verification** — what can be observed in a live product, browser, API, test environment, or other evidence source.

Do not let an incomplete product walkthrough overwrite a baseline comparison that is already supported by matching contract text. Conversely, do not treat a similar name, menu, or card as proof that a contract requirement is covered.

## Default rules

- Treat the PDF as authoritative for contract wording. A pre-existing spreadsheet is an extraction result to verify, not a higher-priority source.
- If the PDF is large, split it by a meaningful contract dimension—delivery period, batch, section, product, or another documented boundary—before detailed review. Preserve the mapping back to the source PDF.
- Run at least two independent verification passes on PDF-derived data: a structural/page-boundary pass and a visual/content pass. For high-risk or ambiguous items, repeat the relevant pass or use an independent reviewer.
- Require at least one explicit comparison group before declaring coverage or risk. If no comparison group is provided, ask for one or limit the output to a verified contract inventory.
- Treat feature extraction, baseline comparison, and live product walkthrough as separate optional stages. Do not perform or report a stage the user did not request.
- Use the user's current output headers and structure. Do not restore deleted columns, add convenient fields, or impose a remembered template.
- Do not claim completion from a successful write response alone. Read back the actual artifact and verify its content and structure.
- Keep facts, judgments, and unresolved questions distinct. Never turn an unverified assumption into a product capability or a contract risk.

## Optional stages

Choose only the stages needed for the request:

- PDF splitting and source mapping
- Contract capability extraction
- Two-pass extraction verification
- Target-scope filtering
- Comparison with an existing inventory or specification
- Live product/browser verification
- Complexity or obsolescence analysis
- Local workbook/report generation
- External document or spreadsheet publication

For detailed procedures, read the relevant references:

- [workflow.md](references/workflow.md) for the end-to-end workflow and stage selection.
- [judgment-rules.md](references/judgment-rules.md) for comparison, risk, evidence, complexity, and obsolescence rules.
- [verification-checklist.md](references/verification-checklist.md) for PDF, spreadsheet, browser, and delegated-review checks.
- [external-write.md](references/external-write.md) before changing a cloud document or spreadsheet.

## Safe operating boundary

Prefer read-only inspection. When using a browser, inspect menus, lists, forms, details, states, and error messages without submitting destructive or costly actions. Do not enter secrets into artifacts. Before an external write, obtain the required authorization and re-read the current target.
