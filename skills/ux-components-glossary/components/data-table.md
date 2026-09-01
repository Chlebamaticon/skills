# Data Table

**Level:** Organism  
**Category:** Data Display

A feature-rich table with sorting, filtering, pagination, and row selection for complex datasets.

## When to use
- Admin dashboards with user, order, or product lists
- Analytics and reporting interfaces
- CRM and ERP record management
- Log viewers and audit trails
- Any dataset requiring sort, filter, and bulk actions

## When to avoid
- Simple, small datasets with no interactivity — use a basic Table
- When data is better represented visually — use charts or cards
- On mobile when the table has many columns — consider a card-based list view
- For layout purposes — use CSS grid or flexbox instead

## States
- **Default** — Table displaying data with default sort order.
- **Sorted** — A column is sorted ascending or descending.
- **Filtered** — Active filters reduce the visible row set.
- **Row Selected** — One or more rows are checked for bulk actions.
- **Loading** — Data is being fetched; skeleton rows or spinner shown.
- **Empty** — No data matches the current filters.
- **Error** — Data failed to load with a retry option.

## Related
[Table](table.md), [Pagination](pagination.md), [Checkbox](checkbox.md), [Search](search.md)

Source: [UX Components](https://www.ux-components.com/components/data-table)
