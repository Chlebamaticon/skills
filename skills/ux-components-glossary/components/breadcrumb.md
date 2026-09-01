# Breadcrumb

**Level:** Molecule  
**Category:** Navigation

A secondary navigation aid showing the user's current location within the site hierarchy.

## When to use
- Deep content hierarchies (e-commerce, docs, file systems)
- Administration dashboards with nested sections
- Content sites with categories and subcategories
- Any page more than 2 levels deep from the root
- When users navigate to pages from search or external links

## When to avoid
- Flat sites or apps with only 1–2 levels of hierarchy
- Single-page apps where all content is on one level
- As a replacement for primary navigation
- Mobile views where space is limited and the path is already clear
- When the current page's title alone provides sufficient orientation

## States
- **Default** — Ancestor items are displayed as clickable links.
- **Current page** — The last item is non-interactive and visually distinguished (often bolder or higher contrast).
- **Hover** — An ancestor link shows an underline or color change on hover.
- **Collapsed** — Intermediate items are hidden behind an ellipsis when the path is too long.
- **Focused** — A link in the breadcrumb has keyboard focus — visible focus ring is shown.

## Related
[Pagination](pagination.md), [Tabs](tabs.md)

Source: [UX Components](https://www.ux-components.com/components/breadcrumb)
