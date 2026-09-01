# Window Splitter

**Level:** Unclassified  
**Category:** Layout

A draggable bar between two adjacent panels that lets users resize them by clicking and dragging.

## When to use
- Code editors with resizable sidebar, terminal, and file explorer panes
- Email clients with a list / preview layout the user can adjust
- Admin tools with master-detail panes where the detail width matters
- Documentation sites with toggleable nav width
- Chat apps with resizable conversation lists

## When to avoid
- Layouts where panels should always be a fixed ratio — use grid columns instead
- Touch-first surfaces — small drag handles are hard to grab on mobile
- When one panel should be optional and hidden entirely — use a Sheet or Collapsible Panel instead
- When the layout never needs to change after initial render — drag affordance becomes noise

## States
- **Default** — Bar is at rest between the two panels.
- **Hover** — Cursor changes to a resize indicator on the bar.
- **Dragging** — User is actively resizing — panels update in real time.
- **Focused** — Bar has keyboard focus; arrow keys nudge the size.
- **Collapsed** — One panel has been resized to its minimum or hidden state.
- **Disabled** — Resizing is locked and the cursor does not change.

## Related
[Scroll Area](scroll-area.md), [Sheet](sheet.md), [Separator](separator.md)

Source: [UX Components](https://www.ux-components.com/components/window-splitter)
