# Dropdown Menu

**Level:** Organism  
**Category:** Navigation

A toggleable overlay that displays a list of actions or navigation options when triggered by a button or link.

## When to use
- Actions menu on rows in a data table (edit, duplicate, delete)
- User account menu in a navigation header
- More options menus (...) on cards or items
- Grouped navigation links for a section of a site
- Sort/filter controls with multiple options

## When to avoid
- When there are only 1–2 actions — show them directly as buttons
- For form option selection — use a Select or Combobox instead
- Nesting more than 2 levels of sub-menus — extremely hard to navigate
- For navigation menus with 10+ items — consider a dedicated nav component
- When actions are context-dependent on a right-click — use Context Menu

## States
- **Closed** — The menu is hidden; only the trigger element is visible.
- **Open** — The floating menu panel is displayed, anchored below the trigger.
- **Item hover** — A menu item is highlighted as the pointer moves over it.
- **Item focused** — A menu item has keyboard focus during keyboard navigation.
- **Item disabled** — An item is visible but non-interactive — shown in a muted style.
- **Sub-menu open** — A child menu has expanded to the side from a parent item.

## Related
[Context Menu](context-menu.md), [Select](select.md), [Combobox](combobox.md)

Source: [UX Components](https://www.ux-components.com/components/dropdown-menu)
