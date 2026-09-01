# Input

**Level:** Atom  
**Category:** Form

A single-line text field that accepts typed user input.

## When to use
- Any form field requiring typed text (name, email, search, URL)
- Search bars
- Inline editing of names or titles
- Single-line settings fields (API keys, webhook URLs)
- Number, date, or password inputs with appropriate type attribute

## When to avoid
- For multi-line content — use Textarea instead
- When a predefined set of options exists — use Select or Combobox
- Placeholder text as a substitute for a label — it disappears on typing
- More fields than necessary — each field adds cognitive load
- Unmasked password fields without a visibility toggle

## States
- **Default** — The field is empty and ready for input.
- **Focused** — The field has focus — a highlighted border or ring signals it is active.
- **Filled** — The user has entered a value — the content is visible in the field.
- **Disabled** — The field is non-interactive — greyed out, cannot be edited.
- **Read-only** — The value is displayed but cannot be changed by the user.
- **Error** — Validation has failed — the border turns red and an error message appears below.

## Anatomy
- **Label** — Describes the expected input. Always present, never replaced by placeholder alone.
- **Input field** — The text box where the user types.
- **Placeholder** — Example value shown when the field is empty — supplemental, not a label.
- **Hint text** — Format guidance or context below the field.
- **Error message** — Validation feedback shown when the field is invalid.

## Related
[Label](label.md), [Textarea](textarea.md), [Combobox](combobox.md)

Source: [UX Components](https://www.ux-components.com/components/input)
