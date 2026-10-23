# Task 1 Report: Library Book Issue and Return-Validity Tracking

**Evidence status:** Hypothetical walkthrough; not an observed or confirmed description of ICFAI/IFHE library operations.  
**Prepared:** 23 October 2026.  
**Data:** Synthetic assumptions only; no student names, ID numbers, borrowing records or private messages.

## 1. Executive summary

The scenario describes a manual book-issue process in which library staff check/scan a student's ID card, issue a book, and write a due/validity date on the book. Handwriting is a weak reminder mechanism: a borrower may overlook the date, the date may be unclear, and staff may need to answer due-date questions or reconcile a return. These are plausible risks, not confirmed incident rates.

The proposal is a lightweight mobile-friendly issue register. Staff scan/check the ID and book barcode or enter synthetic identifiers, confirm that the borrower and item are eligible, record the issue timestamp and due date, and give the borrower a due-date view/reminder. Staff retain authority over exceptions. The proposal does not require live integration, a real student database or AI.

## 2. Scope and method

The assignment permits a hypothetical walkthrough if access is unavailable. This report uses that route because no permissioned library walkthrough, staff interview or real transaction sample was supplied. It therefore makes no claim of direct observation. The current process is derived only from the scenario in the assignment request; all other steps are explicit assumptions that a real investigation would verify.

Scope: one ordinary book issue and its return-validity tracking. Out of scope: fines, student records, fee information, procurement, inventory valuation, and integration with a production library system.

## 3. Current-state process and problem statement

### Hypothetical current steps

1. Borrower presents a college ID card and selected book.
2. Staff checks/scans the ID card.
3. Staff checks the book's availability and any borrowing restrictions (assumed step; verify in fieldwork).
4. Staff records or confirms the issue (the exact record mechanism is unknown).
5. Staff writes the return-validity/due date on the book.
6. Borrower leaves with the book and must remember the due date.
7. At return, staff checks the book and records its return (assumed step; verify in fieldwork).

Potential exceptions include an unreadable ID/barcode, an unavailable book, an incomplete record, a disputed due date, a duplicate issue record, or a device/system outage after the book is physically handed over.

### Problem statement

For a hypothetical library using a handwritten due date, the due date is not necessarily visible to the borrower after leaving the counter and can be difficult to search centrally. This can create avoidable due-date queries, transcription errors and rework. The scale is not known without measured transaction counts and handling times.

## 4. Current workflow

See `current-workflow.mmd`. The diagram intentionally marks availability and return-record steps as assumptions, not confirmed local practice.

## 5. Evidence log and scale estimate

See `evidence-log.csv`. The only scenario fact supplied is that the described current process checks/scans the ID card and writes the validity date on the book. No actual monthly volume or handling time is available.

For a transparent planning model, assume **300 issues/month**, **2 minutes** of staff handling per issue in the current process, and **0.5 additional minutes per issue** for average due-date queries/corrections. These values are not measured. They are deliberately replaceable assumptions.

Current monthly staff effort = 300 × (2 + 0.5) = 750 minutes = 12.5 hours/month.

A sensitivity range is useful. If volume is 150–450 issues/month and additional rework averages 0.25–0.75 minutes/issue, using 2 minutes of baseline handling gives 337.5–1,237.5 minutes/month (5.625–20.625 hours). This range is a scenario analysis, not a claim about the actual library.

## 6. Proposed workflow

1. Staff opens the mobile-friendly issue form.
2. Staff checks/scans the ID card using an approved library process; the prototype stores only a synthetic borrower code.
3. Staff scans/enters the book barcode or synthetic book code.
4. The form validates required fields, item availability and borrowing rules configured by the library.
5. The system calculates the due date from an authorised policy table; staff can see it before confirming.
6. Staff confirms issue. The event is saved with a timestamp and staff role; status becomes `ISSUED`.
7. Borrower sees the due date on a phone through a printed/onscreen receipt or a permitted notification channel. If notifications are unavailable, the due date remains visible on the receipt/issue record.
8. At return, staff selects the open issue and records the return; status becomes `RETURNED`.
9. Overdue reminders are informational only. Staff handle disputes, extensions, damaged books and policy exceptions.

The proposed flow is shown in `proposed-workflow.mmd`. It is a design, not a deployed service.

## 7. Inputs, roles, statuses and controls

### Required inputs

