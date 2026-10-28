# Design decisions and tradeoffs

These decisions explain the architecture in the [README](../README.md). The goal is a personal workflow that can be understood, inspected and resumed, without building a new application.

| Problem | Chosen approach | Why / practical limit |
|---|---|---|
| Information split across chats and files | Notion keeps durable Jobs, Companies, People and Events; a private setup note locates methods/evidence | A new chat can reload state. It must actually read those references; chat memory is not a database. |
| Several roles share the same company learning | One company → many jobs; company-page research is reused | Avoids inconsistent duplicate briefs. Role-specific requirements still belong on each Job. |
| Relationship history needs context | One People record with dated conversation toggles; current next action in properties | Preserves a readable history and sortable action. Cross-contact conversation analytics remain limited. Shared event insights use a separate Events record rather than being copied into every person. |
| Similar openings appear in multiple sources | Match employer/requisition and canonical URL before creating | Prevents mirror duplicates. Ambiguous identity needs review; a title match alone is insufficient. |
| Long prompts are difficult to maintain | Short scheduler trigger refers to a maintained scan procedure and private setup | Procedures can change in one place. That reference must remain readable to the execution environment; failure stops dependent work. |
| Bounded scans might repeatedly see the first page | Save query + cursor and deferred counts in the digest | Continues unfinished coverage without another queue. A cursor is only meaningful for its query; restart at newest after the cycle ends. |
| Resume rewriting can inflate claims | Requirement-to-story mapping, exact edits and a separate QA pass over raw evidence | Makes contribution/scope visible. A separate pass reduces shared assumptions but is not proof of a separate evaluator or of factual truth beyond supplied sources. |
| Work may stop mid-application | Save draft version, reviewed version, open questions and next owner on the Job | Another chat can resume. Changes to evidence or text reopen affected checks. |
| Tool failures can look like successful work | Record source coverage, blockers and write/readback results | Honest partial completion is useful. A generated report cannot substitute for actual connector or scheduler proof. |
| New infrastructure would add maintenance | Existing assistant, connectors, Notion and private files; optional document tools | Local scheduling requires an awake host. Cloud operation needs separate verification; no website, API server, queue or custom database is required. |

## What readers should be able to inspect

The [case](../examples/fictional-case/README.md) provides raw inputs and outputs at the handoffs. Check whether the assessment follows the JD, each resume claim follows a story, and QA rejects a later unsupported revision. Those inspectable decisions demonstrate the design more clearly than an architecture picture alone.

## When the design would change

A team editing concurrently, large-scale discovery, or a need to query thousands of individual interactions could justify stronger coordination or another data model. Those are new requirements, not prerequisites for one person's recruiting workflow. Add infrastructure only after a measured limitation makes its benefit concrete.
