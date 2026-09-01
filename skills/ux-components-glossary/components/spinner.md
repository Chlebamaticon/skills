# Spinner

**Level:** Atom  
**Category:** Feedback

An animated loading indicator that signals an ongoing process with an indeterminate duration.

## When to use
- Button loading states after form submission
- Inline loading within cards or list items fetching data
- Page-level loading overlays during navigation
- Placeholder while asynchronous content is being fetched
- Pull-to-refresh indicators on mobile

## When to avoid
- When the duration is known — use a Progress bar instead
- For initial page loads — use a Skeleton screen for better perceived performance
- For very fast operations (under 300ms) — the spinner will just flash and distract
- Stacking multiple spinners on one page — consolidate into one loading state
- As the only feedback for critical actions — add a text status message too

## States
- **Spinning** — The default animated state indicating loading is in progress.
- **With Label** — A text label accompanies the spinner for additional context.
- **Small / Inline** — Compact size used within buttons or inline with text.
- **Overlay** — Full-region or full-page overlay preventing interaction while loading.

## Related
[Progress](progress.md), [Skeleton](skeleton.md), [Button](button.md)

Source: [UX Components](https://www.ux-components.com/components/spinner)
