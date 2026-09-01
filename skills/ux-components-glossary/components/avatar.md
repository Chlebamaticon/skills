# Avatar

**Level:** Atom  
**Category:** Data Display

A visual representation of a user or entity, typically shown as a photo, initials, or a fallback icon.

## When to use
- User profiles in navigation headers or sidebars
- Comment threads and activity feeds
- Assignee or collaborator indicators on tasks
- Mention chips in rich text editors
- Team or member listing pages

## When to avoid
- When the identity isn't relevant to the context — decorative avatars add noise
- Without fallback handling — always define what happens when images fail
- Very small sizes for primary identification (under 20px becomes unrecognizable)
- As a substitute for a full user profile card when more info is needed
- Showing real photos without user consent or appropriate privacy handling

## States
- **Image loaded** — The profile photo is displayed successfully.
- **Fallback initials** — The image failed or wasn't provided — initials are shown instead.
- **Fallback icon** — No name or image is available; a generic person icon is displayed.
- **Loading** — Image is being fetched — a placeholder or shimmer is shown.
- **Group / stacked** — Multiple avatars overlap in a cluster, with a count badge for overflow.
- **With indicator** — A small status dot (green for online, grey for offline) is overlaid on the avatar.

## Anatomy
- **Image** — The primary display — a profile photo or custom image.
- **Fallback** — Initials or icon shown when the image fails to load or isn't provided.
- **Size variants** — sm / md / lg sizes for different contexts.
- **Avatar Group** — Stacked or clustered avatars representing multiple users.

## Related
[Badge](badge.md), [Tooltip](tooltip.md), [Hover Card](hover-card.md)

Source: [UX Components](https://www.ux-components.com/components/avatar)
