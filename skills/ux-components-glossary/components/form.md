# Form

**Level:** Organism  
**Category:** Form

A container that groups related inputs, manages validation, and handles data submission.

## When to use
- User login and registration flows
- Checkout and payment forms
- Settings and profile editing pages
- Search filters and advanced search panels
- Multi-step wizards with per-step validation

## When to avoid
- For read-only data display — use a detail view or card
- When there is only one input — a standalone input with a button suffices
- For conversational data collection — consider a chat or wizard pattern
- When inputs are independent and don't submit together

## States
- **Default** — All fields are empty or pre-filled, ready for input.
- **Validating** — Inline validation is checking field values as the user types.
- **Error** — One or more fields have validation errors displayed.
- **Submitting** — The form is processing — submit button shows a loading state.
- **Submitted** — The form was successfully submitted — a success message is shown.
- **Disabled** — All fields and the submit button are non-interactive.

## Related
[Input](input.md), [Select](select.md), [Checkbox](checkbox.md), [Radio Group](radio-group.md), [Button](button.md)

Source: [UX Components](https://www.ux-components.com/components/form)
