# Proposed data model (synthetic demonstration only)

## Issue record

| Field | Purpose | Validation |
|---|---|---|
| issue_id | Unique issue transaction | Generated, unique |
| borrower_ref | Pseudonymous borrower key | Required; no real student ID in demo |
| book_ref | Library book barcode/reference | Required; item must exist and be available |
| issued_at | Issue timestamp | System-generated |
| due_at | Return deadline | Derived from approved policy; staff can confirm, not freely edit |
| returned_at | Return timestamp | Empty until a staff member records return |
| status | Current transaction state | Enumerated status only |
| actor_role | Role performing action | Must be authorised for that action |
| policy_version | Rule used to calculate due date | Required for traceability |
| exception_code | Reason for manual review/failure | Required when an exception state is used |

## Role permissions

- Borrower: view own due date; request correction or extension.
- Library staff: create issue/return events and view records needed for service.
- Library supervisor: resolve disputes, policy exceptions and correction requests.
- System process: calculate due date, validate fields, send reminders, append audit events; no independent policy override.

## Audit and privacy

Use append-only events for issue, return, due-date correction, notification attempt, failure and supervisor decision. Store the minimum necessary data, restrict access, and use only synthetic data in this repository. Real retention periods and identity verification must follow the institution's approved policy; this report does not invent one.
