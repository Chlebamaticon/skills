# Color Picker

**Level:** Atom  
**Category:** Form

A specialized input that lets users select a color value from a spectrum, swatches, or by entering a hex/RGB code.

## When to use
- Theme customization interfaces
- Design tools and editors
- Branding and style configuration panels
- Chart or data visualization color assignment
- Personalization settings (profile colors, highlights)

## When to avoid
- When only a few predefined colors are available — use a Select or Radio Group with swatches
- For non-visual contexts where color has no meaning
- On mobile where precision picking is difficult — provide presets
- When accessibility is critical and color alone conveys meaning

## States
- **Default** — Displays the current color swatch and value.
- **Open** — The full color picker panel is visible.
- **Hover** — A preset swatch or slider thumb is highlighted.
- **Selected** — A color has been picked and shown in the swatch.
- **Disabled** — The picker is non-interactive.

## Related
[Input](input.md), [Slider](slider.md), [Popover](popover.md), [Select](select.md)

Source: [UX Components](https://www.ux-components.com/components/color-picker)
