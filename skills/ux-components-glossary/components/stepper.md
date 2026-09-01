# Stepper

**Level:** Unclassified  
**Category:** Navigation

A visual indicator showing the user's position in a multi-step process or wizard.

## When to use
- Multi-step forms like checkout or registration
- Onboarding flows that guide users through setup
- Configuration wizards with sequential steps
- Order tracking showing fulfillment progress
- Any linear process that benefits from progress visibility

## When to avoid
- For non-sequential navigation — use Tabs instead
- When there are more than 7 steps — consider grouping or simplifying
- For real-time progress of a single task — use Progress Bar
- When steps can be done in any order — steppers imply sequence
- For simple two-step flows — a stepper adds unnecessary complexity

## States
- **Completed** — Step is finished — shown with a check mark.
- **Current** — The active step — visually prominent.
- **Upcoming** — Future step — muted appearance.
- **Error** — A step has a validation error — shown with an error indicator.
- **Disabled** — Step cannot be accessed.

## Related
[Progress](progress.md), [Tabs](tabs.md), [Pagination](pagination.md)

Source: [UX Components](https://www.ux-components.com/components/stepper)
