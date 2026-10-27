# Scan digest — two simulated runs, no live execution

All records/results below are authored fixtures. No scheduler, Trackly or Notion run occurred. Query and source data: [discovery fixture](../inputs/job-descriptions.md#discovery-response-fixture). Batch limit: two raw results per run. Existing backlog at the start: zero. Company priority Unset and application status Considering remain unchanged.

## Scenario date 2029-02-02 — run 1

- Query: `fixture-collections-intern-2029`; start offset 0; raw results processed: 2 of total 3.
- Unique new openings: 1 (EX-KES-41); mirror skips: 1 (FIX-M01, same employer/requisition).
- Company records: 1; new Jobs: 1. JD A quick screen advances to the full assessment in the [evaluation](job-evaluation.md).
- Final dispositions: 1 full evaluation, 0 screen-outs. Quick screening and full evaluation of the same opening do not count as two evaluated jobs.
- Action: clarify education equivalence plus location/authorization before applying. No priority set by the agent.
- Remaining: 1 raw discovery; next cursor offset 2 with the same query key; backlog remaining 0. Market-wide coverage is not claimed.

## Scenario date 2029-02-05 — run 2

- Resume saved query at offset 2; raw results processed: 1.
- New opening: EX-KES-42; existing company reused; mirror skips: 0.
- Final dispositions: 0 full evaluations, 1 quick screen-out for the mandatory production-pipeline gap.
- Cumulative unique Jobs: 2; Company records: 1; total mirror skips: 1. Source cycle exhausted; next cycle may restart at newest. Active unevaluated backlog: 0; the eligibility action for evaluated JD A remains open.
- No changed JD or evidence for EX-KES-41: no repeated full assessment. No resume generation, research or networking performed by either scan.

## Retry and failure behavior to reproduce

Replay run 1 with its existing records: match EX-KES-41 before creation; update the same dated section. Expected delta: zero new Jobs, zero new Companies and zero duplicate digest sections. Its saved cursor remains available for continuation.

Separate failure exercise: make JD A unavailable to the assistant before evaluation. Expected: identity/limited screen may be recorded if supported, full evaluation stays incomplete, dependent assessment writes stop, and the digest names the failed source and deferred work. Do not reuse this successful reference answer as evidence that the missing source was read.

A connected implementation would additionally record actual start/completion times, source responses and record/digest readback. Those proofs cannot be supplied by this offline fixture.
