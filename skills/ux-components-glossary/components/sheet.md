# Sheet

**Level:** Organism  
**Category:** Overlay

A panel that slides in from the edge of the screen, overlaying the main content.

## When to use
- Detail panels for list items (click a row, see full detail)
- Filter controls for large datasets
- Mobile navigation menus
- Cart or checkout side panels in e-commerce
- Settings or configuration panels that complement the main view

## When to avoid
- For simple confirmations — use an Alert Dialog
- Complex forms that deserve their own page
- On mobile for bottom sheets taller than 80% — users lose page context
- As a primary navigation pattern on desktop
- When the content has many sub-levels — the sheet gets too complex

## States
- **Closed** — The sheet is off-screen and not visible.
- **Opening** — The panel is animating in from the edge of the screen.
- **Open** — The panel is fully visible and interactive.
- **Scrolled** — Content inside the sheet body has been scrolled — a scroll indicator may appear.
- **Closing** — The panel is animating back off-screen after dismissal.

## Related
[Dialog](dialog.md), [Alert Dialog](alert-dialog.md), [Scroll Area](scroll-area.md)

Source: [UX Components](https://www.ux-components.com/components/sheet)
