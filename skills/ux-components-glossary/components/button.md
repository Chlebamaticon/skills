# Button

**Level:** Atom  
**Category:** Action

The primary mechanism for user-initiated actions.

## When to use
- Submitting forms
- Triggering dialogs, drawers, or modals
- Primary call-to-action on a page
- Confirming or canceling operations
- Any user-initiated action that causes a state change

## When to avoid
- For navigation to a new page — use a Link instead
- More than one primary button per section — dilutes the visual hierarchy
- Vague labels like 'Click here' or 'Submit' — be specific about what happens
- As a container for other interactive elements
- Disabled buttons without explanation of why and how to enable them

## States
- **Default** — The resting, interactive state of the button.
- **Hover** — Cursor is over the button — a subtle background or color shift signals interactivity.
- **Active / Pressed** — The button is being clicked or pressed — a deeper background or inset shadow provides tactile feedback.
- **Focused** — The button has keyboard focus — a visible focus ring is shown for accessibility.
- **Disabled** — The button is non-interactive — reduced opacity, cursor: not-allowed.
- **Loading** — An action is in progress — a spinner replaces or accompanies the label, and the button is non-interactive.

## Related
[Toggle](toggle.md), [Dropdown Menu](dropdown-menu.md), [Popover](popover.md)

Source: [UX Components](https://www.ux-components.com/components/button)
