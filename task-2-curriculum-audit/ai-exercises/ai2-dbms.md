# AI Exercise 2 — Database Management System

## Prompt

> Write a SQL query that returns departments with more than one employee using a synthetic Employees table; explain GROUP BY and HAVING.

## Model and date

- Model: GPT-6
- Date: 2026-10-23

## Output summary

The model returned a query of the form:

```sql
SELECT department_id
FROM Employees
GROUP BY department_id
HAVING COUNT(*) > 1;
```

It also explained that GROUP BY aggregates rows by department, while HAVING filters grouped results based on the aggregate count.

## Verification

A synthetic table was checked with department IDs D1, D1, D2, and D3.

- D1 appears twice
- D2 appears once
- D3 appears once

Expected result: only D1.

## Result

The query logic is correct for the synthetic example and the explanation of GROUP BY/HAVING is accurate. The record does not claim production database use or personal data handling.
