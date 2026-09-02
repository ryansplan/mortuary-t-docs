# First Call UAT plan and results

## Document purpose

This artifact demonstrates a completed, sanitized user acceptance testing cycle
for the First Call workflow. It converts the approved acceptance criteria into
repeatable business scenarios, records results, and documents one defect through
retest and release disposition.

The public record omits real case information, device identifiers, credentials,
and internal environment details. Fictional test data is used throughout.

## Test objective

Confirm that an authorized user can create, complete, review, save, and share a
First Call summary while Mortuary T preserves the correct case association,
document statuses, access rules, and meaning of the external sharing handoff.

## Roles and responsibilities

| Role | Responsibility |
| --- | --- |
| Product owner | Approves requirements, evaluates defects, and makes the release decision. |
| UAT tester | Executes each scenario from the user's perspective and records evidence. |
| Developer | Investigates failed scenarios, implements corrections, and identifies regression risk. |
| Technical writer or business analyst | Maintains requirements, test scenarios, traceability, and user documentation. |

## Test scope

### Included

- New-case initialization.
- Three-step First Call data entry.
- Summary review and correction.
- Save to Compliance and handoff to a device sharing app.
- Canceled-sharing recovery.
- Independent document statuses.
- Locked-state and role restrictions.
- Cross-case data isolation.
- Large Text usability.

### Excluded

- Delivery confirmation inside third-party apps.
- Detailed Property Inventory, Witness Signature, or PDF export testing.
- Performance, penetration, and load testing.
- Production data validation.

## Test conditions

| Item | Test condition |
| --- | --- |
| Test cycle | Sanitized portfolio reconstruction of a completed First Call UAT cycle |
| Product reference | Mortuary T First Call workflow; corrected data-isolation behavior released in version 7.3.6 |
| User roles | Case Owner and transporter or collaborator |
| Platforms | Representative supported iOS and Android devices |
| Accessibility condition | Large Text enabled for the accessibility scenario |
| Test cases | Fictional Case A and Case B with distinct names, dates, locations, and transport details |
| Evidence retained | Scenario outcomes, status observations, defect record, and retest result |

## Entry criteria

- Business requirements and acceptance criteria are approved for the test cycle.
- The test build is available on representative supported devices.
- Fictional test data is prepared for two distinguishable cases.
- The Case Owner and transporter or collaborator roles are available.
- Compliance and device sharing options are available for testing.

## Exit criteria

- Every **Must** requirement has a linked UAT result.
- No critical or high-severity defect remains open.
- Corrected defects pass targeted retest and related regression checks.
- User documentation reflects the accepted behavior.
- The product owner records a release recommendation.

## UAT scenarios and results

| ID | Scenario and principal steps | Expected result | Actual result | Status |
| --- | --- | --- | --- | --- |
| UAT-FC-01 | With no active case, select **Start New Case**. | A unique Case Ref appears; the user is Case Owner; First Call is **Draft**. | All three identifiers and statuses appeared as expected. | Pass |
| UAT-FC-02 | Open First Call; enter distinct Case A details across the deceased and transport-and-call steps; continue to Step 3. | Every entered value is associated with Case A and appears on the summary. | The summary displayed the Case A values entered in both steps. | Pass |
| UAT-FC-03 | From the summary, select **Edit First Call**; correct one field; return to the summary. | The corrected value replaces the prior value. | The revised value appeared and unrelated values remained unchanged. | Pass |
| UAT-FC-04 | Enter an optional compliance-log recipient; select **Save & Share First Call Summary**; continue; choose a sharing app; return to Mortuary T. | First Call is saved before sharing opens; the app requires recipient selection; First Call is **Needs Review**; the case is **Current** and available in Compliance. | The save, external recipient selection, statuses, and Compliance record matched the expected result. | Pass |
| UAT-FC-05 | Repeat the save-and-share action and cancel from the device sharing options. | The First Call remains saved in Compliance and no delivery confirmation is claimed. | The Compliance record remained available; Mortuary T reported only the sharing handoff state. | Pass |
| UAT-FC-06 | Note the Property Inventory and Witness Signature statuses; save and share First Call. | The two independent document statuses do not change. | Both statuses remained unchanged. | Pass |
| UAT-FC-07 | Lock First Call as Case Owner; attempt to edit location, date or time, Plus Code, a case flag, and other form values. | Every edit is blocked and no blocked action triggers an autosave or write. | Fields and actions remained read-only; no blocked change was retained. | Pass |
| UAT-FC-08 | While First Call is locked, reopen it as Case Owner and edit a field. | Normal editing is restored and the authorized change is saved. | Editing resumed and the authorized change appeared on review. | Pass |
| UAT-FC-09 | Access the same workflow as transporter or collaborator; attempt close, reopen, and final First Call actions. | Owner-only actions are unavailable or rejected. | Restricted actions could not be completed. | Pass |
| UAT-FC-10 | Enter an unsaved draft for Case A; change to distinct Case B; open First Call; then return to Case A. | Case B never displays Case A values; returning to Case A restores only valid Case A state. | Initial cycle failed; corrected build passed the targeted retest and Case A regression check. | Pass after retest |
| UAT-FC-11 | Enable Large Text and complete the First Call workflow through summary review and save-and-share confirmation. | Text and controls remain readable and operable without preventing completion. | The workflow remained readable and operable through the handoff. | Pass |

## Defect and retest record

### DEF-FC-001: Prior-case draft appears in another case

| Field | Record |
| --- | --- |
| Linked requirement | NFR-FC-01 |
| Linked scenario | UAT-FC-10 |
| Severity and priority | High severity; high priority |
| Initial status | Failed |
| Final status | Closed after successful retest |
| Affected release | Behavior corrected in Mortuary T 7.3.6 |

**Precondition:** Case A contains a First Call draft with fictional, easily
recognized values. Case B is a different new or shared case.

**Steps to reproduce:**

1. Open Case A and enter First Call draft information.
2. Leave First Call without completing the workflow.
3. Start or join Case B.
4. Open First Call for Case B.

**Expected result:** Only information associated with Case B appears.

**Observed result before correction:** Under a new-case collaboration sequence,
draft values associated with Case A could appear when First Call opened for Case
B.

**Business impact:** A user could rely on information belonging to the wrong
case. This created an unacceptable data-integrity and privacy risk.

**Resolution summary:** First Call state is cleared when the active case
changes. A stored draft is loaded only when its Case Ref matches the active
case, and the current case snapshot remains authoritative.

**Retest result:** Pass. Case B opened without Case A values. Returning to Case
A restored only the valid Case A state. The normal save-to-Compliance workflow
also passed regression testing.

## Test summary

| Measure | Result |
| --- | --- |
| Scenarios executed | 11 |
| Passed on initial execution | 10 |
| Failed on initial execution | 1 |
| Passed after correction and retest | 1 |
| Critical or high-severity defects open | 0 |
| Final UAT outcome | Pass |

## Release recommendation

**Accept for release within the tested scope.** All in-scope **Must**
requirements have passing UAT coverage, DEF-FC-001 passed targeted retest, and
no critical or high-severity defect remains open. External-app delivery remains
outside Mortuary T's verification boundary and should continue to be described
as a handoff rather than a confirmed delivery.

## Related artifacts

- [First Call business requirements](first-call-requirements.md)
- [First Call requirements traceability](first-call-traceability.md)
- [Create and share a First Call summary](../getting-started/index.md)
