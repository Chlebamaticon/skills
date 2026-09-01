# Scroll Area

**Level:** Molecule  
**Category:** Layout

A container with custom-styled scrollbars that overflows content within constrained dimensions.

## When to use
- Sidebars and navigation panels
- Fixed-height content containers (code blocks, chat windows)
- Data tables with many rows in a bounded area
- Modals and drawers with long content
- When the default browser scrollbar breaks your visual design

## When to avoid
- Hiding scrollbars entirely on touch devices — always indicate scrollability
- Wrapping the entire page — use native scroll for full-page layouts
- When content fits without overflow — the component adds unnecessary overhead
- Ultra-thin scrollbars that users can't see or target
- When scroll position state must be controlled externally without the proper API

## States
- **Idle** — Content fits or the user is not scrolling — scrollbar may be hidden or faint.
- **Scrolling** — The user is actively scrolling — the custom scrollbar thumb is visible and moving.
- **Scrollbar hover** — The pointer is over the scrollbar thumb — it may expand or highlight for easier grabbing.
- **Scrollbar dragging** — The user is dragging the scrollbar thumb to a new position.
- **At boundary** — The scroll position is at the top or bottom; further scrolling in that direction is not possible.

## Related
[Table](table.md), [Sheet](sheet.md)

Source: [UX Components](https://www.ux-components.com/components/scroll-area)
