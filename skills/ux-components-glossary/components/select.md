# Select

**Level:** Molecule  
**Category:** Form

A dropdown control that lets the user choose one option from a predefined list.

## When to use
- Country, state, language, or timezone selection
- Category or type filters with fixed options
- Sort order (Newest first, Oldest first, A–Z)
- Form fields with 5–15 discrete options
- When all options are equally likely — no need for search

## When to avoid
- More than 15 options — use Combobox with search
- Only 2–3 options — use Radio Buttons for better scannability
- Multi-select — the native select's multi-select UX is poor; use a custom component
- Binary options like 'Yes/No' — use a Switch or Checkbox
- When users might not know the option name — use Combobox

## States
- **Default / closed** — Shows the selected value or placeholder; the dropdown is hidden.
- **Open** — The dropdown list is visible, with the current selection highlighted.
- **Option hover** — An option is highlighted as the pointer moves over it.
- **Option selected** — The chosen option is marked and reflected in the trigger.
- **Disabled** — The control is non-interactive — greyed out, cannot be opened.
- **Error** — Validation has failed — the trigger border turns red and an error message appears.

## Anatomy
- **Trigger** — The closed state showing the selected value.
- **Placeholder** — Text shown when no value is selected.
- **Dropdown panel** — The list of options, revealed on trigger click.
- **Option items** — Each selectable value, optionally grouped.

## Related
[Combobox](combobox.md), [Radio Group](radio-group.md), [Dropdown Menu](dropdown-menu.md)

Source: [UX Components](https://www.ux-components.com/components/select)
