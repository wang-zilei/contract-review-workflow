# Judgment rules

## Separate result fields conceptually

Even if the user's table has fewer columns, maintain this separation in reasoning:

- **Contract requirement**: the requirement as stated in the PDF.
- **Baseline coverage**: whether the designated comparison group contains the same capability.
- **Product observation**: what was actually seen or executed.
- **Contract risk**: whether a material requirement difference is established.
- **Open question**: what remains unverified.

“Page not fully tested” is an open question or page-status note. It is not automatically a contract risk.

## Coverage labels

Use labels only when they match the user's requested vocabulary. A useful default is:

- **Covered**: the comparison group or observed product capability matches the contract's object, scope, and key requirements.
- **Partially covered**: a material subset is present, but a named parameter, operation, actor, scope, lifecycle state, or integration is missing or different.
- **Not found**: the designated comparison group or inspected product scope has no credible corresponding capability. Do not claim that the backend never supports it.
- **To confirm**: there is a credible lead, but available evidence cannot establish coverage or difference.

## Risk rules

Mark risk only when one of these is established:

- different business object or user role;
- narrower scope than the contract;
- missing named operation or lifecycle state;
- missing key parameter, quantity, unit, protocol, or boundary;
- different integration or external dependency;
- evidence contradicts the contract requirement;
- no credible corresponding item exists in the designated comparison group.

Do not mark risk solely because:

- a page was not opened deeply enough;
- the page is empty or the test data is unavailable;
- the menu label differs while object, scope, and behavior match;
- a page path differs;
- implementation details are not visible in the UI;
- a feature was not proven by a test that the user did not request.

## Matching rules

A match requires semantic alignment across as many dimensions as the contract specifies:

1. object;
2. module/hierarchy;
3. actor and permissions;
4. action set;
5. inputs and key parameters;
6. outputs/state transitions;
7. scope and quantity;
8. integrations and exceptions.

Generic CRUD words are never sufficient by themselves. A matched row must remain traceable to the baseline location and the contract source location.

## Complexity analysis (optional)

Only perform this when requested. A requirement may be labeled “complex” when it involves multiple steps, state transitions, cross-object relationships, permissions, resource scheduling, monitoring/audit, model processing, or external-system integration. A single create/edit/list action is not complex merely because it has a polished UI.

Report the unit of counting—feature point, module, or requirement—and make categories mutually exclusive before giving totals.

## Obsolescence analysis (optional)

Do not call a requirement obsolete as a fact unless the user supplies that determination or reliable evidence supports it. Use “疑似过时” or “建议确认是否保留” when the judgment is based on low current relevance, duplication, a superseded workflow, or a standalone operation with unclear current value. List the criteria and included items.
