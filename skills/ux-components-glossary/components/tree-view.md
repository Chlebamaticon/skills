# Tree View

**Level:** Organism  
**Category:** Data Display

A hierarchical display of nested data using expandable and collapsible parent-child nodes.

## When to use
- File system or folder browsers
- Nested navigation menus (e.g., documentation sidebars)
- Organizational charts or category hierarchies
- Permission or role management with nested groups
- Component or module dependency trees

## When to avoid
- Flat lists with no nesting — use a List instead
- When the hierarchy is only two levels deep — use an Accordion or grouped list
- On mobile where deep nesting creates usability issues
- When users need to compare items across branches simultaneously

## States
- **Collapsed** — Branch children are hidden; expand icon points right.
- **Expanded** — Branch children are visible; expand icon points down.
- **Selected** — A node is highlighted as the current selection.
- **Focused** — A node has keyboard focus with a visible ring.
- **Disabled** — A node is non-interactive and visually dimmed.
- **Loading** — Children are being fetched asynchronously.

## Related
[Accordion](accordion.md), [Navigation Menu](navigation-menu.md), [List](list.md)

Source: [UX Components](https://www.ux-components.com/components/tree-view)
