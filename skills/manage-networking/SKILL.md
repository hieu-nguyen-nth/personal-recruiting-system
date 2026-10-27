---
name: manage-networking
description: Discover or refresh professional contacts and log actual conversations inside People pages; verify identity, preserve history and distinguish drafts from events.
---

# Manage networking — reference implementation

Read the People record, company associations, earlier notes/toggles and user's connection criteria. This sample supplies no school, nationality or personal connection preference.

## Discover

Search accessible professional/company sources for the requested team or connection. Return a small useful shortlist, not an assumed referral list.

| Field | Evidence standard |
|---|---|
| Identity/profile | Matching professional profile; state ambiguity |
| Current role/company | Source and checked date; distinguish previous employment |
| Requested connection | Explicit affiliation evidence; do not infer background from names |
| Relevance | How the person's actual work can answer the question |
| Next step | Specific question or optional draft; referral willingness stays unknown |

Limited source access means a smaller verified result and an explicit limitation. Do not invent profile URLs, email patterns or connections to complete a table.

## Refresh

Match identity before updating. Compare checked facts with older fields, recording source/date. Preserve relationship stage, original notes and earlier company associations unless correcting them. A new employer can add an association without erasing history. Refreshing a profile does not imply outreach occurred.

## Log a conversation

Use the user's account or conversation evidence. Append a native dated toggle in the existing People page with date/channel/topic, substance, agreements and a due date only when agreed. Use the connector's supported block format; the [template](../../templates/person-page.md) is a readable representation, not an API payload.

On retry, find the same event and correct it rather than append a duplicate. Current next action/date live in People properties for sorting; older commitments remain in their toggles. Keep unsent text under Draft. Sent, Replied and Met need actual event evidence. No separate Interaction database is needed.

## Output and example

For discovery, return shortlist + identity/connection sources + uncertainties + useful question. For updates, return changed facts + preserved history + next action + write/readback result. An unverified match does not justify creating a speculative person record.

The [fictional People page](../../examples/fictional-case/outputs/people-page.md) contains two conversations, one current next action and an unsent draft. Shared professional-community membership is established by a synthetic profile source. Searching, refreshing or drafting never authorizes sending, introducing or requesting a referral on the user's behalf.
