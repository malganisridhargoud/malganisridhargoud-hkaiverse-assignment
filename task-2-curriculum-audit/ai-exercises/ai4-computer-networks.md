# AI Exercise 4 — Computer Networks

## Prompt

> Explain what an HTTP 404 response means and distinguish it from a DNS resolution failure.

## Model and date

- Model: GPT-6
- Date: 2026-10-23

## Output summary

The model explained that a 404 is an HTTP response from a reachable server indicating that the requested resource was not found, while a DNS failure happens before the client reaches the intended host.

## Verification

The distinction was checked against the HTTP semantics reference and the general DNS resolution flow:

- DNS failure: client cannot resolve the domain name to an IP address; the request never reaches the target service
- HTTP 404: client reaches the server and the server responds with a 404 status code because the resource is not found

## Result

The distinction is correct and matches the relevant protocol-level semantics. This was a conceptual verification and not a live network capture exercise.
