# First Call requirements traceability

## Purpose

This matrix connects the First Call business requirements to acceptance
criteria, published user guidance, UAT coverage, and recorded outcomes. It lets
a reviewer follow the workflow from business need through release evidence.

See [First Call business requirements](first-call-requirements.md) for the full
requirement and acceptance-criteria statements.

## Status definitions

| Status | Meaning |
| --- | --- |
| Covered | A requirement has acceptance criteria, documentation, and at least one UAT scenario. |
| Pass | The linked UAT scenario met its expected result in the sanitized test cycle. |
| Pass after retest | The initial result exposed a defect and the corrected behavior passed retest. |

## Traceability matrix

| Requirement | User story | Acceptance criteria | Documentation evidence | UAT coverage | Result |
| --- | --- | --- | --- | --- | --- |
| BR-FC-01 | US-FC-01, US-FC-03 | AC-FC-01 through AC-FC-09 | [Create and share a First Call summary](../getting-started/index.md) | UAT-FC-01 through UAT-FC-06 | Pass |
| BR-FC-02 | US-FC-02, US-FC-03 | AC-FC-05 through AC-FC-08 | [Save and share the summary](../getting-started/index.md#save-and-share-the-summary) | UAT-FC-04, UAT-FC-05 | Pass |
| FR-FC-01 | US-FC-01 | AC-FC-01 | [Create the case](../getting-started/index.md#create-the-case) | UAT-FC-01 | Pass |
| FR-FC-02 | US-FC-01 | AC-FC-02 | [Record the deceased's details](../getting-started/index.md#record-the-deceaseds-details) | UAT-FC-02 | Pass |
| FR-FC-03 | US-FC-01 | AC-FC-03 | [Record transport and call details](../getting-started/index.md#record-transport-and-call-details) | UAT-FC-02 | Pass |
| FR-FC-04 | US-FC-01 | AC-FC-04 | [Review the First Call summary](../getting-started/index.md#review-the-first-call-summary) | UAT-FC-03 | Pass |
| FR-FC-05 | US-FC-02, US-FC-03 | AC-FC-05 | [Review the First Call summary](../getting-started/index.md#review-the-first-call-summary) | UAT-FC-04 | Pass |
| FR-FC-06 | US-FC-02 | AC-FC-06 | [Save and share the summary](../getting-started/index.md#save-and-share-the-summary) | UAT-FC-04 | Pass |
| FR-FC-07 | US-FC-02 | AC-FC-07 | [Correct or recover the workflow](../getting-started/index.md#correct-or-recover-the-workflow) | UAT-FC-05 | Pass |
| FR-FC-08 | US-FC-02, US-FC-03 | AC-FC-08 | [Verify the result](../getting-started/index.md#verify-the-result) | UAT-FC-04 | Pass |
| FR-FC-09 | US-FC-03 | AC-FC-09 | [Expected result](../getting-started/index.md#expected-result) | UAT-FC-06 | Pass |
| FR-FC-10 | US-FC-04 | AC-FC-10 through AC-FC-12 | [Related business rules](../getting-started/index.md#related-business-rules) | UAT-FC-07 through UAT-FC-09 | Pass |
| NFR-FC-01 | US-FC-04 | AC-FC-13 | [Before you begin](../getting-started/index.md#before-you-begin) | UAT-FC-10; DEF-FC-001 | Pass after retest |
| NFR-FC-02 | US-FC-04 | AC-FC-10 through AC-FC-12 | [First Call business rules](first-call-requirements.md#business-rules) | UAT-FC-07 through UAT-FC-09 | Pass |
| NFR-FC-03 | US-FC-02, US-FC-03 | AC-FC-05 through AC-FC-08 | [Sharing and delivery are different events](../getting-started/index.md#save-and-share-the-summary) | UAT-FC-04, UAT-FC-05 | Pass |
| NFR-FC-04 | US-FC-01 | AC-FC-14 | [First Call UAT plan and results](first-call-uat.md) | UAT-FC-11 | Pass |

## Coverage summary

| Measure | Result |
| --- | --- |
| Requirements in scope | 16 |
| Requirements with acceptance criteria | 16 of 16 |
| Requirements with UAT coverage | 16 of 16 |
| UAT scenarios passed | 11 of 11 |
| Defects remaining open | 0 |

All in-scope requirements are covered. One data-isolation scenario initially
failed, was corrected, and passed retest. See
[DEF-FC-001](first-call-uat.md#def-fc-001-prior-case-draft-appears-in-another-case)
for the sanitized defect record.

## Change-impact use

When First Call behavior changes, update this matrix before release:

1. Identify each affected requirement and acceptance criterion.
2. Revise the linked user documentation.
3. Add or update the applicable UAT scenario.
4. Record the new outcome and any defect or retest evidence.
5. Recalculate the coverage summary and release recommendation.
