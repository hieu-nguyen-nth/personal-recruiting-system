# Person page template

Use one existing People record per verified person. Keep company links, current role, channel, relationship stage and current next action/date in the properties. Preserve earlier user notes and factual-source links in the page body.

## Identity and context

Verified professional profile; current role/team and source/check date; connection evidence if requested; uncertainties. A shared affiliation is not referral willingness. Do not infer identity or background from a name.

## Conversation history

Create a native Notion toggle for each dated conversation or outreach event. The collapsible block below is a GitHub representation of the format, not a Notion API payload. When using a connector, read its supported block format and preserve existing toggles.

<details>
<summary>YYYY-MM-DD — channel — topic</summary>

- Context and purpose:
- Actual notes / useful details:
- Agreed next step and due date, if any:
- Supporting link, if appropriate:
- Message state, if relevant: Draft / actually sent / reply received. Record only what happened.

</details>

Use a separate dated toggle for the next conversation. Correct a matching entry rather than duplicating it on retry. Update the People next-action properties to the current follow-up, while retaining the earlier agreement inside its dated toggle.

See the [completed synthetic People page](../examples/fictional-case/outputs/people-page.md) for two hypothetical conversations and a later current action. No real outreach is represented.

Related events appear through the Events relation. A linked speaker/attendee context is not automatically a conversation. General event insights stay on the event page; a personal conversation may reference it without copying all its notes.
