# Calendar

**Level:** Organism  
**Category:** Form

A visual date grid that displays a month at a time, allowing users to view and select dates.

## When to use
- Booking and scheduling flows
- Date range selection (hotel stays, report periods)
- Inline date pickers on forms where dates are a primary field
- Event calendars and availability views
- Any context where the user benefits from visualizing the full month

## When to avoid
- When users know the exact date — a plain text input is faster
- For dates far in the future or past — add a year picker or direct input
- For time selection — that requires a separate Time Picker
- On very small screens without a proper responsive layout
- When only the month and year matter — use simpler select dropdowns

## States
- **Default** — Month grid is displayed; no date is selected.
- **Selected** — A single day cell is highlighted as the chosen date.
- **Range start / end** — In range-selection mode, the start and end dates are highlighted with distinct markers.
- **In range** — Days between start and end are highlighted with a continuous fill.
- **Today** — The current calendar date is visually marked, independent of selection.
- **Disabled** — Dates outside the allowed range are visually muted and non-interactive.

## Related
[Input](input.md), [Select](select.md), [Popover](popover.md)

Source: [UX Components](https://www.ux-components.com/components/calendar)
