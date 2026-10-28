# Personal Recruiting System

A recruiting workflow built from an assistant, reusable skills, Notion and a connected job source. It connects discovery, company learning, relationships and evidence-backed resume preparation without a custom website or backend.

This repository is a **reference implementation and a fictional demonstration**. It exposes system design and operating methods, not a candidate's resume, contacts, personal strategy or account configuration. Cloning it does not install skills, connect accounts or create a schedule.

## See the system work

Start with the [complete fictional case](examples/fictional-case/README.md). Follow two openings at one company from discovery to an independently reviewed text draft. Inspect the raw evidence, requirement mapping, exact edits and QA corrections. Every case fact was invented from scratch; it is not an anonymized resume.

| Capability demonstrated | Inspectable evidence |
|---|---|
| Workflow and agent instruction design | [Six detailed skills](docs/skills.md): inputs, decision steps, outputs, stopping conditions and handoffs |
| Information modeling | [One canonical schema](docs/database-schema.md): one company → many jobs; personal conversations inside People pages; event insights in Events |
| Evidence-based decisions | [Role assessment](examples/fictional-case/outputs/job-evaluation.md) separates industry, functional and feasibility questions |
| Research translated into action | [Six-section company profile](examples/fictional-case/outputs/company-brief.md) explains business, product, competition, recent changes and PM culture/hiring with source limits |
| Relationship continuity | [People page](examples/fictional-case/outputs/people-page.md) preserves two conversations and a current action |
| Resume tailoring and quality control | [Exact changes](examples/fictional-case/outputs/tailoring-proposal.md), [draft versions](examples/fictional-case/outputs/resume-draft.md), [rejected claims and correction check](examples/fictional-case/outputs/qa-review.md) |
| Reliable bounded automation | [Simulated digest](examples/fictional-case/outputs/scan-digest.md) shows deduplication, deferred cursors and retry/failure expectations |
| Engineering judgment | [Design decisions and tradeoffs](docs/design-decisions.md); [capability and validation boundaries](docs/capabilities-and-validation.md) |

## Architecture

![Ideal recruiting architecture: a request or verified schedule enters one coordinator with methods for evaluation, research, networking, tailoring and QA. Notion holds Jobs, Companies, People and Events. Private evidence supports reviewed application content and optional document outputs; humans decide, contact people and submit.](docs/recruiting-system-ideal.svg)

This is the **ideal reference architecture**, not a diagram of an individual's enabled installation. One coordinator routes five specialist methods. Company Intelligence is a standalone research method; a compact installation can keep networking inside its coordinator. Six public skill folders do not imply six installed personal skills. See [components and handoffs](docs/architecture.md).

Notion holds Jobs, Companies, People and Events. A company can have many openings; its executive intelligence brief, six-section profile and dated insights stay on the company page. Research starts from a company name/URL without requiring a JD or resume. Companies link to many JDs, People and Events. People can link to many Companies and Events; Events can link to many Companies and People. Each JD links to one Company. Individual conversations live under dated toggles in a person's page. Event-wide insights live in Events, with many-to-many Companies/People links; see the [event template](templates/event-page.md). Private master-resume, story, bullet and skills artifacts supply evidence. Optional document tools format/export approved content and require separate exact-file checks.

Scheduled work discovers, screens, evaluates and saves a bounded digest. Research, networking and resume preparation run on request. The human controls priorities, corrects facts, reviews materials, sends outreach and submits applications. Local execution requires an awake computer with the app running; cloud execution requires separately verified access. No live schedule, private binding or individual run log is included.

## Duplicate the system

1. **Understand the decisions:** read [architecture](docs/architecture.md), [tradeoffs](docs/design-decisions.md) and the [schema](docs/database-schema.md).
2. **Replay offline first:** follow the [fictional case](examples/fictional-case/README.md). No accounts are needed; the outputs are reference answers, not live execution proof.
3. **Prepare private inputs:** use the [artifact guide](docs/supporting-artifacts.md) and copy its [blank pack](templates/supporting-artifacts.md) outside this checkout. Supply your own facts and goals.
4. **Choose methods:** read the [skill catalog](docs/skills.md). Load repo-local instructions or adapt/install them without overwriting existing personal skills. Installation alone grants no service access.
5. **Connect and map privately:** complete the [setup note](templates/private-setup.md) outside the repo and use the [build prompt](prompts/build-your-workspace.md). Inspect existing trackers, reuse fields and verify relations before relying on them.
6. **Try one real request:** use the [request guide](docs/using-the-workflow.md). Save the exact draft, reviewed version and next action so another chat can continue.
7. **Create and verify scheduling:** follow [schedule setup](docs/scheduling.md), observe the actual test and first recurring run. Keep procedures in a maintained reference; keep the trigger short.
8. **Review before publishing:** check the complete proposed tree, history and metadata using the [sharing review](docs/privacy-review.md).

The examples use general industry, function, problem, learning and feasibility dimensions, without private scoring weights or personal targeting rules. Skill instructions, connectors, schedulers and saved records have separate responsibilities. Text QA does not establish PDF layout or employer ATS performance. See [what is demonstrated versus verified](docs/capabilities-and-validation.md).
