# Workflow

## 1. Align the assignment

Confirm or infer only what is necessary:

- authoritative contract source and whether the PDF is the source of truth;
- requested delivery periods, products, sections, or other scope;
- whether a pre-extracted workbook exists;
- the comparison group: existing feature inventory, PRD, implementation record, live product, or another named baseline;
- whether live browser verification is requested;
- required outputs and whether external publication is authorized;
- current headers or templates when the target artifact already exists.

If missing information would materially change the result, ask one concise question. Otherwise proceed with a conservative scope and state it.

## 2. Split a large contract when useful

Split only to reduce review load or isolate a meaningful boundary. Record:

- source PDF and split artifact;
- source-page range and split-page range;
- delivery period/batch/section boundary;
- first and last contract item in each split;
- any page shared by adjacent scopes.

Do not split a table row or a continuation across pages into separate capabilities. At every boundary check both the preceding and following page.

## 3. Extract contract capabilities

Extract the smallest contract-deliverable unit supported by the PDF. Preserve the source wording; do not improve grammar, normalize ambiguous terms, or infer omitted parameters. For each item, retain whatever fields are present in the source or required by the user's target format, such as location, module, name, requirement text, quantity, notes, and source page.

Model each requirement internally as:

- object and actor;
- action or lifecycle operation;
- inputs and configurable parameters;
- processing or decision logic;
- output and state change;
- permissions and scope;
- integrations and dependencies;
- exception or boundary conditions.

These are analysis dimensions, not mandatory output columns. Use them to prevent a generic operation from being matched to the wrong object.

## 4. Verify the extracted data twice

### Pass A: structure and pagination

Check page count, row count, scope boundaries, source-page mapping, delivery/batch continuity, repeated headers, merged cells, continuation rows, product/section changes, omissions, duplicates, and row shifts.

### Pass B: visual and content fidelity

Check requirement text, numbers, units, quantities, abbreviations, model names, punctuation, OCR-prone characters, notes, and continuation text against the PDF page image or equivalent primary rendering.

Keep an error log with source location, field, observed value, corrected value, issue type, and evidence. Do not silently patch uncertain text; mark it unresolved.

## 5. Select a comparison mode

### Inventory/specification comparison

Compare the verified contract inventory with the named baseline. Match by object, hierarchy, actor, scope, behavior, and key constraints—not by a generic word such as “list”, “edit”, “delete”, or “search”. Preserve the baseline's actual row/path when reporting a match.

### Live product verification

Start from the user's provided product entry point. Enumerate relevant reachable modules before inspecting a single subpage. Inspect the relevant list, create, detail, state, permission, and exception surfaces. Record observed evidence separately from the contract comparison.

If both modes are requested, produce both conclusions instead of collapsing them.

## 6. Produce the requested output

Use the user's existing headers when supplied. If the target is a risk report, normally include only items with a material contract-to-baseline/product difference, unless the user asks for a full matrix. Keep source page, exact contract wording, actual observation, and reproducible path where the target structure supports them.

Optional complexity, obsolescence, or prioritization analysis must be labeled as analysis rather than contract fact. Define the classification, make categories mutually exclusive if reporting totals, and identify the items included.

## 7. External publication

External publication is optional. Before writing, re-read the target's current version, structure, headers, and effective range. Write only the authorized scope. After writing, re-read the actual result and verify row counts, headers, ordering, key records, and stale-content removal.
