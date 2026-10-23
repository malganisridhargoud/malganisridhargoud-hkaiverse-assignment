# HKAIVERSE Round 2 Assessment — Two-Task Submission

**Scope:** Task 1 workflow investigation and Task 2 curriculum audit/redesign.

> **Evidence and integrity note:** Task 1 is explicitly hypothetical and based on the scenario supplied by the author. No claim is made that the library process was observed directly at ICFAI/IFHE. The curriculum transcript is based on a user-supplied photograph of a printed B.Tech CSE curriculum page; the exact official batch/version record remains provisional until the applicable academic regulation is directly verified. Job descriptions are taken from public company career pages and were accessed on 23 October 2026. Synthetic examples are labelled as such.

## 1. Executive summary

This package contains two separate assignments.

- Task 1 models a hypothetical library issue/return-validity workflow and proposes a mobile-friendly digital register with checks, approval boundaries, auditability and reminder logic.
- Task 2 audits a B.Tech CSE curriculum from a photographed source, recommends targeted practical changes, records public job-description evidence, and documents AI-assisted learning checks with verification notes.

The draft is structurally strong and already separates the tasks, captures five synthetic workflow tests, records its assumptions, and discloses the curriculum discrepancy. The main improvements added here are stronger evidence traceability: an official curriculum verification note, a credit reconciliation file, a set of AI exercise transcripts, and a job-evidence record that distinguishes dated public postings from seniority-limited roles.

## 2. Repository structure and navigation

### Root-level files

- [README.md](README.md) — reviewer guide and submission summary
- [AI-USE.md](AI-USE.md) — AI-use declaration and verification policy
- [CONTRIBUTION.md](CONTRIBUTION.md) — personal contribution statement
- [LIMITATIONS.md](LIMITATIONS.md) — final global limitations and unresolved checks

### Sources and evidence

- [sources/source-register.md](sources/source-register.md) — source register and access log
- [sources/official-curriculum-verification.md](sources/official-curriculum-verification.md) — official baseline verification record and provisional status
- [sources/job-description-evidence.md](sources/job-description-evidence.md) — dated public postings and skills evidence

### Task 1: workflow investigation

- [task-1-college-workflow/report.md](task-1-college-workflow/report.md)
- [task-1-college-workflow/current-workflow.mmd](task-1-college-workflow/current-workflow.mmd)
- [task-1-college-workflow/proposed-workflow.mmd](task-1-college-workflow/proposed-workflow.mmd)
- [task-1-college-workflow/evidence-log.csv](task-1-college-workflow/evidence-log.csv)
- [task-1-college-workflow/test-cases.csv](task-1-college-workflow/test-cases.csv)
- [task-1-college-workflow/time-savings.csv](task-1-college-workflow/time-savings.csv)
- [task-1-college-workflow/data-model.md](task-1-college-workflow/data-model.md)
- [task-1-college-workflow/limitations.md](task-1-college-workflow/limitations.md)

### Task 2: curriculum audit and redesign

- [task-2-curriculum-audit/report.md](task-2-curriculum-audit/report.md)
- [task-2-curriculum-audit/course-map.csv](task-2-curriculum-audit/course-map.csv)
- [task-2-curriculum-audit/curriculum-proposal.csv](task-2-curriculum-audit/curriculum-proposal.csv)
- [task-2-curriculum-audit/credit-reconciliation.csv](task-2-curriculum-audit/credit-reconciliation.csv)
- [task-2-curriculum-audit/job-description-comparison.csv](task-2-curriculum-audit/job-description-comparison.csv)
- [task-2-curriculum-audit/ai-verification-log.csv](task-2-curriculum-audit/ai-verification-log.csv)
- [task-2-curriculum-audit/feedback-summary.md](task-2-curriculum-audit/feedback-summary.md)
- [task-2-curriculum-audit/interactive-tool/index.html](task-2-curriculum-audit/interactive-tool/index.html)
- [task-2-curriculum-audit/ai-exercises](task-2-curriculum-audit/ai-exercises) — prompt/output verification notes for five representative AI-assisted subject exercises

## 3. Task 1 — workflow scenario, method and results

