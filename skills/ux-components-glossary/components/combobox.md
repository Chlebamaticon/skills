# Combobox

**Level:** Molecule  
**Category:** Form

A composite control combining a text input with a dropdown list, allowing the user to filter and select from available options.

## When to use
- Country, timezone, or language selectors with 50+ options
- Tagging interfaces where users search existing tags
- Assigning from large user lists in collaboration tools
- Search-ahead fields for products, locations, or categories
- When options are fetched async based on typed input

## When to avoid
- Short lists of fewer than 8 options — use a Select instead
- When users always know exactly what to type — a plain Input is simpler
- Without an empty state — users need feedback when nothing matches
- For multi-select with many items — consider a dedicated multi-select or tag input
- On mobile where virtual keyboards make typing cumbersome

## States
- **Default** — The input shows the placeholder or current value; the dropdown is hidden.
- **Focused / Open** — The dropdown opens and the full list is shown, ready for filtering.
- **Typing** — The list filters in real time as the user types a query.
- **Loading** — Async options are being fetched — a spinner is shown inside the dropdown.
- **Empty** — No options match the query — an informative empty state message is displayed.
- **Selected** — A value has been chosen — it appears in the input field and the dropdown closes.

## Related
[Select](select.md), [Input](input.md), [Dropdown Menu](dropdown-menu.md)

Source: [UX Components](https://www.ux-components.com/components/combobox)
