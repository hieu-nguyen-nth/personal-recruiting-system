# Personal Recruiting System

A practical kit for running a personal recruiting workflow with an assistant, Notion and a connected job source. It supports job evaluation, company research, networking, resume tailoring and independent quality review. Use existing tools; no website or backend is required.

The repository contains generic sample skills, templates and fictional examples. Your resume, evidence banks, contacts, targeting strategy, tracker links and account configuration stay in your private workspace. Cloning this repository does not install skills, connect tools or create schedules.

## How it works

![Recruiting workflow: a local job scan or user request enters one coordinator, which uses evaluation, tailoring and QA specialists, handles company research and networking, and reads or updates Jobs, Companies and People. Candidate evidence stays private; document export is deferred.](docs/recruiting-system-overview.svg)

The diagram shows one coordinator plus three specialist methods: **evaluation, tailoring and independent QA**. Company research and networking are procedures inside the coordinator in this configuration. The repository also includes optional standalone sample skills for those procedures; their presence here does not mean they are installed in a user's environment.

Local scheduled work follows the Jobs path: discover, screen, evaluate and write a digest. Research, networking and resume preparation run when requested. The human sets priorities, reviews text, sends outreach and submits applications. Actual schedules, run results and private bindings remain outside this repository; see [how to verify execution](docs/scheduling.md).

There are three linked databases. One company can have many jobs; each identified job belongs to one company. Insights live on company pages, and conversations live under dated toggles on the person's People page. Private master-resume/story/bullet/skills artifacts supply evidence rather than another tracker. The current workflow stops at text proposals and content QA; Google Docs/PDF preparation is deferred and optional. See the [schema](docs/database-schema.md), [skill catalog](docs/skills.md) and [artifact guide](docs/supporting-artifacts.md).

| Tool / person | Responsibility |
|---|---|
| Notion | Jobs, company research, contacts, conversation toggles and next actions |
| Agent + skills | Evaluate work and fit, research with sources, propose edits and check evidence |
| Trackly or another connected job source | Discover openings and retrieve JDs |
| Scheduler | Run a bounded scan in the selected runtime; local Codex requires an awake computer with the app running |
| Private files / optional document editor | Authoritative candidate evidence, resume versions and approved exports |
| You | Set priorities, correct evidence, review drafts, contact people and apply |

## Start here

1. **Understand the model:** read the [architecture](docs/architecture.md) and the single [database schema](docs/database-schema.md).
2. **Prepare private evidence:** use the [supporting-artifact guide](docs/supporting-artifacts.md). Keep your completed files outside this repository.
3. **Choose methods:** review the [skill catalog](docs/skills.md). Use your existing methods or adapt the clearly labeled samples; keep personal criteria private.
4. **Build the workspace:** give an assistant the [build prompt](prompts/build-your-workspace.md) and a privately completed [setup note](templates/private-setup.md). Inspect/reuse existing trackers, preserve assignments and notes, then verify relations.
5. **Try a small workflow:** follow the [fictional worked example](docs/worked-example.md) and [request guide](docs/using-the-workflow.md). Evaluate a job, save a company finding, log a real conversation in a person's page, then prepare text and run separate QA.
6. **Create the actual schedule:** follow [scheduling](docs/scheduling.md), observe the one-time test and then the first recurring scan. A saved prompt is not execution proof.
7. **Review before sharing:** check all files and history using the [privacy guide](docs/privacy-review.md).

## What to customize

Industry fit, functional fit, problem similarity, career learning and eligibility are useful evaluation dimensions. Their importance depends on your goals; the sample uses qualitative evidence rather than a personal scoring formula. A strong functional match can coexist with limited industry experience or unknown eligibility. See the [worked assessment and resume example](docs/worked-example.md).

Skills are instruction sets; connectors provide access to services; the scheduler triggers execution; Notion preserves work between chats. None substitutes for another. Checks on resume content do not prove PDF layout or employer ATS performance. Company priority, application status and referral willingness must not be inferred from an agent recommendation.
