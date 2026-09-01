# Time Picker

**Level:** Molecule  
**Category:** Form

A specialized input for selecting a time value with hour, minute, and optional AM/PM controls.

## When to use
- Scheduling appointments and meetings
- Setting alarms or reminders
- Event creation with start and end times
- Business hours configuration
- Timer and countdown settings

## When to avoid
- When only a date is needed — use a Date Picker
- When time precision beyond minutes isn't needed and a dropdown of time slots works
- For duration input — consider separate hour/minute fields or a number input
- When the valid time range is very constrained — use a Select with predefined options

## States
- **Default** — Displays placeholder or current time value.
- **Open** — Time selection UI is visible.
- **Selected** — A time value has been chosen and displays in the input.
- **Focused** — Input has keyboard focus.
- **Disabled** — The picker is non-interactive.
- **Error** — An invalid time has been entered.

## Related
[Date Picker](date-picker.md), [Input](input.md), [Select](select.md)

Source: [UX Components](https://www.ux-components.com/components/time-picker)
