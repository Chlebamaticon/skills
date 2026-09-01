# Context Menu

**Level:** Organism  
**Category:** Navigation

A floating menu that appears on right-click, providing contextual actions related to the clicked element.

## When to use
- File or item management (rename, move, delete)
- Text editor actions (cut, copy, paste, format)
- Canvas or design tool operations
- Table row actions in data-heavy interfaces
- Supplementary power-user shortcuts in complex tools

## When to avoid
- As the only way to access critical actions — hidden menus exclude non-power users
- On touch-only devices where right-click isn't available
- For actions that belong in a primary toolbar or button
- Overloading with too many items — keep to 5–7 actions maximum
- Without keyboard accessibility — all items must be reachable by keyboard

## States
- **Hidden** — Default state — the menu is not rendered until triggered.
- **Open** — Menu is displayed at the pointer position after a right-click or long-press.
- **Item hover** — A menu item is highlighted as the pointer moves over it.
- **Item disabled** — An item is shown but non-interactive — greyed out with cursor: not-allowed.
- **Sub-menu open** — A nested sub-menu has expanded to the side from the highlighted item.

## Related
[Dropdown Menu](dropdown-menu.md), [Popover](popover.md), [Tooltip](tooltip.md)

Source: [UX Components](https://www.ux-components.com/components/context-menu)
