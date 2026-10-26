# Metric definitions and Power BI review checklist

## Questions to settle in the model

| Metric | Required clarification |
| --- | --- |
| Billing | Is this invoiced, recognized, or collected revenue? What is the source grain? |
| Treatment, medication, room cost | Are these mutually exclusive components or overlapping totals? |
| Profit | What is the exact DAX expression, and how does it reconcile to billing and included costs? |
| Patient count | Does the model count rows, encounters, patient IDs, or distinct patient IDs? |
| Payment status share | Is the denominator billed amount or record count? Confirm status/color mapping and filters |
| Insurance coverage | Is this approved coverage, an amount billed to insurers, or a payment received? |

No exact DAX implementation is asserted without inspecting the model.

## Presentation and correctness backlog

1. Reconcile Paid/Pending: the Main screenshot's light-blue Paid segment is 60.79%, while the original narrative calls 60.79% Pending.
2. Reconcile the 2.81M Profit card to billing and the included cost measures. Do not present the original roughly 56% margin as validated until then.
3. Replace “Total Patient” with a precise grain-aware label and confirm distinctness.
4. Document currency, date coverage, source provenance, and refresh requirements.
5. Add readable dates and chronological sorting to the billing chart before describing seasonality.
6. Improve contrast, spelling (“Treatment”), and visual hierarchy in Power BI Desktop.
7. Interpret provider comparisons with encounter counts, case mix, and scope limits.

The PBIX and original screenshot text have not been modified. These tasks require model inspection and rendering in Power BI Desktop.

## Evidence status

Verified: ZIP CRC integrity, nonempty DataModel entry, three populated report sections with 13, 10, and 7 visual containers, and valid chunk CRCs in all three screenshots. Container counts include navigation and decorative elements.

Unverified: DAX evaluation, source refresh, relationship correctness, distinct-patient counts, status amounts, profit definition, currency, source period, and external data provenance. No business outcome or production deployment is claimed.
