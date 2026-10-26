# Personal Recruiting System

A practical kit for running a personal recruiting workflow with an assistant, Notion and a connected job source. It supports job evaluation, company research, networking, resume tailoring and independent quality review. Use existing tools; no website or backend is required.

The repository contains generic sample skills, templates and fictional examples. Your resume, evidence banks, contacts, targeting strategy, tracker links and account configuration stay in your private workspace. Cloning this repository does not install skills, connect tools or create schedules.

## How it works

![Ideal recruiting architecture: a verified schedule or user request enters one coordinator with five specialist methods for evaluation, company research, networking, tailoring and QA. Notion holds Jobs, Companies and People; private evidence and configured document tools support checked application files and human approval.](docs/recruiting-system-ideal.svg)

This is the **ideal reference architecture**, not a report of an individual's local installation. It contains one coordinator and five specialist methods: **evaluation, company research, networking, tailoring and independent QA**. The six generic sample skills in this repository illustrate those modules; a smaller installation can keep research and networking inside the coordinator. Cloning the repository does not activate them.

Scheduled work follows the Jobs path: discover, screen, evaluate and write a digest. Research, networking and resume preparation run when requested. Use a verified local or cloud runtime according to your operating needs; local Codex requires an awake computer with the app running. The human sets priorities, reviews materials, sends outreach and submits applications. Local implementation diagrams, actual schedules, run results and private bindings stay outside this repository; see [how to verify execution](docs/scheduling.md).

There are three linked databases. One company can have many jobs; each identified job belongs to one company. Insights live on company pages, and conversations live under dated toggles on the person's People page. Private master-resume/story/bullet/skills artifacts supply evidence rather than another tracker. The complete target workflow includes editable documents, PDF export and exact-file QA through configured document tools. This stage is optional for a text-only installation and requires its own capability checks. See the [schema](docs/database-schema.md), [skill catalog](docs/skills.md) and [artifact guide](docs/supporting-artifacts.md).

| Tool / person | Responsibility |
|---|---|
| Notion | Jobs, company research, contacts, conversation toggles and next actions |
| Agent + skills | Evaluate work and fit, research with sources, propose edits and check evidence |
| Trackly or another connected job source | Discover openings and retrieve JDs |
| Scheduler | Run a bounded scan in a verified local or cloud runtime; check tool access and actual writeback |
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