- Synthetic borrower reference (real ID data must not be copied into this repository).
- Book barcode/reference.
- Issue date/time generated by the system.
- Due date generated from a policy table and confirmed by staff.
- Staff role/reference for audit attribution (use synthetic values in demonstration data).
- Optional notification preference/contact handled only in an approved real system; do not store real contact details in this assignment.

### Statuses

`DRAFT` → `VALIDATING` → `READY_FOR_ISSUE` → `ISSUED` → `RETURNED`; exception states: `NEEDS_REVIEW`, `REJECTED`, `FAILED`, `OVERDUE` (derived from due date and non-return, not an approval state), `CANCELLED`.

### Approval boundaries and accountability

- **Accountable owner:** Library operations lead (proposed role, not a statement about the actual organisation).
- **Library staff:** may issue/return books only within the approved library rules.
- **Borrower:** may view their own due date and request correction/extension; cannot change the due date or mark a book returned.
- **System:** may validate fields, calculate due dates from a configured policy and send reminders; it must not approve policy exceptions on its own.
- **Authorised supervisor:** decides disputed records, policy exceptions, overrides and unresolved failures.

### Audit record

Record event ID, synthetic borrower code, book code, old/new status, timestamp, action type, staff role, due date, policy version and exception reason. Keep the minimum data necessary and follow the institution's approved retention/access policy. The student prototype must use fake identifiers only.

## 8. Five synthetic test cases

See `test-cases.csv` for preconditions, input, expected outcome, recovery and simulated result. The cases are **design-level simulations**, not executed tests against a live library system.

- Normal issue: valid synthetic borrower and available book; create one `ISSUED` record with a policy-derived due date.
- Missing information: no book code; reject submission with a clear validation message and do not issue.
- Duplicate: same open borrower-book issue is submitted again; flag the duplicate and check the original record before taking action.
- Unauthorized request: borrower attempts to alter the due date or mark a return; deny the action and log it.
- Failed step: notification service fails after issue record is saved; preserve `ISSUED`, record notification failure and provide the due date through the receipt/manual fallback. Never roll back a valid physical issue silently.

## 9. Time-saving model and net savings

The calculation is in `time-savings.csv`. The scenario assumes 300 issues/month. Current effort is 2.5 minutes per issue (2.0 issue handling + 0.5 average rework/query), or 750 minutes/month. Proposed handling is assumed to be 1.5 minutes per issue plus 60 minutes/month of staff review/support, giving 510 minutes/month. Net recurring savings = 750 − 510 = **240 minutes (4 hours) per month**.

Assume a one-time 8-hour setup/training effort. Simple payback = 8 hours ÷ 4 hours/month = **2 months**, assuming the estimated savings persist. This is not a financial return guarantee. If real measurements show lower volume or greater support overhead, the benefit may disappear. Measure at least 20–30 permissioned transactions or a suitable sample before making a real deployment decision.

## 10. Fallback, risk and abandonment criterion

- If the mobile device/network fails, use the institution's approved paper/legacy procedure, record a temporary reference, and reconcile the record when service returns. Never bypass eligibility checks simply because the system is unavailable.
- If notification fails, preserve the issue record and show/print the due date; retry or use an approved alternate channel.
- If a barcode cannot be read, staff manually verifies the book identifier and records the exception.
- If a duplicate or conflicting record appears, stop automated action and ask the authorised staff member to resolve it.
- Risks: incorrect policy configuration, inaccurate identifiers, notification delivery failure, over-collection of personal data, staff training burden, and digital exclusion.
- **Change/abandon criterion:** if a permitted baseline study shows that due-date queries/rework are negligible and the new process adds more than its saved handling/support time, do not deploy the digital flow as designed. Consider a simpler printed due-date receipt instead.

## 11. Where software rules suffice and whether AI adds value

Rules and ordinary software are sufficient for field validation, duplicate detection, due-date calculation, role-based access, reminders and audit logs. AI adds no necessary value to issuing a book or calculating a due date; using AI here could add cost, unpredictability and privacy risk. AI might later help summarise anonymised feedback, but it should not decide borrowing eligibility or override policy.

## 12. Limitations and next steps

This is hypothetical, not a measured case study. No library staff interview, direct observation, real volume count, policy document or technical integration was available. Before treating the proposal as an operational recommendation, seek permission, validate each process step, measure a representative sample, confirm the official borrowing/renewal rules, and obtain the library owner's approval. Respect refusal and do not collect personal records.
