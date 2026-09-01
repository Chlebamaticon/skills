# Rating

**Level:** Atom  
**Category:** Form

An interactive or read-only star-based control for providing or displaying a score.

## When to use
- Product and service reviews
- Customer satisfaction and feedback surveys
- Content quality ratings (articles, recipes, media)
- Skill or difficulty level indicators
- Quick sentiment capture in forms

## When to avoid
- When you need precise numeric input — use a Slider or Input instead
- For binary feedback — use a Switch or thumb up/down buttons
- When the scale has more than 10 points — the visual becomes cluttered
- For ranked ordering of multiple items — use a sortable list instead
- When ratings aren't actionable — showing them without context adds noise

## States
- **Empty** — No value selected — all icons are unfilled.
- **Hover** — Icons fill up to the hovered position, previewing the potential value.
- **Selected** — A value has been chosen; icons are filled to that point.
- **Half Value** — Supports half-increments for finer-grained scoring.
- **Read-only** — Displays a score without allowing interaction.
- **Disabled** — Non-interactive; visually muted.

## Related
[Slider](slider.md), [Input](input.md), [Toggle](toggle.md)

Source: [UX Components](https://www.ux-components.com/components/rating)
