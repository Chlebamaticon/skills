# Label

**Level:** Atom  
**Category:** Form

A text element that identifies and describes a form control for both sighted users and assistive technology.

## When to use
- Every form input, select, textarea, checkbox, and radio button
- Expanding clickable area for checkboxes and radio buttons
- Providing accessible names for custom form controls
- Always — there are almost no exceptions

## When to avoid
- Using placeholder text as the only label — it disappears and has low contrast
- Positioning labels far from their associated control
- Abbreviating label text to save space — clarity wins over brevity
- Using aria-label as a complete substitute when visible labels are possible
- Labels that don't accurately describe what the field expects

## States
- **Default** — The label is displayed next to or above its associated control.
- **Required** — An asterisk or 'Required' indicator is shown when the associated field is mandatory.
- **Optional** — An '(optional)' note is shown when most fields are required and this one is not.
- **Disabled** — The label appears muted when its associated control is disabled.
- **Error** — The label may be highlighted in an error color when its associated field has a validation error.

## Related
[Input](input.md), [Checkbox](checkbox.md), [Radio Group](radio-group.md)

Source: [UX Components](https://www.ux-components.com/components/label)
