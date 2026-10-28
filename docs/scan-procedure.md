# Maintained scan procedure

Use this as a generic starting procedure, with actual bindings and parameters supplied privately. The [short trigger](../prompts/daily-scan.md) points here or to a private adapted copy. Editing a document does not create, move or pause a task.

## Inputs and preflight

Read the private setup, configured search scope/limits, previous digest and selected evaluation method. Verify the executing environment can read the exact evidence and access job-source and Notion tools. Inspect schemas and use existing saved views where available. Missing required access stops dependent writes and produces a precise blocker.

## Bounded work

1. Use the saved query/cursor for unfinished discovery. Keep raw result count within the configured limit, including mirrors. Record source-reported total/remaining count when provided; otherwise say unknown. Resume the same query before starting another newest-first cycle.
2. Match employer/requisition and canonical URL against existing Jobs before creating. Reuse the existing Company page and relation. Two requisitions create two Jobs; an aggregator mirror of one requisition does not.
3. Quick-screen discoveries. Run full evaluation only with the full JD for viable/unclear roles; separately bound the active unevaluated backlog. Read prior assessments before treating blank metadata as missing work. Re-evaluate only for material JD changes or explicit requests.
4. Preserve user priority, application status, original notes and provider saved statuses. Keep eligibility unknown where evidence is absent. Carry forward an unchanged user-dependent action without repeatedly requesting the same input.
5. Leave failed or inaccessible assessments incomplete. Process independent items only if available within the same bounds; report partial coverage and the exact deferred work.

## Digest and continuation

Use one stable date section for the configured reporting timezone. On retry, update that section and match existing records; do not duplicate jobs, companies or reports. Record actual execution times in live runs, source/query coverage, new unique openings, duplicate skips, full evaluations, screen-outs, backlog/deferred counts, next cursor, known deadlines, actions/owners and errors. Unknown totals stay unknown.

Quick screening followed by full evaluation is one opening with a full final disposition, not two evaluated jobs. An evaluated role can retain an unresolved eligibility action without remaining an unevaluated backlog item. Verify changed records and the digest by readback before reporting successful persistence.

No resume generation, deep research, people discovery, event logging, outreach, referrals, submissions, master-evidence edits or document/PDF work occurs in this default scan. Those are separate requests. Configure notification behavior through the scheduler's supported settings; useful outcomes are worthwhile new roles, time-sensitive actions, failures or input required.

The [two-run fixture](../examples/fictional-case/outputs/scan-digest.md) illustrates cursor continuation and expected retry/failure behavior without pretending to be execution evidence. See [scheduling](scheduling.md) to create and verify an actual task.
