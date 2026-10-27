# Fictional case: from discovery to a reviewed draft

**Every person, organization, achievement, number, source excerpt, conversation and date in this case was invented for this demonstration.** It is not an anonymized candidate history. The year 2029 is a fictional scenario clock, not a current vacancy claim. Reserved `example.invalid` URLs are identifiers for fixtures, not working research links.

The candidate is **Candidate Cedar**, a community equipment-desk assistant studying service design. The target is a discovery internship at the fictional **Kestrel Exhibit Systems**, which makes collection-intake software. A second opening at the same company requires unsupported production engineering. This deliberately contrasts transferable functional evidence with an industry gap.

## Read it in ten minutes

| Step | Input | Inspect the result |
|---|---|---|
| 1. Establish facts | [Evidence, bullet variants and skills](inputs/candidate-evidence.md), [master resume](inputs/master-resume.md) | Contribution limits are visible before any rewriting |
| 2. Discover and assess | [Two JDs and a mirror](inputs/job-descriptions.md) | [Evaluation](outputs/job-evaluation.md): conditional discovery fit, technical mismatch |
| 3. Learn about the company | [Synthetic source excerpts](inputs/company-source-excerpts.md) | [Company Intelligence profile](outputs/company-brief.md): executive brief, six sections and source limits |
| 4. Manage a relationship | Same source pack and hypothetical user notes | [People page](outputs/people-page.md): two toggles, one current action, unsent draft |
| 5. Tailor | JD A, raw evidence and company brief | [Proposal](outputs/tailoring-proposal.md): requirement mapping and exact edits |
| 6. Review a changed draft | [Standalone review input](inputs/review-draft.md) and raw evidence | [QA](outputs/qa-review.md): reject injected errors, check the correction |
| 7. Preserve automation state | Three discovery fixtures, two bounded simulated runs | [Digest](outputs/scan-digest.md): duplicate skip, cursor, coverage and retry behavior |

The outputs are authored reference answers, not transcripts of an actual tool run. The two conversation events are hypothetical user-provided facts. They are not evidence of real outreach. No Notion records, tasks, applications, exports or external messages are created by this case.

## Replay with an assistant, without accounts

Open this repository as read-only reference. Use one skill at a time with its linked inputs. A useful starting request is:

> Read `skills/evaluate-job/SKILL.md`, this case's candidate evidence, master resume and full job descriptions. Evaluate JD A and screen JD B. Use only these fictional files; do not browse or write to external services. Keep education equivalence unknown and distinguish the two requisitions from the mirror. Produce an assessment before reading the reference output.

Continue with Company Intelligence at Standard depth using only the source pack, producing the executive brief and all six framework sections. No JD or candidate evidence is needed for that step. For networking, ask for one source-backed contact and then supply the two hypothetical events from the People output as user notes. For tailoring, request an evidence map and proposed edits for JD A. Test QA separately: supply `inputs/review-draft.md`, original evidence and JD A **without opening the outputs folder or providing the corrected draft/reference QA answer**. Compare factual behavior, not identical prose.

Expected checks: the mirror creates no second opening; industry fit differs from functional fit; no retention or production-coding claim survives QA; education equivalence remains unknown; no draft is marked sent/submitted. All public source fixtures are fictional, so the assistant must not claim live source verification.

## Continuation checkpoint

Example job-page state after the corrected content review:

```text
Target: Kestrel Exhibit Systems / EX-KES-41
Company: the one existing Kestrel Exhibit Systems page
Application status: Considering (unchanged)
User priority: Unset (unchanged)
Requested outcome: prepare content through QA; stop before finalization
Completed: assessment; requested Standard company profile; proposed draft; QA correction check
Sources: evidence-v1; master-r0; JD-A-v1; SRC-01..06
Current draft: draft-r3
Reviewed draft: draft-r3; content Ready for user review
Open question: whether the certificate satisfies the enrollment requirement
Next action: user reviews content and verifies education equivalence
Document/PDF checks: Not assessed; no application submitted
```

A continuation request should read this checkpoint and `draft-r3`, address the open question or requested edit, then recheck affected claims. It should not restart discovery, change priority, or regenerate company research without a reason.

## Data model represented here

One Company → Jobs EX-KES-41 and EX-KES-42. One People page → two dated conversation toggles. Insights remain sections of the Company page. Source IDs and story IDs are document references, not additional databases or mandatory Notion ID columns. See the [canonical schema](../../docs/database-schema.md).
