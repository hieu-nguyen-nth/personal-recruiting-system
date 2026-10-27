# Component architecture

This is the ideal reference architecture shown in the [overview](recruiting-system-ideal.svg). It describes the complete target workflow, not an individual's enabled capabilities. Actual local implementation views and execution evidence remain private.

The coordinator is an instruction set executed by the assistant. It routes evaluation, company research, networking, tailoring and independent QA through configured methods; a smaller setup can combine procedures inside the coordinator. It is not a continuously running server. The reusable repository contains no live account configuration.

| Component | Reads | Produces / owns |
|---|---|---|
| Request or scheduler | Specific record/request, cadence and scope from private setup | Starts one bounded execution in the chosen runtime |
| Coordinator | Current record, source material, private setup and selected skill | Chooses the next step; records completion or the precise blocker |
| Job-source connector | Search constraints or exact provider ID | Full JD, source URL and provider availability; not a guarantee of live employer status |
| Research tools | Public company/professional sources and prior notes | Dated facts, citations, labeled inference and unknowns |
| Five specialist methods | JD, company/contact context and the relevant private artifacts | Evaluation, research, networking updates, evidence-backed proposals and independent review; see [skill catalog](skills.md) |
| Notion | Existing schemas, records, relations and page bodies | Three linked databases, source-backed assessments, research, conversation toggles and saved next steps |
| Optional document tools | Approved text and a copied template | Editable resume and exact exported file, separately checked for layout |
| Human | Recommendations, proposed changes and QA findings | Priorities, factual corrections, final approval, outreach and submission |

## Execution and handoffs

A discovered role is matched to Jobs by canonical employer/requisition before creation. A second role at the same company gets a different Jobs row linked to the existing company. Each new discovery receives a quick scope screen; viable/unclear roles use the selected evaluation method. The scan reports work left unfinished rather than marking the whole market reviewed.

Company research is reused across roles. Basic research establishes products, customers, direction and useful questions. Deep research connects recent primary-source evidence to team criteria, candidate positioning and unresolved decisions. User priority controls extra effort; an agent's fit assessment does not set it automatically.

People holds current contact facts and actionable follow-up. A person's page holds all conversation history under dated toggles. Refreshing a role or adding a conversation preserves earlier toggles, user notes and relationship stage. See the single [schema](database-schema.md) for relations and field ownership.

Tailoring proposes supported changes using the current evidence. QA independently checks the actual draft against the JD and raw evidence. User edits invalidate checks on affected text. Text QA can finish without document export; final-file claims require checking that exact file.

The job page is the continuation point: last completed step, next step, requested stopping point, exact current draft and open questions. The scheduler owns timing/history; a private setup note holds bindings and the linked digest. Avoid concurrent edits to the same record; no queue or locking service is needed for this personal workflow.

## Completion boundaries

A configured schedule is not an observed run. Record the actual scheduled trigger, tool results and verified Notion writeback; test the recurring task separately. This can prove local integration without proving laptop-closed operation. See [scheduling](scheduling.md). Store actual IDs, timestamps, test employers and results privately; the shared kit documents how to repeat the checks.

A tool failure leaves its dependent step incomplete. A stored JD read is not a fresh employer-site check. A contact match is not a referral. A draft is not a sent message or submitted application. These distinctions make the system resumable without inventing progress.

## Inspect implementation decisions

Read the [decision/tradeoff log](design-decisions.md) for why these components exist, the [case](../examples/fictional-case/README.md) for inspectable handoffs, and [capability boundaries](capabilities-and-validation.md) for the distinction between authored outputs, private integration experience and optional target features. The [maintained scan procedure](scan-procedure.md) keeps detailed behavior out of the trigger prompt.
