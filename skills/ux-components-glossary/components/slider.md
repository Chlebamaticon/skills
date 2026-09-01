# Slider

**Level:** Atom  
**Category:** Form

A control for selecting a numeric value by dragging a thumb along a track.

## When to use
- Volume, brightness, or opacity controls
- Price range filters in e-commerce
- Image editing adjustments (contrast, saturation, etc.)
- Zoom level controls
- Settings where users benefit from seeing the full range visually

## When to avoid
- When precision matters — use an Input instead
- When the range is very large (e.g., 0–10,000) — the thumb movement becomes too imprecise
- For binary choices — use a Switch or Checkbox
- When there are only a few discrete options — use a Radio Group or Select
- On mobile when the drag target is too small to hit reliably

## States
- **Default** — Thumb rests at the initial value; track shows the filled and unfilled portions.
- **Hover** — Thumb enlarges or shows a value tooltip on mouse hover.
- **Active / Dragging** — Thumb is being dragged — value updates in real time.
- **Focused** — A visible focus ring on the thumb for keyboard users; arrow keys adjust the value.
- **Disabled** — Non-interactive; thumb and track are visually muted.
- **Range** — Two thumbs define a minimum and maximum selection within the track.

## Related
[Input](input.md), [Progress](progress.md), [Radio Group](radio-group.md)

Source: [UX Components](https://www.ux-components.com/components/slider)
