# Alert Dialog

**Level:** Organism  
**Category:** Overlay

A modal overlay that interrupts the user with a critical message requiring an explicit decision before they can continue.

## When to use
- Confirming permanent deletions (files, accounts, data)
- Irreversible actions like publishing or sending
- Before actions with significant side effects (e.g., 'This will notify all users')
- Security-sensitive operations (revoke access, reset passwords)
- When the user must acknowledge a blocking error or warning

## When to avoid
- For routine or easily reversible actions — this creates dialog fatigue
- When a simple toast confirmation is sufficient
- As a pattern for collecting form input — use a Dialog instead
- For informational messages that don't require a decision — use an Alert
- Too frequently — each use should feel genuinely important

## States
- **Open** — Dialog is visible and blocking — overlay is active, focus is trapped inside.
- **Confirming** — The confirm button is in a loading state while the destructive action processes.
- **Closed** — Dialog is hidden; no DOM presence unless using a portal.
- **Confirm disabled** — The confirm action is disabled until the user performs a required step, such as typing a name.
- **Error** — The action failed; an inline error message is shown within the dialog.

## Related
[Dialog](dialog.md), [Alert](alert.md), [Sheet](sheet.md)

Source: [UX Components](https://www.ux-components.com/components/alert-dialog)
