# Switch

**Level:** Atom  
**Category:** Form

A toggle control for instantly switching between two mutually exclusive states.

## When to use
- Immediately-applied settings (dark mode, notifications, visibility)
- Feature toggles in admin or settings panels
- Any binary preference with instant effect
- Enabling/disabling a specific feature or integration
- Simple yes/no configuration options

## When to avoid
- When the change requires confirmation before applying — use a checkbox + save
- For multi-value selections — use Radio or Select
- Form fields that are submitted together — use Checkbox instead
- Without a label — the state alone doesn't communicate what's being toggled
- When the on/off labels alone don't make the action clear

## States
- **Off** — The switch is in the inactive state — the thumb is on the left and the track is grey.
- **On** — The switch is active — the thumb is on the right and the track is highlighted (e.g., white or green).
- **Focused** — The switch has keyboard focus — a visible focus ring surrounds the control.
- **Disabled off** — The setting is off and cannot be changed — greyed out.
- **Disabled on** — The setting is on and locked — the on state is visible but non-interactive.
- **Loading** — The toggle action is being processed — a spinner may appear inside the thumb.

## Related
[Checkbox](checkbox.md), [Toggle](toggle.md), [Radio Group](radio-group.md)

Source: [UX Components](https://www.ux-components.com/components/switch)
