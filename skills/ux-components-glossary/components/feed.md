# Feed

**Level:** Unclassified  
**Category:** Data Display

A scrollable list of articles or content items loaded incrementally as the user scrolls — with ARIA semantics that let screen readers navigate item-by-item without losing context.

## When to use
- Social media timelines and post streams
- News article streams with infinite or progressive loading
- Activity logs and audit trails that grow over time
- Search results that load more on scroll
- Notification or inbox streams

## When to avoid
- Short, fixed-length lists — use a List instead
- When users need to compare items globally — feeds break that mental model
- When pagination is more appropriate (e.g., reviewable historical records)
- When you can't track read position across sessions

## States
- **Initial loading** — First page of items is being fetched; show a skeleton or spinner.
- **Loaded** — Items are visible and interactive.
- **Loading more** — User scrolled near the end; next page is fetching.
- **End of feed** — No more items to load; show a terminal indicator.
- **Empty** — Feed has no items yet — show an empty state with onboarding.
- **Error** — A page failed to load; offer a retry control.

## Related
[List](list.md), [Timeline](timeline.md), [Card](card.md)

Source: [UX Components](https://www.ux-components.com/components/feed)
