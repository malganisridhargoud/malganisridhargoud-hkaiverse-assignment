# Task 2 Report: B.Tech CSE Curriculum Audit and Redesign

**Prepared:** 23 October 2026  
**Programme shown in source image:** B.Tech in Computer Science & Engineering  
**Campus/admission batch/version:** Not visible in the supplied photograph; exact applicability to the author's batch is unverified.  
**Source basis:** User-provided photograph of the printed curriculum table; job-description links from official company career pages. This is a student proposal, not an official ICFAI syllabus revision.

## 1. Executive summary

The photographed curriculum covers programming, mathematics, engineering foundations, data structures, algorithms, web technologies, databases, data science, machine learning, operating systems, networks, cloud computing, cryptography, software engineering, a special project, internship/research, thesis/seminar, electives and power skills. This is a broad foundation. The redesign therefore prioritises **assessment and practical-depth updates** over declaring existing subjects obsolete.

The main proposed improvement is to make end-to-end engineering outcomes explicit in existing courses: tested APIs, secure role boundaries, SQL/data validation, CI practices, cloud deployment/monitoring, AI-output verification and measurable capstone outcomes. A proposed workflow-engineering lab connects the library-book scenario from Task 1 to databases, web development, testing, access control and auditability.

### Credit baseline discrepancy and verification status

Visible semester totals are I=22, II=22, III=23, IV=23, V=21, VI=21, VII=15, VIII=15. These add to **162 credits**, while the printed grand total in the photograph appears to say **163**. This report does not silently reconcile the discrepancy. The official curriculum version and exact semester VII/VIII course-level credit allocation must be confirmed before final credit approval.

The assessment package therefore uses a **provisional curriculum baseline** until the relevant official syllabus/regulation is verified. The supporting record is in [../sources/official-curriculum-verification.md](../sources/official-curriculum-verification.md), and the reconciliation file is [credit-reconciliation.csv](credit-reconciliation.csv). The proposal targets approximately **36 credits of course/assessment scope affected** (about 22.1% of 163 or 22.2% of 162), not 36 additional credits. The overall programme credit total is intended to remain unchanged. Affected-credit counting must be validated against the official course-level structure because the image does not expose all final-year allocations.

## 2. Baseline course map

See `course-map.csv` for all visible courses, codes, semester assignments, credits and transcription notes. Course credits for Semesters I–VI are copied from the visible table. Semester VII/VIII show a bundled total of 15 credits each, but the individual credits for internship/research, thesis/seminar, electives and Digital Humanities Elective are not legible. The file therefore leaves these individual credits blank rather than inventing allocations.

### Visible semester totals

| Semester | Printed credits | Main content visible in photograph |
|---|---:|---|
| I | 22 | Mathematics, English, digital fabrication, physics, chemistry, programming, traditional knowledge audit |
| II | 22 | Higher calculus, communication, electronics, DS/AI introduction, environmental sciences, data structures, engineering graphics |
| III | 23 | IoT, OOP, probability/statistics, theory of computation, algorithms, economics/management, discrete mathematics, power skills |
| IV | 23 | Signal processing, computer architecture, digital humanities elective, web technologies, Python/R coding practice, data science, DBMS, power skills |
| V | 21 | Cryptography, OS, compiler construction, ML, software engineering, core elective, power skills |
| VI | 21 | Computer vision, networks, big data, cloud, core elective, special project, power skills |
| VII | 15 | Internship/research, thesis/seminar, electives/professional discipline, digital humanities elective; individual credits unclear |
| VIII | 15 | Same categories visible; individual credits unclear |

## 3. Job-description evidence

Four official career pages were accessed on 23 October 2026 and are recorded in `job-description-comparison.csv`:

