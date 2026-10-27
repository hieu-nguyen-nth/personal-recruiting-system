---
name: resume-qa
description: Independently check a named resume draft against raw evidence and its JD; prioritize factual and coverage defects and recommend minimal corrections with explicit review limits.
---

# Resume QA — reference implementation

Require the exact draft/version, full JD and authoritative evidence. Read raw stories rather than trusting the tailoring rationale or bullet bank. Inaccessible evidence means Insufficient evidence for affected checks, not approval.

## Review order

| Pass | Verify |
|---|---|
| Facts | Titles, dates, credentials, personal contribution and source conflicts |
| Measurement | Units, baseline, sample, window, attribution and limitations; targets versus outcomes |
| Context | Assistance versus ownership, coursework versus employment, pilot versus rollout, prototype versus production |
| JD coverage | Material duties and mandatory requirements; evidence gaps versus vocabulary gaps |
| Clarity | Readable action/result, internal consistency, redundancy and supported proficiency |
| Exact file, when available | Current file's layout, page count and extraction; never infer these from text or an older export |

Prioritize unsupported claims over cosmetic improvements. Do not invent an ATS score, hiring probability or final approval. Transferable evidence can be useful without pretending to be direct industry experience.

## Findings and outcome

```text
Severity: Blocking / Material / Editorial
Draft version and exact text:
Source / JD requirement:
Why it fails:
Smallest useful correction:
Recheck result, if performed:
```

Blocking means an unsupported qualification, ownership claim or material outcome that must be resolved before content is ready. Material means ambiguous scope, obscured relevant evidence or a substantive coverage problem. Editorial means wording without factual change. Missing mandatory qualifications cannot be repaired by phrasing; retain the feasibility gap.

Conclude Revise, Insufficient evidence, or Ready for user review. Name the checked version, unresolved questions and actual checks. Content readiness differs from application eligibility and human approval. Save the checked draft and next step without changing application status.

Recommend targeted corrections, not a whole-resume rewrite. Recheck affected claims against raw evidence when text changes. If the current export was not inspected, label layout, PDF extraction and ATS behavior Not assessed.

The [fictional QA report](../../examples/fictional-case/outputs/qa-review.md) rejects a deliberately injected company-wide retention claim and production-coding claim, checks corrected wording, and keeps education equivalence unresolved. It demonstrates content review, not PDF validation or submission.
