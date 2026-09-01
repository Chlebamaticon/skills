# Skeleton

**Level:** Atom  
**Category:** Feedback

A placeholder that mimics the shape and layout of content while it is loading.

## When to use
- Page initial loads with substantial content (feeds, dashboards)
- Image and card grids where layout is known in advance
- Table rows loading from an API
- User-generated content like comments and profiles
- Any load over 300ms where a spinner would feel too open-ended

## When to avoid
- For very fast operations (under 300ms) — the skeleton flash is distracting
- When the final layout is unknown — generic skeletons create confusion
- As a persistent state — if data never loads, show an error
- For small inline elements like buttons or badges
- When a spinner or empty state communicates loading more clearly

## States
- **Loading** — The shimmer animation is running — content is being fetched.
- **Loaded** — Data has arrived — the skeleton is replaced by the real content.
- **Error** — Loading failed — the skeleton is replaced by an error state or empty state message.

## Related
[Progress](progress.md), [Card](card.md), [Avatar](avatar.md)

Source: [UX Components](https://www.ux-components.com/components/skeleton)