1. Wipro AI Engineer L1, posting start date shown as 12 October 2026: computer vision and machine-learning development.
2. Wipro Fullstack developer, posting start date shown as 15 October 2026: React/TypeScript, Python APIs, role-based access, accessibility, and API integration. The page content describes a lead/6+ years role, so it is used only as a skill signal, not a claim about fresher eligibility.
3. Caterpillar Software Engineer — Performance Engineering, posting dates shown as 9–15 October 2026: performance testing, profiling, monitoring, SQL and programming.
4. Hexagon Capability Hub India Software Engineer (Functional Testing): test design, integration/regression, AI-assisted test generation, APIs and SQL; the result does not clearly show a posting date.

Job postings change. Dates and requirements are recorded as displayed in the pages/results at access time. Experience-level mismatch matters: senior roles reveal skill expectations but cannot establish entry-level hiring requirements. The comparison does not claim that all these skills are absent from the curriculum; course titles alone do not reveal depth. The appropriate next step is to inspect detailed course outlines and assessments.

## 4. KEEP / UPDATE / REDUCE / ADD proposal

The detailed rows and prerequisites are in `curriculum-proposal.csv`. Key decisions:

### KEEP

- **CS101 Computer Programming, CS203 Design and Analysis of Algorithms, CS302 Operating Systems, CS306 Computer Networks:** preserve foundational programming, algorithmic reasoning and systems knowledge. These foundations support later applied work; modern tools should not replace them.

### UPDATE

- **CS102 Data Structures:** add edge-case testing, complexity explanation and code review if not already assessed.
- **CS205 Web Enabled Technologies:** consider API design, accessibility, secure sessions and end-to-end testing.
- **DS202 Industry coding practice (Python/R):** make Git, debugging, automated tests and reproducibility explicit outcomes.
- **CS206 DBMS:** include query plans, transaction behaviour, constraints and safe schema/data validation in labs.
- **CS304 Software Engineering:** assess requirements traceability, code review, test strategy and release workflow.
- **DS304 Machine Learning:** assess leakage prevention, baselines, evaluation discipline and model limitations.
- **DS307 Big Data Systems and CS307 Cloud Computing:** add pipeline validation, identity/access controls, cost awareness, monitoring and rollback where these are not already covered.
- **SP301 Special Project:** require synthetic data, test evidence, risk analysis, failure recovery and a measured outcome.

These are conditional recommendations: compare the detailed syllabus and current assessments first to avoid duplicating existing work.

### REDUCE — conditional only

The photo labels two core electives as `CSXXX` without identifying their titles. The proposal conditionally considers reducing one credit from each elective only if an actual syllabus comparison establishes duplication and an approved integrated lab preserves outcomes. **Do not apply these reductions to unidentified electives automatically.** If the actual elective is not redundant or regulation disallows it, keep its credits and adjust the proposal through an approved elective/assessment route.

### ADD

- **Workflow Engineering, Testing and Responsible AI Lab:** proposed elective/module based on Task 1. It would cover workflow states, database constraints, role-based access, audit logs, failure recovery, tests and measured operational value using synthetic records. It is a proposal, not an existing official course.
- **Secure Delivery and Observability module:** embed in existing coding practice/Software Engineering where possible rather than adding credits by default. Cover CI checks, dependency hygiene, logs and rollback.

## 5. Eight to twelve specific reasons

1. CS101 and CS102 are foundations; preserve them and assess implementation quality rather than replacing fundamentals with tool-specific instruction.
2. CS203 is the natural home for algorithmic efficiency; maintain rigorous analysis and practical tests.
3. CS205 is already present by title, so verify its depth before adding a separate web course; update assessments where API/security/accessibility coverage is missing.
4. DS202 explicitly includes industry coding practice, making it a practical place to assess Git, tests, debugging and reproducibility.
5. CS206 already covers DBMS; build stronger evidence through transactions, constraints, query validation and safe data handling rather than duplicate database theory.
6. CS304 already covers Software Engineering; use its assessments for requirements, test strategy, reviews and release practices.
7. DS304 and CS305 are listed as ML and computer vision courses; use job evidence to check whether practical model evaluation and reproducibility are adequately assessed.
8. DS307 and CS307 are listed as Big Data Systems and Cloud Computing; pipeline validation, access control, observability and cost/rollback exercises can connect theory to deployment practice.
9. CS306 Computer Networks should remain because API and distributed-system work depends on network fundamentals.
10. SP301 Special Project can assess integrated engineering outcomes without assuming a new standalone course is required.
11. Performance-testing job evidence supports adding a measurable load/latency exercise to existing testing/project work, subject to course-owner review.
12. A Task 1-derived workflow lab creates a practical bridge between requirements analysis, DBMS, web technology, software testing, access control and human approval.

