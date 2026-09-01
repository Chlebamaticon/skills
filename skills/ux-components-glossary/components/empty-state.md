# Empty

**Level:** Unclassified  
**Category:** Feedback

A placeholder UI shown when there is no content to display in a given area.

## When to use
- When a list, table, or grid has no items to display
- After a search or filter returns zero results
- First-time user experiences before any data exists
- Error states where content failed to load
- When a feature is not yet configured or enabled

## When to avoid
- When data is loading — use Skeleton or Spinner instead
- For temporary states that resolve in seconds
- When content exists but is hidden by filters — show a filter-specific message
- As a permanent landing page — it should be a transitional state
- With overly complex illustrations that distract from the action

## States
- **No Data** — The collection is genuinely empty — no items exist yet.
- **No Results** — A search or filter returned nothing — suggest clearing filters.
- **Error** — Content failed to load — offer a retry action.
- **First Use** — The user hasn't created anything yet — guide them to start.

## Related
[Skeleton](skeleton.md), [Spinner](spinner.md), [Card](card.md)

Source: [UX Components](https://www.ux-components.com/components/empty-state)
