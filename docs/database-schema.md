# Database schema

This is the single reference for fields, relations, page content and setup checks. Reuse existing names/status options and add a field only if an equivalent is absent. Three databases are sufficient: Jobs, Companies and People. Conversations are dated toggles inside a People page, not a fourth database.

## Relations

```mermaid
erDiagram
    COMPANIES ||--o{ JOBS : "has openings"
    COMPANIES }o--o{ PEOPLE : "professional associations"

    COMPANIES {
        title Name
        url Website
        select UserPriority
        select ResearchDepth
        date LastReviewed
        relation Jobs
        relation People
    }
    JOBS {
        title Role
        relation Company
        rich_text JDLink
        select ApplicationStatus
        select EvaluationStatus
        date LastEvaluated
        rich_text NextAction
        date NextActionDate
        url ResumeLink
    }
    PEOPLE {
        title Name
        relation Company
        rich_text Channel
        status Stage
        rich_text CurrentRole
        date LastChecked
        rich_text NextAction
        date NextActionDate
    }
```

**One company → many jobs.** A verified opening belongs to one company. An unresolved inbox item may temporarily have an empty Company field; resolve it before treating its identity as established. The diagram describes the intended model, not a claim that every live workspace enforces required fields. Native Notion page identities need no extra ID column.

| Relation | Reverse property | Configuration |
|---|---|---|
| Jobs.Company → Companies | Companies.Jobs | Limit Jobs.Company to **1 page**; Companies.Jobs has **No limit**. Many distinct openings point to the same company page. |
| People.Company → Companies | Companies.People | Preserve multiple known professional associations; both sides may have many pages. One person still has one People record. |

Enable the corresponding reverse property and reuse it if already present. Notion supports two-way relations and a `1 page` / `No limit` setting. Verify the actual setting; a textual schema is not proof it has been applied. [Official relation documentation](https://www.notion.com/help/relations-and-rollups).

## Fields and page content

| Database | Minimum properties | Page body |
|---|---|---|
| Jobs | Existing role title, Company relation, JD link, application status and notes; evaluation state/date, next action/date, resume link if needed | Source/canonical identity; assessment with evidence and unknowns; last completed preparation step, requested stopping point, next step and exact draft version |
| Companies | Name, website, user priority, research depth, last reviewed; reciprocal Jobs and People | Executive intelligence brief; six-section company profile; dated sourced insights; role/team criteria; open questions. See [company template](../templates/company-page.md). |
| People | Existing name, Company relation, profile/contact channel, relationship stage and notes; current role, last checked, next action/date if needed | Identity/source notes plus one dated toggle per actual conversation or outreach event. See [person template](../templates/person-page.md). |

Suggested evaluation states: Not evaluated, Screened out, Evaluated, Needs info, Error. This is separate from application status. Empty metadata does not prove an earlier assessment is absent: read the page first. Unknown eligibility is not a rejection. Retain existing application and relationship status options.

Research Depth can retain existing Basic (Quick alias) and Deep choices while adding Standard. Preserve saved values; use Standard at execution time only when neither a request nor saved depth exists. Company Intelligence sections belong in the existing page body, not six new columns or another database.

Keep one Company property per tracker. Reuse JD Link and Channel/profile fields; do not add URL copies. Put a genuine provider/requisition ID in job-page metadata when useful. Deduplicate by employer and requisition/canonical URL, including aggregator mirrors. Two different openings at the same company are two Jobs rows, not duplicates.

## Conversation storage

Each contact's page contains dated native Notion toggles such as `YYYY-MM-DD — video call — product team`. Preserve every earlier toggle. Append new factual notes or revise the matching toggle when correcting that conversation; retrying the same request must not append it twice. Keep only the current next action/date in the People properties for sorting; the dated toggle retains its context and agreed follow-up. Draft outreach is labeled Draft and never recorded as sent without evidence.

## Views and setup checks

Use **Needs evaluation** for active unreviewed/Needs info/Error jobs; **Considering decisions** for unresolved actions even after evaluation; **Companies** for priority/depth; and **Networking actions** for People with a due next action. No conversation-table view is needed.

1. Read the live schemas and privately back up affected records, views and company assignments. Complete pagination before claiming full coverage.
2. Reuse/create Companies; map old labels to specific company pages. Resolve ambiguous aliases; preserve blanks and all existing associations. Do not collapse several job rows into one company row.
3. Migrate the existing Jobs.Company to a relation, restore mapped values, enable reciprocal Jobs and set the single-page limit. If old rows have multiple companies, resolve those cases before restricting them; do not silently drop values.
4. Migrate People.Company similarly, retaining multiple associations and reciprocal People. Keep all conversation toggles and notes in their original person pages. Do not create or delete another database as part of this template.
5. Read back all mapped assignments and unaffected statuses/notes/dates. Check two different jobs opening the same company page, the company's reverse Jobs list, a person's company links and unchanged conversation toggles. Inspect the real relation limits and views.

These steps describe the target setup, not an instruction to run unverified connector-specific DDL. Use the chosen connector's documented capabilities or the Notion UI after inspecting the live schema. See the [build prompt](../prompts/build-your-workspace.md).

## Inspect the fictional records

The [case checkpoint](../examples/fictional-case/README.md#continuation-checkpoint), [role assessments](../examples/fictional-case/outputs/job-evaluation.md), [company page](../examples/fictional-case/outputs/company-brief.md) and [People page](../examples/fictional-case/outputs/people-page.md) show this model with invented records. One company owns two distinct openings; both hypothetical conversations remain inside one People page. These Markdown fixtures do not create Notion databases.
