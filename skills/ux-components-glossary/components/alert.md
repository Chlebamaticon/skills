# Alert

**Level:** Molecule  
**Category:** Feedback

A static, non-interactive message that communicates important information, feedback, or status to the user.

## When to use
- Form validation summaries at the top of a form
- System status messages (e.g., 'Maintenance scheduled for tonight')
- Permission or access warnings on restricted pages
- Successful completion of a background task the user initiated
- Contextual tips or informational notices within a workflow

## When to avoid
- For ephemeral confirmations — use a Toast instead
- When the message requires user input or a decision — use an Alert Dialog
- Stacking many alerts at once — prioritize the most critical one
- As a replacement for empty states or placeholder content
- For marketing or promotional messages

## States
- **Info** — Neutral informational message, typically blue — no urgency implied.
- **Success** — Confirms a positive outcome, typically green.
- **Warning** — Signals a potential issue that needs attention, typically yellow.
- **Error** — Indicates a failure or blocking condition, typically red.
- **Dismissible** — An optional close button allows the user to remove the alert from the page.

## Related
[Toast](toast.md), [Alert Dialog](alert-dialog.md), [Badge](badge.md)

Source: [UX Components](https://www.ux-components.com/components/alert)
