---
name: evaluate-job
description: Quickly screen or fully assess a job against evidence, career goals and feasibility; distinguish unknowns from blockers and save an actionable recommendation.
---

# Evaluate a job — reference implementation

Read the exact JD, source/check date, existing assessment, relevant company brief, candidate evidence and privately supplied goals. Use an established private method when configured; otherwise use this qualitative framework. This skill does not rewrite resumes or supply personal weights.

## Identity and depth

Match employer/requisition, then canonical URL. An aggregator mirror is another source for the same opening. A matching title alone does not justify merging records.

**Quick screen:** inspect function, required level, timing/location and explicit mandatory requirements. Screen out only for a supported mismatch; otherwise advance or flag missing information. An inaccessible full JD can support only a limited screen, never a full evaluation.

**Full evaluation:** read the complete posting, identify the main deliverable and map material requirements to evidence. Re-evaluate when the JD materially changes or the user requests it, rather than because another scan occurred.

## Assessment

| Dimension | Decision question | Evidence |
|---|---|---|
| Industry / customer | Direct domain experience or transferable understanding? | Actual customers, workflow and operating context |
| Function | Has the candidate performed the required work? | Personal actions, decisions, deliverables and collaboration |
| Problem / product | How similar are the problem and constraints? | Product surface, complexity, scale and method |
| Career value | What would the assignment add? | Ownership, mentorship and learning; unconfirmed details remain unknown |
| Feasibility | Are explicit requirements established? | Education equivalence, dates, location and stated authorization conditions |

Use Strong / Partial / Gap / Unknown with a source and implication. Absence of evidence differs from evidence of absence. Do not infer citizenship, sponsorship or credentials. For a configured numeric method, preserve its treatment of unknown inputs rather than silently rescaling.

An adjacent industry can offer strong functional fit; an attractive employer cannot erase an unsupported mandatory technical requirement. Identify the fact most likely to change the recommendation.

## Output and persistence

```text
Identity / source version / date / review depth:
Actual work and expected deliverable:
Fit: dimension | judgment | source | implication
Hard mismatch versus decision-changing unknowns:
Recommendation and evidence limits:
Next action and owner:
Evaluation state; user priority preserved:
```

Use current status options. Evaluated can coexist with unknown eligibility if the assessment is complete. Needs info means a missing input prevents completing the assessment; Error means an operation failed. Do not change application status merely because a role was assessed. Read earlier notes before saving; verify the result and Company relation afterward.

The [fictional assessment](../../examples/fictional-case/outputs/job-evaluation.md) gives a discovery role strong observation fit but limited industry experience and unknown education equivalence. A second role is screened out for a mandatory production-pipeline gap. Both link to one company; the first role's mirror is skipped.
