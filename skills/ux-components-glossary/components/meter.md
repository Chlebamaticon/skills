# Meter

**Level:** Unclassified  
**Category:** Feedback

A visual gauge that represents a scalar value within a known range.

## When to use
- Disk or storage usage indicators
- Password strength indicators
- Battery or signal level displays
- Quota or limit consumption tracking
- Performance or health scores

## When to avoid
- For task completion — use Progress Bar instead
- When the range is unknown or infinite
- For precise data entry — use Slider or Number Input
- When the value changes in real-time rapidly — it becomes distracting
- Without context — always label what the meter measures

## States
- **Low** — Value is in the safe/low range — typically green.
- **Medium** — Value is in the moderate range — typically yellow.
- **High** — Value is in the critical/high range — typically red.
- **Full** — Value has reached the maximum.

## Related
[Progress](progress.md), [Slider](slider.md), [Badge](badge.md)

Source: [UX Components](https://www.ux-components.com/components/meter)
