# Date Picker

**Level:** Molecule  
**Category:** Form

A specialized input that allows users to select a date from a calendar dropdown.

## When to use
- Booking and reservation forms
- Event creation with specific dates
- Filter controls for date ranges
- Birth date and age-gated fields
- Scheduling and deadline selection

## When to avoid
- When only a relative date matters (e.g., 'last 7 days') — use a select or radio group
- For time-only input — use a Time Picker instead
- When the date range is extremely narrow — a simple select may be easier
- For free-form text entry where dates are optional context

## States
- **Default** — Empty or pre-filled input, calendar closed.
- **Open** — Calendar popup is visible and user can select a date.
- **Hover (day)** — A day cell is highlighted on mouse hover.
- **Selected** — The chosen date is visually marked in the calendar and shown in the input.
- **Disabled** — The input and calendar trigger are non-interactive.
- **Error** — An invalid date has been entered, with validation message shown.
- **Range** — Two dates selected to define a start and end range.

## Related
[Calendar](calendar.md), [Input](input.md), [Time Picker](time-picker.md), [Popover](popover.md)

Source: [UX Components](https://www.ux-components.com/components/date-picker)
