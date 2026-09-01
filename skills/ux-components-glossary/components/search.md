# Search

**Level:** Unclassified  
**Category:** Form

A specialized text input optimized for search queries with optional typeahead and clear functionality.

## When to use
- Finding content across an application
- Filtering lists, tables, or catalogs
- Global search with keyboard shortcut activation
- Searching within a specific context like a dropdown or dialog
- Site-wide or documentation search

## When to avoid
- When there are fewer than 10 items — simple scanning is faster
- As the only way to navigate — always provide browse/filter alternatives
- When search terms are highly specialized — add guided filters instead
- Without clear result feedback — always indicate matches or empty state
- For structured data entry — use form inputs with validation

## States
- **Empty** — No query entered — shows placeholder text and search icon.
- **Focused** — Input is focused — ready for typing.
- **Active** — User is typing — may show live results.
- **Loading** — Results are being fetched.
- **Results** — Matching results are displayed.
- **No Results** — Query returned no matches.

## Related
[Input](input.md), [Combobox](combobox.md), [Dropdown Menu](dropdown-menu.md)

Source: [UX Components](https://www.ux-components.com/components/search)