Task 1 uses a hypothetical branch-library scenario: a member’s ID is checked and scanned; a due date is written on the book; the return is verified later; and the process is redesigned for mobile-friendly tracking, auditability and reduced manual error.

The report documents:

- the current-state process and its weaknesses,
- a proposed process with explicit state changes and rule checks,
- approval boundaries and fallback logic,
- five synthetic test scenarios,
- a transparent time-savings model with assumptions.

The design emphasises that the workflow does not rely on unauthorised edits and that duplicate or stale issue records are prevented by a constrained state model. The time-savings estimate remains a scenario-based estimate rather than a measured institutional data point.

## 4. Task 2 — curriculum baseline, proposal and evidence

Task 2 begins from a photographed curriculum table for “4.7.6. B.Tech in Computer Science & Engineering.” The course map preserves the visible semester totals and codes, and it explicitly flags the unresolved issues rather than silently correcting them.

Key points:

- The visible semester totals from the photo sum to 162 credits.
- The printed grand total appears to say 163 credits.
- The individual final-year credits for Semesters VII and VIII are not legible in the supplied image.
- The applicable admission-batch regulation and official curriculum URL are not yet confirmed.

The proposal therefore treats the curriculum as a provisional baseline. It recommends targeted updates to assessment depth and practical outcomes rather than radical credit changes, and it keeps the total credit count intended to remain constant while calling out the conditional elective reductions and approval requirements.

## 5. Key calculations and unresolved credit discrepancy

The core issue is not a missing formula; it is an unresolved source mismatch.

- Visible semester totals: 22 + 22 + 23 + 23 + 21 + 21 + 15 + 15 = 162
- Printed grand total on the photograph appears to be 163
- The package does not change the course map to force a match; it preserves the discrepancy and labels it as unresolved

The proposal file [task-2-curriculum-audit/credit-reconciliation.csv](task-2-curriculum-audit/credit-reconciliation.csv) documents the intended balance: most changes are assessment updates, not additional programme credits; two conditional one-credit reductions are only valid when the actual elective and regulation are identified; and a new lab is proposed only within approved elective space or by replacing existing content.

This means the final percentage-affected calculation should be treated as provisional until the official batch-specific curriculum is verified.

## 6. How to run the interactive tool

Open the file below in a browser and test the course filters and credit summary:

- [task-2-curriculum-audit/interactive-tool/index.html](task-2-curriculum-audit/interactive-tool/index.html)

If using a local server is preferred, run the folder from a static file server. The page is a lightweight, local comparison tool and is not a production-grade student information system.

## 7. Evidence classification, privacy and AI-use policy

The package follows a conservative evidence approach:

- Source transcription is clearly separated from official university documents.
- Job postings are used as skills signals, not as proof of entry-level eligibility when the posting clearly requires senior experience.
- Synthetic test inputs are labelled as synthetic.
- No personal or confidential academic data is used.
- AI output is recorded with a verification note, not presented as a live system execution.

The relevant policy records are:

- [AI-USE.md](AI-USE.md)
- [sources/source-register.md](sources/source-register.md)
- [sources/official-curriculum-verification.md](sources/official-curriculum-verification.md)
- [sources/job-description-evidence.md](sources/job-description-evidence.md)

## 8. Personal contribution and limitations

The package acknowledges the following limitations clearly:

- Task 1 is hypothetical and not a measured institutional workflow.
- The course version, regulation, and admission batch are not officially verified yet.
- The degree credit discrepancy remains unresolved in the source image.
- Final-year course-level credits are not legible from the photo.
- Job descriptions are public snapshots and may change.

The relevant files are:

- [CONTRIBUTION.md](CONTRIBUTION.md)
- [LIMITATIONS.md](LIMITATIONS.md)
- [task-1-college-workflow/limitations.md](task-1-college-workflow/limitations.md)
- [task-2-curriculum-audit/feedback-summary.md](task-2-curriculum-audit/feedback-summary.md)

## 9. Sources and access dates

The relevant access log is maintained in:

- [sources/source-register.md](sources/source-register.md)

The source register includes the curriculum photo and the public job pages used for the audit. The package does not claim any private college documents or internal faculty records.

