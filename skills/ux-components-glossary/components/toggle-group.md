# Toggle Group

**Level:** Molecule  
**Category:** Action

A set of toggle buttons where selecting one option may deselect others.

## When to use
- View mode selectors (Day / Week / Month)
- Alignment controls (Left / Center / Right)
- Filter tag groups where multiple can be active
- Text formatting (bold + italic together)
- Size or variant selectors (S / M / L / XL)

## When to avoid
- When one option must always be selected — handle that logic explicitly
- Too many options — beyond 5–6 items, use a different control
- When labels need to be long — toggle labels should be 1–3 words
- For navigation — use Tabs instead
- Without a default selection when one is logically required

## States
- **One active (single)** — Single-select mode — one button is active and all others are inactive.
- **Multiple active (multi)** — Multi-select mode — several buttons are simultaneously active.
- **None active** — No button is selected — only valid when 'no selection' is an intentional option.
- **Item hover** — The pointer is over an item — a subtle hover style signals it is interactive.
- **Item focused** — An item has keyboard focus — a focus ring is shown.
- **Item disabled** — A specific item in the group is non-interactive — shown in a muted style.

## Related
[Toggle](toggle.md), [Tabs](tabs.md), [Radio Group](radio-group.md)

Source: [UX Components](https://www.ux-components.com/components/toggle-group)
