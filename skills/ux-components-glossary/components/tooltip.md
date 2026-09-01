# Tooltip

**Level:** Molecule  
**Category:** Overlay

A small, informational popup that appears on hover or focus to describe an element.

## When to use
- Icon-only buttons that need text labels (toolbar icons, icon buttons)
- Clarifying an abbreviated or truncated label
- Keyboard shortcut hints alongside menu items
- Explaining a disabled element and why it's disabled
- Expanding acronyms or technical terms

## When to avoid
- Interactive content — use a Popover for links, buttons, or forms
- Essential information — tooltips are hidden and keyboard-only users may miss them
- On touch-only devices where hover doesn't exist
- More than one short sentence — if it's longer, use a Popover or inline help
- Attaching to static text that isn't an interactive element

## States
- **Hidden** — Default state — tooltip is not visible.
- **Delayed open** — Hover or focus has started the open delay timer (400–600ms).
- **Visible** — Tooltip is fully shown near the trigger element.
- **Closing** — Hover or focus has ended — tooltip fades out immediately.

## Related
[Popover](popover.md), [Hover Card](hover-card.md), [Button](button.md)

Source: [UX Components](https://www.ux-components.com/components/tooltip)
