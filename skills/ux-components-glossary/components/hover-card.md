# Hover Card

**Level:** Molecule  
**Category:** Overlay

A popover that appears on hover over a trigger, used to preview supplementary information.

## When to use
- User mentions in comments — show name, avatar, and role
- Link previews in documents or feeds
- Item references in a project management tool
- Stock or asset tickers with a quick price chart
- Tooltip replacements when more content context is needed

## When to avoid
- On touch devices — hover doesn't exist on mobile
- For critical information — users may never hover
- When the content requires user interaction — use a Popover instead
- For error messages or validation feedback — use inline messages
- If the hover area is very small — users can't reliably trigger it

## States
- **Hidden** — Default state — the card is not visible.
- **Delayed open** — The pointer has entered the trigger; the open delay timer is running (300–500ms).
- **Open** — The card is fully visible and anchored near the trigger.
- **Closing** — Pointer has left both the trigger and card — a brief grace period before hiding.

## Related
[Tooltip](tooltip.md), [Popover](popover.md), [Avatar](avatar.md)

Source: [UX Components](https://www.ux-components.com/components/hover-card)
