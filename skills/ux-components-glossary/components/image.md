# Image

**Level:** Atom  
**Category:** Content

A component for displaying responsive, accessible images with optional captions and fallback states.

## When to use
- Product photos in e-commerce listings
- User-uploaded content in galleries
- Hero images and banners
- Thumbnails in cards and lists
- Avatar images with fallback initials

## When to avoid
- For decorative backgrounds — use CSS background-image
- For icons or simple graphics — use SVG or an Icon component
- When the image is purely ornamental — mark as role='presentation'
- For complex interactive media — use a Video or Carousel component

## States
- **Loading** — Image is being fetched; a placeholder or skeleton is shown.
- **Loaded** — Image has fully rendered.
- **Error** — Image failed to load; fallback content is displayed.
- **Lazy** — Image is below the fold and will load when scrolled into view.

## Related
[Avatar](avatar.md), [Card](card.md), [Carousel](carousel.md)

Source: [UX Components](https://www.ux-components.com/components/image)