## 6. Credit impact and regulatory conditions

The intended scope is to affect about 36 credits of existing course/assessment content, approximately 22% of the printed programme total. The proposal does **not** intend to add 36 credits on top of the degree. Most changes are updates to existing course assessment without changing credit values. Two possible one-credit reductions are conditional on identifying the actual electives and receiving approval; a proposed new lab should preferably replace or use approved elective space rather than expand the total.

Because the photograph does not show course-level credit splits for Semesters VII/VIII and the grand total conflicts with the semester sum, a formally exact credit reallocation cannot be responsibly certified from this image alone. The course map flags this. Before adoption, the curriculum owner must verify the official version, prerequisite rules, elective combinations, internship/thesis credit allocation and regulatory limits. If no approved change is possible, implement the learning outcomes as revised assessments inside existing courses.

## 7. Five AI-assisted subject exercises

`ai-verification-log.csv` contains one exercise each for Data Structures, DBMS, Operating Systems, Computer Networks and Machine Learning. The prompts, GPT-6 model label, date, short output summary, verification method and result are recorded. The checks use synthetic examples and manual reasoning; they do not claim production-system testing. Where the verification is conceptual rather than executed, that limitation is stated.

The purpose is to demonstrate disciplined use: prompt an AI, inspect the output, verify independently, record what the human checked, and avoid using confidential data. A full submission should retain the exact prompt/output transcript if available and not misrepresent a reasoning check as execution.

## 8. Proposed lab/capstone based on Task 1

**Proposed title:** Mobile Library Issue and Due-Date Workflow Lab.  
**Host course:** CS304 Software Engineering or SP301 Special Project; alternatively an approved elective.  
**Prerequisite knowledge:** programming, basic DBMS, web/API basics and testing.  
**Learning outcomes:** model a process; design a relational record; enforce roles and state transitions; calculate a policy-based due date; audit changes; recover from failure; test edge cases; calculate net time saved; document privacy limitations.  
**Dataset:** synthetic borrowers and book references only.  
**Milestones:** (1) current-state map and assumptions, (2) schema/API and state model, (3) mobile-friendly issue/return UI, (4) role checks and audit log, (5) five exception tests, (6) measured comparison and report.  
**Acceptance tests:** normal issue, missing data, duplicate issue, unauthorised due-date edit/return action, notification/system failure with fallback.  
**Measured value:** compare current/proposed handling time plus review/support effort; report assumptions and confidence limits.

AI is not required to calculate due dates or authorise borrowing. Deterministic rules are safer and easier to audit for this workflow.

## 9. Feedback, risks and limitations

No faculty or graduate feedback is claimed because no actual voluntary response was supplied. `feedback-summary.md` records this honestly and includes optional questions to use if a willing person is available. The course version, admission batch, semester VII/VIII credit allocation, detailed course outcomes, and job-level suitability require confirmation. The current proposal relies on course titles and public job descriptions, not a full mapping of lecture plans or assessment rubrics.

## 10. Conclusion

The proposal preserves foundational CS subjects and recommends targeted practical updates, a workflow lab and stronger evidence of testing, secure design, cloud operations and AI verification. The design should be revised after confirming the applicable official curriculum and comparing the detailed existing assessments. It is a student recommendation, not an official syllabus change.
