# Popover

**Level:** Molecule  
**Category:** Overlay

A non-modal floating panel anchored to a trigger element for supplementary content.

## When to use
- Color pickers, date pickers, and emoji selectors
- Contextual filters or sorting controls
- Inline editing of a field without leaving the page
- 'Add tag' or 'assign member' flows
- Help text or onboarding tips with interactive content

## When to avoid
- When the content is simple text — use a Tooltip instead
- For critical flows requiring focused attention — use a Dialog
- When nested deeply — popovers inside popovers are disorienting
- On small screens where the panel may overlap content unexpectedly
- When the action has irreversible consequences — require explicit confirmation

## States
- **Closed** — The popover is hidden; only the trigger is visible.
- **Open** — The floating panel is visible and anchored to its trigger.
- **Repositioned** — Automatic collision detection has flipped the popover to the opposite side to stay within the viewport.
- **Focused within** — A form element or interactive item inside the popover has focus.
- **Closing** — A click outside or Escape key has triggered dismissal; the panel may animate out.

## Related
[Tooltip](tooltip.md), [Hover Card](hover-card.md), [Dialog](dialog.md)

Source: [UX Components](https://www.ux-components.com/components/popover)
