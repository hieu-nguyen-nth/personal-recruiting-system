# Create and prove the schedule

Use a cloud execution environment if the workflow must run while your computer is off. Check that the exact account/chat exposes both the required connectors and scheduling. Local Codex automations need the local environment and do not satisfy that requirement by themselves. Official guidance: [scheduled tasks](https://learn.chatgpt.com/docs/automations) and [setup walkthrough](https://developers.openai.com/training/walkthroughs/scheduled-tasks).

1. Connect the job source and Notion in the intended cloud chat, and make the private methods and candidate reference readable there. Test one full JD read and a marked Notion test-page write interactively. Record actual errors and approval requirements.
2. From that chat, ask the scheduler to **create one one-time task** using [the smoke-test prompt](../prompts/scheduled-smoke-test.md), with a concrete future time and time zone. Inspect the returned schedule card/task entry. Record its actual URL/identifier and displayed run time in the private setup note.
3. Let that actual task run while the computer is asleep. Inspect scheduler history and the specific Notion writeback. A successful interactive test, task creation confirmation or generated report text alone is insufficient proof.
4. If it succeeds, create **one recurring cloud task** using [the daily prompt](../prompts/daily-scan.md) and your chosen cadence/time zone. Record the real task URL and next run. Check its first actual execution and ensure the one-time test is completed/inactive.
5. In Scheduled, inspect the run details, edit timing or pause/delete the task as needed. Keep only the intended recurrence. Recheck access after changing connectors or private references.

If cloud scheduling or unattended connector writes are unavailable, leave the schedule Not created/Blocked and name the missing capability. Do not quietly substitute a local task or a reminder that merely asks the user to do the work. Add custom infrastructure only after the limitation and tradeoff are understood.
