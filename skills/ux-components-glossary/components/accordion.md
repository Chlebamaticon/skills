# Accordion

**Level:** Molecule  
**Category:** Disclosure

A vertically stacked set of interactive headings, each revealing or hiding a section of content when clicked.

## When to use
- FAQ sections where users scan for specific questions
- Settings panels with many grouped options
- Sidebar navigation with nested sub-items
- Product detail pages (specs, shipping, returns)
- Mobile layouts where vertical space is limited

## When to avoid
- When users need to see all content simultaneously for comparison
- For critical information that must always be visible
- When there are only 1–2 items — just show the content directly
- When the content inside is very short — the toggle overhead isn't worth it
- Complex multi-step forms where context from previous steps matters

## States
- **Collapsed** — The default state — only the trigger is visible, content is hidden.
- **Expanded** — Content panel is fully visible and the indicator (chevron) is rotated.
- **Focused** — The trigger has keyboard focus — a visible focus ring is shown.
- **Disabled** — The trigger is non-interactive; toggling is prevented.
- **Loading** — Content is being fetched asynchronously before it can be shown.

## Anatomy
- **Container** — Wraps all items and provides consistent visual grouping.
- **Trigger** — The clickable header that toggles the panel open or closed.
- **Indicator** — An icon (usually a chevron) that visually signals open/closed state.
- **Content Panel** — The revealed section containing the body content.

## Related
[Collapsible](collapsible.md), [Tabs](tabs.md), [Separator](separator.md)

Source: [UX Components](https://www.ux-components.com/components/accordion)
