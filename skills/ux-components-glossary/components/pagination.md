# Pagination

**Level:** Molecule  
**Category:** Navigation

A control for navigating between pages of content in a dataset or list.

## When to use
- Large datasets like search results, product listings, or user tables
- When loading all results at once would harm performance
- When users need to reference a specific page (e.g., 'results were on page 3')
- Administration tables with many rows
- Content archives with discrete pages

## When to avoid
- When infinite scroll provides a better UX (social feeds, image galleries)
- Very small datasets (under 20 items) — just show everything
- When Load More is a better progressive pattern
- On mobile for data tables — consider a different layout
- Paginating static content on a single page — use anchored sections instead

## States
- **Default** — Non-active page buttons are shown at their resting style.
- **Active / Current** — The current page is visually highlighted — bold, filled, or contrasting.
- **Hover** — A page button shows a hover state as the pointer moves over it.
- **Disabled** — Previous is disabled on page 1; Next is disabled on the last page.
- **Ellipsis** — Skipped page ranges are represented by a non-interactive ellipsis item.

## Related
[Table](table.md), [Select](select.md)

Source: [UX Components](https://www.ux-components.com/components/pagination)
