# Tabs

**Level:** Molecule  
**Category:** Navigation

A set of layered content panels, only one visible at a time, switched via labeled triggers.

## When to use
- Switching between related views (Overview / Analytics / Settings)
- Product pages with multiple content types (Description / Reviews / Specs)
- Profile pages with different data sections
- Code editors (Edit / Preview / Split)
- Dashboard sections where only one view is needed at a time

## When to avoid
- When users need to compare content across tabs — the toggling defeats comparison
- More than 5–7 tabs — navigation becomes unwieldy; consider a sidebar
- Sequential steps in a workflow — use a Stepper instead
- Content that's independent rather than parallel alternatives
- Nesting tabs inside tabs — deeply confusing spatial model

## States
- **Active** — The selected tab — its panel is visible and the trigger has an active indicator.
- **Inactive** — Non-selected tabs — their panels are hidden.
- **Hover** — The pointer is over a tab trigger — a subtle color shift signals interactivity.
- **Focused** — A tab trigger has keyboard focus — a visible focus ring is shown.
- **Disabled** — A tab is visible but cannot be selected — shown in a muted style.

## Related
[Accordion](accordion.md), [Collapsible](collapsible.md), [Separator](separator.md)

Source: [UX Components](https://www.ux-components.com/components/tabs)
