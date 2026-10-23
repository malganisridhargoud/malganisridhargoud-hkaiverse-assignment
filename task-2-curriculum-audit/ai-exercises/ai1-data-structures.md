# AI Exercise 1 — Data Structures

## Prompt

> Explain how to detect a cycle in a linked list using Floyd’s slow/fast pointer method and give a small dry run.

## Model and date

- Model: GPT-6
- Date: 2026-10-23

## Output summary

The model stated that a cycle can be detected by moving one pointer one node at a time and a second pointer two nodes at a time. If the fast pointer reaches null, there is no cycle. If the two pointers meet, a cycle exists. It also described a short dry run with a sequence of pointer movements.

## Verification

A manual dry run was carried out on two synthetic cases:

1. Acyclic list: A → B → C → null
   - slow = A, fast = A
   - slow moves to B, fast moves to C, then fast reaches null
   - Result: no cycle

2. Cyclic list: A → B → C → B
   - slow = A, fast = A
   - slow advances to B, fast advances to C, then to B
   - Result: pointers meet; cycle exists

## Result

The logic matches Floyd’s cycle-detection algorithm and is consistent with the manual trace. This is a conceptual verification and does not claim compiled code execution or a live program run.
