# Progress

**Level:** Atom  
**Category:** Feedback

A visual indicator of completion percentage for a determinate task or process.

## When to use
- File upload and download progress
- Multi-step form or onboarding completion
- Profile completeness indicators
- Task or project completion status
- Loading a resource where progress can be measured

## When to avoid
- When duration is unknown — use a Spinner or skeleton instead
- For very fast operations (under 300ms) — the flash is disorienting
- When a simple percentage number suffices
- Animating fake progress on indeterminate tasks — erodes trust
- Multiple competing progress bars on a single screen

## States
- **Empty (0%)** — The fill is at zero — the process has not yet started.
- **In progress** — The fill spans a portion of the track, reflecting partial completion.
- **Complete (100%)** — The fill spans the full track — the process is finished.
- **Indeterminate** — An animated fill bounces back and forth to indicate an unknown duration.
- **Error** — The fill turns red to signal the process has failed.

## Related
[Skeleton](skeleton.md), [Toast](toast.md)

Source: [UX Components](https://www.ux-components.com/components/progress)
