# Checkbox

**Level:** Atom  
**Category:** Form

A binary control that lets the user toggle an option on or off independently of other choices.

## When to use
- Multi-select options from a list (filter categories, permissions)
- Toggling a single boolean preference ('Enable notifications')
- Agreeing to terms or conditions
- Selecting items for a bulk action
- Indeterminate state for 'select all' with partial selection

## When to avoid
- When only one option can be selected — use Radio Buttons instead
- For mutually exclusive yes/no choices — use a Switch or Toggle
- Without a visible label — unlabeled checkboxes are inaccessible
- Long lists of 6+ options without search/filter — consider a different input
- For triggering immediate actions — checkboxes should capture state, not cause effects

## States
- **Unchecked** — The default state — the option is not selected.
- **Checked** — The option is selected — a checkmark is shown inside the box.
- **Indeterminate** — Some but not all children are selected — a dash is shown; used in select-all patterns.
- **Focused** — The checkbox has keyboard focus — a visible focus ring is shown.
- **Disabled** — The checkbox is non-interactive — greyed out, cannot be changed by the user.
- **Error** — Form validation has failed — the checkbox and label are highlighted with an error color.

## Related
[Radio Group](radio-group.md), [Switch](switch.md), [Label](label.md)

Source: [UX Components](https://www.ux-components.com/components/checkbox)
