# Number Input

**Level:** Atom  
**Category:** Form

A text field restricted to numeric values with optional increment and decrement controls.

## When to use
- Quantity selectors in e-commerce carts
- Setting numeric thresholds or limits
- Adjusting counts, amounts, or quantities
- Form fields requiring precise numeric values
- Configuration panels with numeric parameters

## When to avoid
- When the valid range is very large — use a plain text input with validation
- For approximate values — use a Slider instead
- When the number represents a date, phone, or card — use a masked input
- For binary on/off — use a Switch or Toggle

## States
- **Default** — Displays the current numeric value.
- **Focused** — The input has keyboard focus for direct typing.
- **Hover** — Increment or decrement button is highlighted.
- **Disabled** — The input and buttons are non-interactive.
- **Min Reached** — The decrement button is disabled at minimum value.
- **Max Reached** — The increment button is disabled at maximum value.
- **Error** — An out-of-range or invalid value is entered.

## Related
[Input](input.md), [Slider](slider.md), [Select](select.md)

Source: [UX Components](https://www.ux-components.com/components/number-input)
