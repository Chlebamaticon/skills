# Collapsible

**Level:** Molecule  
**Category:** Disclosure

A primitive that toggles the visibility of a content section, without the stacked list structure of an Accordion.

## When to use
- Advanced options or secondary content that most users won't need
- Expanding a preview row in a table to show more details
- Read-more patterns on truncated descriptions
- Optional configuration panels in settings
- When you want disclosure without the structured list of Accordion

## When to avoid
- When multiple related sections need to collapse — use an Accordion instead
- For critical information that should always be visible
- When the revealed content is very short — just show it
- As a navigation mechanism — use a proper navigation component
- To hide error messages or important warnings

## States
- **Closed** — The default state — only the trigger is visible, content is hidden.
- **Open** — Content is fully visible; the trigger reflects the open state.
- **Focused** — The trigger has keyboard focus — a focus ring is visible.
- **Disabled** — The trigger is non-interactive; content cannot be toggled.

## Related
[Accordion](accordion.md), [Sheet](sheet.md), [Dialog](dialog.md)

Source: [UX Components](https://www.ux-components.com/components/collapsible)
