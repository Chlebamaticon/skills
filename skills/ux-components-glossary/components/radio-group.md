# Radio Group

**Level:** Atom  
**Category:** Form

A set of mutually exclusive options where selecting one deselects the others.

## When to use
- Mutually exclusive choices with 2–5 options
- Settings like 'Notification preference: Immediate / Daily / Weekly'
- Subscription or pricing tier selection
- Survey questions with one valid answer
- When users benefit from seeing all options at once

## When to avoid
- More than 5–6 options — use a Select instead
- When multiple selections are valid — use Checkboxes
- For a simple on/off toggle — use a Switch
- Long descriptions per option — consider cards or a different selection pattern
- Defaulting to no selection when a sensible default exists — always pre-select one

## States
- **Unselected** — The option is not chosen — an empty circle is displayed.
- **Selected** — The option is chosen — a filled dot appears inside the circle.
- **Focused** — The radio control has keyboard focus — a focus ring is shown.
- **Disabled unselected** — The option is shown but cannot be selected — greyed out.
- **Disabled selected** — The option is selected but cannot be changed — a locked state.
- **Error** — The group has a validation error — a message is shown and the group is highlighted.

## Related
[Checkbox](checkbox.md), [Switch](switch.md), [Select](select.md)

Source: [UX Components](https://www.ux-components.com/components/radio-group)
