# Treegrid

**Level:** Unclassified  
**Category:** Data Display

A tabular grid whose rows can be expanded and collapsed to reveal nested child rows — combining the columns of a table with the hierarchy of a tree.

## When to use
- Code coverage reports where files roll up into folders into repos
- File system browsers with metadata columns (size, modified, owner)
- Project trackers with parent epics and child tasks in a single table
- Comment threads with expandable replies plus author/time columns
- Org charts that show role, team, and headcount per row

## When to avoid
- Flat tabular data with no hierarchy — use a Data Table instead
- Single-column hierarchical data — use a Tree View instead
- When users need to globally sort columns — sorting collapses or disturbs the tree structure
- On mobile, where the combined grid + tree becomes too dense to read or interact with

## States
- **Collapsed** — A parent row is showing only itself; child rows are hidden.
- **Expanded** — A parent row is showing its children indented underneath.
- **Selected** — A row is highlighted as the active selection.
- **Focused** — A cell or row has keyboard focus with a visible ring.
- **Sorted** — A column header indicates the current sort order.
- **Loading** — Child rows are being fetched asynchronously after expansion.
- **Disabled** — A row is non-interactive and visually dimmed.

## Related
[Tree View](tree-view.md), [Data Table](data-table.md), [Table](table.md)

Source: [UX Components](https://www.ux-components.com/components/treegrid)
