# Toast

**Level:** Molecule  
**Category:** Feedback

A brief, auto-dismissing notification that appears to confirm an action or communicate a system event.

## When to use
- Confirming background saves or auto-saves
- Action results (item deleted, message sent, file uploaded)
- Non-critical error notifications that don't block the workflow
- Undo confirmations with a 5-second undo action
- System events outside of the user's current focus

## When to avoid
- Critical errors requiring user acknowledgment — use an Alert or Dialog
- Content the user needs to read in detail — it disappears too fast
- Stacking more than 3 toasts simultaneously — becomes noisy
- Toasting every single action — reserve for meaningful feedback
- Permanent notifications — toasts are for transient messages

## States
- **Entering** — The toast is animating in from the corner of the viewport.
- **Visible** — The toast is fully shown and the auto-dismiss timer is running.
- **Hovered / Paused** — The pointer is over the toast — the dismiss timer is paused.
- **Exiting** — The timer has expired or the user dismissed it — the toast is animating out.
- **Success** — A green icon and tone confirm a positive outcome.
- **Error** — A red icon indicates a failure or non-critical error.

## Related
[Alert](alert.md), [Dialog](dialog.md), [Progress](progress.md)

Source: [UX Components](https://www.ux-components.com/components/toast)
