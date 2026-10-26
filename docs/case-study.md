# Case study: making healthcare billing evidence reviewable

## Decision context

An operations or finance reviewer needs to understand billing concentration, cost measures, payment categories, and provider workload. The report places high-level cards above department, diagnosis, procedure, and provider breakdowns.

## Approach

Review the overview and provider pages, connect each chart to a business question, then reconcile narrative claims against the visible chart legends and financial cards. This case uses the supplied report artifacts; it does not claim access to a live healthcare system or independently verified source records.

## Findings supported by the screenshots

Cardiology has the highest displayed billing, followed by Orthopedics and General Surgery. X-Ray and CT Scan lead the procedure billing chart. Provider billing and patient-count distributions vary, which suggests investigating volume and case mix before judging performance.

## Quality checks that change the interpretation

The Main chart maps Paid to 60.79% and Pending to 39.21%, while the More Details text reverses those labels. That disagreement must be resolved against the underlying aggregation before a collections strategy is based on it.

The financial cards also need reconciliation: displayed billing of 5M and treatment cost of 3M do not explain a displayed profit of 2.81M. Medication and room costs may overlap with other measures; the available documentation does not settle the calculation. A validated profit margin is therefore not reported here.

The Provider page explicitly labels a visual “Count of Patient ID.” A count is not necessarily a distinct-patient count, and raw volume does not measure clinical quality or productivity without context.

## Recommendations to evaluate

- Reconcile status labels and financial measure definitions with the model owner.
- Add a documented due-date/payment-date analysis before prioritizing overdue collections.
- Compare billing per encounter and case mix when studying provider workload.
- Document cost inclusion rules and patient-count grain before financial or operational decisions.

These are analytical recommendations. No recovered revenue, improved margin, or clinical outcome is claimed.

## Delivery limits

The embedded model and layouts are present and the archive is intact. Interactive behavior, DAX calculations, source refresh, provenance, and the narrative corrections inside the PBIX require a Windows Power BI Desktop review. The original artifacts are retained as the evidence being reviewed.
