# Verification checklist

## Contract and PDF

- [ ] PDF is identified as authoritative.
- [ ] If split, every split has a source-page mapping.
- [ ] Shared boundary pages were checked from both sides.
- [ ] No continuation row was broken into a new capability.
- [ ] Scope, delivery period, batch, product, and section transitions are correct.
- [ ] Total rows and per-scope rows reconcile.
- [ ] Pass A checked pagination, row shifts, omissions, duplicates, and boundaries.
- [ ] Pass B checked wording, numbers, units, quantities, notes, abbreviations, and OCR-sensitive text.
- [ ] Unclear text is marked unresolved rather than guessed.

## Comparison

- [ ] At least one comparison group is explicitly identified.
- [ ] Contract-to-baseline and product-page conclusions are separate.
- [ ] Matches use object and hierarchy, not generic CRUD words.
- [ ] Parameters, roles, scope, lifecycle, and integrations are compared where specified.
- [ ] “Not found” is not phrased as absolute backend non-support.
- [ ] Page-test incompleteness is not silently converted into contract risk.
- [ ] Any optional complexity/obsolescence totals have a stated, mutually exclusive classification.

## Browser and delegated review

- [ ] Browser review starts from the user's provided top-level entry point.
- [ ] Relevant reachable modules were enumerated before deep inspection.
- [ ] Lists, forms, details, states, permissions, and exceptions were checked as needed.
- [ ] No real task, destructive action, paid action, or secret was submitted without authorization.
- [ ] Delegated results were checked by phase + sequence + module + name before integration.
- [ ] Every delegated item has evidence tied to the correct requirement, not merely valid JSON.

## Deliverables

- [ ] Existing headers and structure were read before writing.
- [ ] No deleted field or old template was restored without instruction.
- [ ] Risk report contains concrete differences and reproducible evidence.
- [ ] Internal agent IDs, secret values, and irrelevant exploration notes are excluded.
- [ ] Local artifacts pass structural checks.
- [ ] External artifacts were read back after writing.
- [ ] Final counts reconcile with the verified item inventory.
