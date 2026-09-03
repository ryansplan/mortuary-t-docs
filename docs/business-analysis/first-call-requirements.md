# First Call business requirements

## Document purpose

This artifact translates the First Call business need into testable product
requirements. It supports the documented
[Create and share a First Call summary](../getting-started/index.md) workflow and
provides the source requirements for the traceability matrix and UAT package.

This is a sanitized portfolio artifact. It contains no production records,
credentials, proprietary implementation details, or real decedent information.

## Business need

Mortuary and death-care professionals need a consistent way to capture First
Call information, associate it with the correct case, preserve it for compliance
review, and hand off a summary through a device sharing app. The workflow must
distinguish saving a record from delivering a message and must protect case data
when users change cases or roles.

## Business objective

Provide one case-linked First Call workflow that enables an authorized user to:

- Create and identify a case.
- Record available deceased, contact, location, transport, and call information.
- Review and correct the summary before saving it.
- Save the First Call to Compliance.
- Open external sharing options without implying delivery.
- Protect locked First Calls and prevent data from crossing case boundaries.

## Stakeholders and actors

| Stakeholder or actor | Interest or responsibility |
| --- | --- |
| Case Owner | Creates the case, maintains First Call information, and controls final First Call actions. |
| Transporter or collaborator | Contributes permitted case information without receiving owner-only controls. |
| Compliance reviewer | Uses the saved First Call record and status when reviewing the case. |
| Product owner | Defines expected behavior, resolves scope questions, and accepts or rejects the release. |
| UAT tester | Executes business scenarios, records evidence, and verifies corrected defects. |
| Mortuary T | Maintains the active case, form state, document status, and Compliance record. |
| Device sharing app | Receives the First Call summary from Mortuary T for user-directed sending. |

## Scope

### Included

- Starting a new case and generating a Case Ref.
- Capturing the three-step First Call workflow.
- Reviewing and editing the summary.
- Saving the First Call to Compliance.
- Opening and canceling the device sharing options.
- Verifying the resulting First Call and case statuses.
- Enforcing locked-state and role-based restrictions.
- Isolating First Call information by Case Ref.

### Excluded

- Confirming delivery by an external messaging or sharing app.
- Property Inventory and Witness Signature data-entry procedures.
- Compliance checklist completion and PDF export details.
- Dispatch, GPS tracking, routing, fleet management, payroll, and invoicing.

## Assumptions and constraints

- A device sharing app, not Mortuary T, controls recipient selection and message
  delivery.
- First Call information may be incomplete when initially recorded because the
  user records the information available at the time of the call.
- Property Inventory and Witness Signature are independent case activities.
- Public portfolio evidence must use fictional or sanitized information.
- Owner-only restrictions must remain effective even if a restricted action is
  attempted outside the visible interface.

## User stories

| ID | User story |
| --- | --- |
| US-FC-01 | As a Case Owner, I want to record and review the available First Call information so that the case begins with one consistent summary. |
| US-FC-02 | As a Case Owner, I want First Call saved before I open an external sharing app so that canceling or interrupting sharing does not discard the compliance record. |
| US-FC-03 | As a compliance reviewer, I want clear document statuses and case-linked information so that I can identify the record available for review without assuming a message was delivered. |
| US-FC-04 | As a product owner, I want role, locked-state, and case-boundary controls so that users cannot make unauthorized changes or carry information into the wrong case. |

## Requirements

Priority uses the MoSCoW scale: **Must**, **Should**, **Could**, or **Won't** for
this scope.

