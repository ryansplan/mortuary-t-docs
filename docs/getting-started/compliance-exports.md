# Review Compliance and export case documents

Use this procedure to review case-document statuses, complete the compliance
checklist, and generate the Due Diligence Report and Case Packet.

Each export is a snapshot of the case at the time it is generated. Regenerate
an export after changing a document or compliance status.

## Before you begin

- Confirm that the applicable case is active.
- Note the **Case Ref** and **Compliance ID**.
- Save First Call to Compliance.
- Send Property Inventory to Compliance if its details must appear in the Case
  Packet.
- Collect the Witness Signature if it must appear in the Case Packet.

## Open the compliance case

1. From **Active Case Workflow**, select **View in Compliance**. You can also
   open **Compliance** from the Case Workflow screen.
2. Select the applicable case.
3. Confirm that the displayed **Case Ref** and **Compliance ID** match the case
   you intend to review.

## Review case-document statuses

1. Under **Case Documents**, review the status of **First Call**.
2. Review the status of **Property Inventory**.
3. Review the status of **Witness Signature**.
4. Open any document that needs attention before generating the exports.
5. If Property Inventory displays **Started**, select **Send to Compliance** to
   save its current snapshot and change its status to **Sent**.

!!! note "Exports preserve the current statuses"
    A Case Packet can identify First Call as **Needs Review**, Property
    Inventory as **Sent**, and Witness Signature as **Collected**. Generating an
    export does not change those workflow statuses.

## Complete the compliance checklist

1. Review the medical-certification and registration due-time indicators.
2. Turn on **Medical certification complete** after the requirement is
   satisfied.
3. Turn on **Death registered** after registration is complete.
4. Turn on **Disposition permit obtained** after the permit is available.
5. Verify that each completed item records a completion time.

The **Death registered** checklist item appears as **Registration** in the
generated reports.

## Generate the Due Diligence Report

1. Review the document statuses, checklist, and outreach attempts.
2. Select **Generate Due Diligence Report**.
3. Review the generated PDF.
4. Confirm that the report includes:
   - Case identification and decedent context
   - First Call, Property Inventory, and Witness Signature statuses
   - Case Packet inclusion indicators
   - Compliance-item completion and due times
   - Outreach attempts
5. Save or share the PDF using the device options.

## Generate the Case Packet

1. Confirm that every document intended for the packet has the expected
   status.
2. Select **Generate Case Packet**.
3. Review the generated PDF.
4. Confirm that the packet includes the applicable sections:
   - Cover and case summary
   - Case-document status summary
   - Due Diligence Summary and outreach log
   - First Call details
   - Property Inventory details when its status is **Sent**
   - Witness Signature details and signature when its status is **Collected**
   - Export metadata
5. Save or share the PDF using the device options.

!!! warning "Protect exported case information"
    Compliance exports can contain personal details, a handwritten signature,
    case identifiers, and device metadata. Share them only with authorized
    recipients. Do not commit real exports to the public documentation
    repository.

## Expected result

- The compliance case displays the current status of each case document.
- Completed checklist items include recorded completion times.
- The Due Diligence Report summarizes document, compliance, and outreach
  status.
- The Case Packet contains the applicable case documents and export metadata.
- Each generated PDF reflects the case state at its generation time.

## Correct or recover the workflow

- **Property Inventory is missing from the packet:** Return to the compliance
  case, select **Send to Compliance**, and regenerate the Case Packet.
- **Witness Signature is missing from the packet:** Collect the signature and
  regenerate the Case Packet.
- **A checklist item is incorrect:** Correct the item in Compliance and
  regenerate both exports.
- **A document status needs attention:** Open the document from **Case
  Documents**, complete the applicable action, and regenerate the exports.
- **An export is outdated:** Generate a new PDF after the case changes.
- **PDF sharing or delivery is uncertain:** Check the selected sharing app and
  the saved file location.

## Related business rules

- Generating an export does not change First Call, Property Inventory, or
  Witness Signature status.
- The Due Diligence Report is a status-focused summary of the case documents,
  compliance items, and outreach attempts.
- The Case Packet combines the available case summary, document details, due
  diligence information, signature, and export metadata.
- Property Inventory must be **Sent** for its current snapshot to be included
  in the Case Packet.
- A collected Witness Signature can be included in the Case Packet.
- Exported PDFs contain the state recorded when they were generated and do not
  update automatically.
  