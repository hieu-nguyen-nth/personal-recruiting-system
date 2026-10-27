# Skill catalog and handoffs

Six public reference skills define triggers, inputs, procedures, outputs and stopping conditions. They are general methods authored for this kit, not copies of private candidate methods. Personal scoring weights, real evidence and networking preferences belong in the private setup.

| Skill | Required inputs | Output / handoff | Inspect an example |
|---|---|---|---|
| [Coordinator](../skills/recruiting-coordinator/SKILL.md) | Request, private setup, existing record/checkpoint | Selected method, exact draft/version and next action; honors requested stop | [Continuation state](../examples/fictional-case/README.md#continuation-checkpoint) |
| [Evaluate job](../skills/evaluate-job/SKILL.md) | Full JD for full review, candidate evidence, goals, existing assessment | Quick/full assessment, evidence, unknowns, recommendation | [Two role decisions](../examples/fictional-case/outputs/job-evaluation.md) |
| [Company Intelligence](../skills/research-company/SKILL.md) | Company name/URL, depth, prior notes and sources; JD/resume optional | Executive brief + six-section profile; Quick/Basic, Standard, Deep or focused refresh | [Company brief](../examples/fictional-case/outputs/company-brief.md) |
| [Manage networking](../skills/manage-networking/SKILL.md) | Company/person, criteria, verified sources or actual notes | Source-backed discovery/refresh or a dated toggle; current action preserved | [People page](../examples/fictional-case/outputs/people-page.md) |
| [Tailor resume](../skills/tailor-resume/SKILL.md) | Exact JD, master resume, stories, bullet/skills evidence | Positioning, requirement mapping, exact edits and a named draft | [Tailoring proposal](../examples/fictional-case/outputs/tailoring-proposal.md) |
| [Resume QA](../skills/resume-qa/SKILL.md) | Exact draft, raw evidence and JD | Prioritized defects, minimal corrections and named-version outcome | [Rejection and recheck](../examples/fictional-case/outputs/qa-review.md) |

## Use and install

Load the relevant SKILL.md as instructions, or adapt/install through your environment's supported skill flow. These repo-local folders are not automatically installed. Avoid overwriting a same-named personal skill: choose a separate name/location. Installation grants neither account access nor scheduled execution.

Links work within this checkout. If installing a skill elsewhere, preserve accessible linked resources or replace relative paths with configured private locations. The [artifact guide](supporting-artifacts.md) and [blank pack](../templates/supporting-artifacts.md) define inputs without requiring a particular vendor for private files.

A compact installation can use coordination, evaluation, Company Intelligence, tailoring and QA as five separate methods, with networking handled inside coordination. The six public modules describe reusable responsibilities, not six proven personal installations. See [capability boundaries](capabilities-and-validation.md).

## Run an application workflow

Evaluate or load the existing assessment → reuse/request company research → map requirements to evidence → tailor → review the exact draft against raw sources → save checkpoint → human review. Networking is optional and requested separately. Stop after any named stage. A change to text/evidence reopens affected QA; saved state permits continuation across chats.

The [offline replay](../examples/fictional-case/README.md#replay-with-an-assistant-without-accounts) gives an explicit prompt and expected behaviors. Match facts, decisions and limits, not identical wording. The QA pass is separate from tailoring reasoning; independent human review remains valuable.
