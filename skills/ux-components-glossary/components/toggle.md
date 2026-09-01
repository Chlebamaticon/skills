# Toggle

**Level:** Atom  
**Category:** Action

A button that switches between two states (on/off, active/inactive) and visually reflects the current state.

## When to use
- Text formatting toolbars (Bold, Italic, Underline)
- View mode switchers (Grid / List)
- Filter chips that include/exclude a category
- Map layers or overlay visibility
- Mute/unmute and show/hide controls in media players

## When to avoid
- When the action isn't stateful — use a regular Button
- For settings outside an active UI context — use a Switch
- Without clear active/inactive visual differentiation
- More than 5–6 in a group — consider a different selection model
- For binary choices in forms — use a Switch or Checkbox

## States
- **Inactive** — The default state — the button is not pressed; background is transparent or minimal.
- **Active / Pressed** — The button is on — a filled background or distinct border signals the active state.
- **Hover (inactive)** — The pointer is over an inactive toggle — a subtle hover effect signals interactivity.
- **Hover (active)** — The pointer is over an active toggle — a hover effect suggests it can be deactivated.
- **Focused** — The toggle has keyboard focus — a visible focus ring is shown.
- **Disabled** — The toggle is non-interactive — its state is visible but cannot be changed.

## Related
[Switch](switch.md), [Button](button.md), [Toggle Group](toggle-group.md)

Source: [UX Components](https://www.ux-components.com/components/toggle)
