# Collect and manage a Witness Signature

Use this procedure to enter witness details, select the witness type, collect a
signature, and view, replace, or share the collected signature.

Witness Signature is a separate case activity. Its status does not depend on
the First Call or Property Inventory status.

## Before you begin

- Confirm that the applicable case is active.
- Note the **Case Ref** displayed on the **Case Workflow** screen.
- Confirm that the witness is available to review the acknowledgment and sign.
- Gather the witness's name, title or role, and organization or facility.

## Open Witness Signature

1. From **Active Case Workflow**, locate **Witness Signature**.
2. Select **Open Witness Signature**.
3. Confirm that the displayed **Case reference** matches the active case.

## Enter the witness details

1. Enter the **Signer name**.
2. Enter the witness's **Title or role**.
3. Enter the **Organization or facility**.
4. Select the applicable witness type:
   - **Pickup witness**
   - **Release witness**
   - **Receiving witness**
   - **General witness**
5. Review the **Acknowledgment text** that appears for the selected witness
   type.
6. Ask the witness to confirm that the details and acknowledgment are correct.

## Collect the signature

1. Ask the witness to sign inside the signature box.
2. If the signature needs to be redrawn, select **Clear Signature** and collect
   it again.
3. Select **Save Signature**.
4. Verify that the signature summary displays the witness details, signature,
   and collection timestamp.
5. Return to **Case Workflow** and verify that Witness Signature displays
   **Collected**.

!!! important "Treat signatures as sensitive information"
    Collect a signature only for an authorized case and an informed witness.
    Do not add real signatures or unsanitized case exports to the public
    documentation repository.

## View or replace the signature

1. From **Active Case Workflow**, select **View / Replace Witness Signature**.
2. Review the witness details, acknowledgment, signature, and collection time.
3. Select **Replace Signature** when the stored signature or its supporting
   details must be corrected.
4. Enter the current details, collect the replacement signature, and select
   **Save Signature**.
5. Verify that the updated signature and collection timestamp appear.

## Share the signature

1. From the signature summary, select **Share Existing Signature**. You can also
   select **Share Signature** from the case record.
2. In the device sharing options, select the intended app and recipient.
3. Complete the selected app's sending process.
4. Return to Mortuary T and confirm that the collected signature remains
   available.

!!! important "Sharing does not confirm delivery"
    Mortuary T passes the signature to the selected app. It does not confirm
    that the app delivered the signature to the recipient. Verify delivery in
    the selected app when needed.

## Expected result

- The witness details and acknowledgment are tied to the active Case Ref.
- Witness Signature displays a **Collected** status.
- The signature summary displays the current signature and collection time.
- The collected signature is available to view, replace, or share.
- The current collected signature can be included in a generated Case Packet.

## Correct or recover the workflow

- **Witness details are incorrect before saving:** Correct the fields before
  collecting or saving the signature.
- **The signature is unclear before saving:** Select **Clear Signature** and ask
  the witness to sign again.
- **Information is incorrect after saving:** Select **Replace Signature** and
  collect a corrected signature.
- **Sharing is canceled:** Return to the signature summary. The collected
  signature remains saved.
- **Delivery is uncertain:** Check the selected sharing app. Mortuary T records
  the handoff, not delivery to the recipient.

## Related business rules

- A signature belongs to the active case identified by its Case Ref.
- The supported witness types are pickup, release, receiving, and general.
- Saving a signature changes Witness Signature to **Collected**.
- Replacing a signature updates the current signature and collection time.
- Sharing a signature does not change its collected status.
- Witness Signature retains a status independent of First Call and Property
  Inventory.

## Continue the case workflow

After collecting the witness signature, continue by
[reviewing Compliance and exporting case documents](compliance-exports.md).
