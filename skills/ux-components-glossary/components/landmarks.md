# Landmark Regions

**Level:** Unclassified  
**Category:** Layout

Semantic HTML5 regions (header, nav, main, aside, footer, search) that let screen reader users jump between major sections of a page with a single keystroke.

## When to use
- Every public-facing page — landmarks are foundational accessibility, not optional
- Wrapping the primary content area in a main element
- Marking site navigation, page headers, and footers
- Distinguishing complementary sidebars from primary content
- Multi-region pages with distinct sections (article + related items)

## When to avoid
- Wrapping every div in a landmark — overuse defeats the purpose
- Using section without an accessible heading (aria-labelledby or visible label)
- Adding redundant ARIA roles when the matching HTML5 element exists
- Nesting multiple landmarks of the same type without distinguishing aria-labels

## States
- **Default** — Native HTML5 landmark element rendered with default semantics.
- **Labeled** — Landmark has an aria-label or aria-labelledby for screen reader disambiguation.
- **Multiple of same type** — Multiple landmarks of the same role (e.g., two navs) each have a distinct label.

## Related
[Navigation Menu](navigation-menu.md), [Form](form.md), [Menubar](menubar.md)

Source: [UX Components](https://www.ux-components.com/components/landmarks)