| ID | Requirement | Priority |
| --- | --- | --- |
| BR-FC-01 | The product must provide a case-linked workflow for recording and preserving First Call information. | Must |
| BR-FC-02 | The product must distinguish saving a First Call record from delivery through an external app. | Must |
| FR-FC-01 | When an authorized user starts a new case, the product must generate a unique Case Ref, identify the user as Case Owner, and set First Call to **Draft**. | Must |
| FR-FC-02 | The product must capture the available deceased, location, contact, identification, date, time-of-death, and case-flag information. | Must |
| FR-FC-03 | The product must capture the available funeral-home, drop-off, transport, crew, special-note, location-code, dispatcher, call-type, call-time, and call-date information. | Must |
| FR-FC-04 | The Case Owner must be able to review the First Call summary and return to the form to correct information before saving. | Must |
| FR-FC-05 | The product must treat the optional recipient entry as compliance-log information and must not use it to select the actual message recipient. | Must |
| FR-FC-06 | When the user continues from the save-and-share confirmation, the product must save First Call to Compliance before opening the device sharing options. | Must |
| FR-FC-07 | Canceling or leaving the device sharing options must not reverse the completed save to Compliance. | Must |
| FR-FC-08 | After the save-and-share handoff, First Call must display **Needs Review**, the case must appear as **Current**, and the saved First Call must be available in Compliance. | Must |
| FR-FC-09 | First Call actions must not change the independent statuses of Property Inventory or Witness Signature. | Must |
| FR-FC-10 | A locked First Call must be read-only. The Case Owner may reopen it; a transporter or collaborator may not perform owner-only close, reopen, or final actions. | Must |
| NFR-FC-01 | First Call form and draft data must remain associated only with the matching Case Ref when the active case changes. | Must |
| NFR-FC-02 | Role and locked-state restrictions must be enforced at both the interface and write-operation boundaries. | Must |
| NFR-FC-03 | User-facing messages must state that Mortuary T hands content to the selected app but does not confirm delivery. | Must |
| NFR-FC-04 | The workflow must remain understandable and operable with supported accessibility settings, including Large Text. | Should |

## Acceptance criteria

| ID | Given | When | Then |
| --- | --- | --- | --- |
| AC-FC-01 | No case is active | The user selects **Start New Case** | A unique Case Ref appears, the user is Case Owner, and First Call is **Draft**. |
| AC-FC-02 | A draft First Call is open | The user completes the deceased-details step | The entered deceased, location, contact, identification, date, time, and flag information remains available for review. |
| AC-FC-03 | Deceased details have been recorded | The user completes the transport-and-call step | The entered transport, crew, location-code, dispatcher, and call information remains available for review. |
| AC-FC-04 | The summary contains incorrect information | The Case Owner selects **Edit First Call** and makes a correction | The corrected information appears on the reviewed summary. |
| AC-FC-05 | A recipient is entered in the optional summary field | The user starts the save-and-share action | The device sharing app still requires the user to choose the actual recipient. |
| AC-FC-06 | The reviewed summary is ready | The user selects **Save & Share First Call Summary** and continues | The First Call is saved to Compliance before the device sharing options open. |
| AC-FC-07 | The device sharing options are open | The user cancels or returns without sending | The saved First Call remains available in Compliance. |
| AC-FC-08 | Mortuary T has handed the summary to the selected app | The user returns to the case workflow | First Call is **Needs Review**, the case is **Current**, and the First Call is available in Compliance. |
| AC-FC-09 | Property Inventory and Witness Signature have existing statuses | The user saves and shares First Call | The two other document statuses do not change. |
| AC-FC-10 | First Call is locked | Any user attempts to change a First Call field | The change is blocked and no autosave or write operation records it. |
| AC-FC-11 | First Call is locked | The Case Owner reopens it | Normal First Call editing becomes available. |
| AC-FC-12 | A transporter or collaborator is viewing the case | The user attempts an owner-only final action | The action is unavailable or rejected. |
| AC-FC-13 | First Call data exists for Case A | The user changes to Case B and opens First Call | Only data associated with Case B appears; no Case A draft value is reused. |
| AC-FC-14 | A supported Large Text setting is enabled | The user completes the First Call workflow | Content and controls remain readable and operable without blocking the workflow. |

## Business rules

- A Mortuary T case includes First Call, Property Inventory, and Witness
  Signature as independently tracked activities.
- First Call begins in **Draft** status.
- **Save & Share First Call Summary** performs an internal save before it opens
  the external sharing options.
- The optional recipient field supports the compliance log only.
- A device-sharing handoff does not prove that a message was delivered.
- A locked First Call is read-only until the Case Owner reopens it.
- Draft or form state is valid only when its Case Ref matches the active case.

## Related artifacts

- [First Call cross-functional workflow](first-call-swimlane.md)
- [First Call requirements traceability](first-call-traceability.md)
- [First Call UAT plan and results](first-call-uat.md)
