# Minimal Notion structure

Inspect each live data source before writing. Names below are recommended mappings, not assumptions about existing trackers. Reuse equivalent properties before adding anything. Keep existing titles, status values, dates and rich-text notes. If an existing Company label already works, keep it; put navigation relations on Companies rather than adding a parallel Company column to every tracker.

| Record | One row represents | Minimum fields |
|---|---|---|
| Jobs | One specific opening | Existing role title, Company, JD link, application status and notes; Evaluation Status (select), Last Evaluated (date), Next Action (text), Next Action Date (date), Resume Link (URL), only if absent |
| Companies | One company, independent of an opening | Name (title), Website (URL), User Priority (select: Unassigned/High/Normal/Low), Research Depth (select: Basic/Deep), Last Reviewed (date); one-way Jobs and People navigation relations |
| People | One professional contact | Existing name, Company, relationship stage, contact/profile channel and notes; Current Role (text, including team if known), Last Checked (date), Next Action (text), Next Action Date (date), only if absent |
| Interactions | One dated conversation or outreach event | Existing title, date, takeaway, follow-up and follow-up date; Person (relation to People) |

Evaluation Status: **Not evaluated, Screened out, Evaluated, Needs info, Error**. Treat an empty value as not yet reviewed by this workflow. Inspect earlier assessments in the page before reevaluating; empty metadata does not prove no prior evaluation exists. Evaluation status is independent of whether an application was submitted.

Use a company page's narrative for current brief, sourced insights, team criteria and open questions. Use a job page for the assessment and a small preparation note: last completed step, next step, requested stopping point, exact draft/PDF version and unresolved questions. Keep relationship facts and evidence on the person's page and dated conversations in Interactions.

## Views

- **Needs evaluation:** active/considering jobs whose evaluation status is empty, Not evaluated, Needs info or Error. Closed, skipped and rejected applications are excluded according to the user's actual status mapping.
- **Companies:** identity, user priority, depth and review date, with priority filtering.
- **Networking actions:** people with a next action, sorted by its due date. Use the existing people table to browse all contacts.
- **Interactions:** person, event date, takeaway, follow-up and due date.

Backfill Companies' navigation relations from existing exact company labels; retain the original label fields. The agent maintains those navigation links when adding records. Do not silently merge aliases, change relationship stage or claim a profile was freshly checked just because its URL was copied. Reuse an existing Channel/profile field instead of copying the same URL into a new column. Deduplicate jobs using their existing JD link; store an actual provider ID in page metadata when available rather than introducing a column that merely repeats the URL. Seed companies as unresearched with Unassigned priority; leave unknown website and review date blank. For a new workspace, create the four tables; for an existing workspace, reuse equivalent tables.

## Completion checks

Read back the schema and views. Confirm record counts, existing application/relationship statuses, note text and dates were preserved. Verify relation targets on a job, a person and an interaction. After an uncertain create, query before retrying. If a query is paginated, finish reading every page before claiming full migration coverage.
