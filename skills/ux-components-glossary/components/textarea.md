# Textarea

**Level:** Atom  
**Category:** Form

A multi-line text input for longer-form content like comments or descriptions.

## When to use
- Comments and reply boxes
- Bio, description, or 'about me' fields
- Feedback forms and bug reports
- Message composition in chat or email-like interfaces
- Code input where a full code editor is overkill

## When to avoid
- For single-line content — use an Input instead
- When rich text formatting is needed — use a rich text editor
- Auto-sizing textarea to very tall heights without a max — disrupts layout
- For very structured data like addresses — use separate fields
- Without indicating expected length — height should hint at what you expect

## States
- **Default** — The field is empty and ready for input.
- **Focused** — The field is active — a highlighted border or ring signals it is ready for input.
- **Filled** — The user has entered text — content is visible and the field may have auto-expanded.
- **Disabled** — The field is non-interactive — greyed out, text cannot be entered.
- **Error** — Validation has failed — the border turns red and an error message appears below.
- **At limit** — The character count is at or near the maximum — the counter may change color to warn the user.

## Related
[Input](input.md), [Label](label.md)

Source: [UX Components](https://www.ux-components.com/components/textarea)
