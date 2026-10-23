# AI Exercise 3 — Operating Systems

## Prompt

> For processes P1 (arrival 0, burst 4) and P2 (arrival 1, burst 2), calculate FCFS completion, turnaround and waiting times.

## Model and date

- Model: GPT-6
- Date: 2026-10-23

## Output summary

The model stated that the FCFS order is P1 then P2. It reported completion times of 4 for P1 and 6 for P2; turnaround times of 4 and 5; and waiting times of 0 and 3.

## Verification

A Gantt chart was checked manually:

- Time 0–4: P1 runs
- Time 4–6: P2 runs

Calculations:

- P1 completion time = 4; turnaround = 4 − 0 = 4; waiting = 4 − 4 = 0
- P2 completion time = 6; turnaround = 6 − 1 = 5; waiting = 5 − 2 = 3

## Result

The arithmetic is consistent with the manual schedule. This is a synthetic manual check, not a full OS simulator or lab execution.
