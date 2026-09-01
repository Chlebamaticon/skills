# Table

**Level:** Organism  
**Category:** Data Display

A structured grid of rows and columns for displaying tabular data.

## When to use
- Administration panels with lists of users, orders, or records
- Data comparison (pricing plans, feature matrices)
- Logs, transactions, or audit trails
- Any dataset where column relationships matter
- Bulk operations with multi-row selection

## When to avoid
- Simple lists where only one column is meaningful — use a List
- Deeply hierarchical data — use a Tree or expandable accordion
- Mobile-first layouts where columns collapse awkwardly
- Displaying only 1–3 rows — a card list is more scannable
- Very wide tables without horizontal scroll handling

## States
- **Default** — Rows are displayed at rest with standard background and borders.
- **Row hover** — The pointer is over a row — a subtle background highlight aids scanning.
- **Row selected** — A row's checkbox is checked — it is highlighted for bulk action.
- **Sorted** — A column header has a sort indicator (arrow) showing the active sort direction.
- **Loading** — Skeleton rows are shown while data is being fetched.
- **Empty** — No rows match the current filter or the dataset is empty — an empty state is shown.

## Related
[Pagination](pagination.md), [Badge](badge.md), [Checkbox](checkbox.md)

Source: [UX Components](https://www.ux-components.com/components/table)
