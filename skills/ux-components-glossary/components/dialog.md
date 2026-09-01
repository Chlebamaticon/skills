# Dialog

**Level:** Organism  
**Category:** Overlay

A modal window that appears over the main content to present information or collect input.

## When to use
- Create or edit forms that shouldn't leave the current page context
- Viewing expanded details from a list or card
- Multi-step wizards with limited steps (2–3)
- Quick actions like sharing, inviting, or configuring an item
- Media lightboxes or enlarged previews

## When to avoid
- Complex, long forms — they're better as dedicated pages
- When no user action is required — use a Drawer or Sheet
- Nesting dialogs inside dialogs — deeply confusing UX
- Full-page content — the modal should complement, not replace the page
- Auto-opening dialogs without a clear user trigger

## States
- **Closed** — The dialog is hidden and not rendered in the DOM (or hidden via aria-hidden).
- **Open** — The dialog is visible; backdrop is active and focus is trapped inside.
- **Submitting** — The primary action is in progress — confirm button is loading, form is non-interactive.
- **Error** — An inline error is displayed within the dialog body after a failed operation.
- **Scroll locked** — The page body scroll is locked while the dialog is open to prevent background scrolling.

## Related
[Alert Dialog](alert-dialog.md), [Sheet](sheet.md), [Popover](popover.md)

Source: [UX Components](https://www.ux-components.com/components/dialog)
