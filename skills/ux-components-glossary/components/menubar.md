# Menubar

**Level:** Organism  
**Category:** Navigation

A horizontal bar of top-level menu items, each opening a dropdown of actions or sub-menus.

## When to use
- Desktop-class web applications (editors, IDEs, design tools)
- When the application has many commands that need organized access
- File management interfaces with CRUD operations
- When users expect traditional desktop menu behavior
- Applications where keyboard shortcut discoverability matters

## When to avoid
- For simple websites or content pages — use a Navigation Menu instead
- On mobile — the pattern doesn't translate well to touch interfaces
- When there are only 2–3 top-level actions — use Buttons or a Dropdown Menu
- For site-level navigation — use Tabs or a navigation bar
- When the application is task-focused with a limited action set

## States
- **Default** — All triggers are visible in the bar; no dropdown is open.
- **Open** — A trigger is active and its dropdown is displayed below.
- **Hover-follow** — While one menu is open, hovering adjacent triggers immediately opens their dropdowns.
- **Item Highlighted** — A menu item is highlighted via hover or keyboard navigation.
- **Submenu Open** — A nested submenu is visible, triggered by hovering a parent item with a chevron.
- **Disabled Item** — A menu item is visible but non-interactive, shown in muted text.

## Related
[Dropdown Menu](dropdown-menu.md), [Context Menu](context-menu.md), [Tabs](tabs.md)

Source: [UX Components](https://www.ux-components.com/components/menubar)
