# Glossary — UX Components Atomic Catalog

Disclosed reference for [`ux-components-glossary`](SKILL.md). Level blurbs and placements from UX Components [`ATOMIC_CATEGORIES`](https://www.ux-components.com/js/components.js); purposes and detail from [`components-data.js`](https://www.ux-components.com/js/components-data.js).

Load `components/{id}.md` when defining or composing that component. Leave **Unclassified** entries unclassified — do not invent a level.

## Atoms

*Basic, indivisible UI elements — the smallest functional building blocks.*

| Component | Purpose |
| --- | --- |
| [Button](components/button.md) | The primary mechanism for user-initiated actions. |
| [Badge](components/badge.md) | A small visual indicator, typically a number or short text, used to highlight a count, status, or label. |
| [Avatar](components/avatar.md) | A visual representation of a user or entity, typically shown as a photo, initials, or a fallback icon. |
| [Label](components/label.md) | A text element that identifies and describes a form control for both sighted users and assistive technology. |
| [Input](components/input.md) | A single-line text field that accepts typed user input. |
| [Textarea](components/textarea.md) | A multi-line text input for longer-form content like comments or descriptions. |
| [Checkbox](components/checkbox.md) | A binary control that lets the user toggle an option on or off independently of other choices. |
| [Radio Group](components/radio-group.md) | A set of mutually exclusive options where selecting one deselects the others. |
| [Switch](components/switch.md) | A toggle control for instantly switching between two mutually exclusive states. |
| [Toggle](components/toggle.md) | A button that switches between two states (on/off, active/inactive) and visually reflects the current state. |
| [Separator](components/separator.md) | A visual divider used to separate sections of content or groups of related items. |
| [Progress](components/progress.md) | A visual indicator of completion percentage for a determinate task or process. |
| [Skeleton](components/skeleton.md) | A placeholder that mimics the shape and layout of content while it is loading. |
| [Slider](components/slider.md) | A control for selecting a numeric value by dragging a thumb along a track. |
| [Spinner](components/spinner.md) | An animated loading indicator that signals an ongoing process with an indeterminate duration. |
| [Rating](components/rating.md) | An interactive or read-only star-based control for providing or displaying a score. |
| [Chip](components/chip.md) | A compact, interactive element representing an input, attribute, or action in a condensed form. |
| [Image](components/image.md) | A component for displaying responsive, accessible images with optional captions and fallback states. |
| [Number Input](components/number-input.md) | A text field restricted to numeric values with optional increment and decrement controls. |
| [Color Picker](components/color-picker.md) | A specialized input that lets users select a color value from a spectrum, swatches, or by entering a hex/RGB code. |
| [Icon](components/icon.md) | A symbolic graphic element used for visual communication, labeling, and wayfinding. |

## Molecules

*Simple combinations of atoms that form distinct, reusable UI patterns.*

| Component | Purpose |
| --- | --- |
| [Alert](components/alert.md) | A static, non-interactive message that communicates important information, feedback, or status to the user. |
| [Card](components/card.md) | A self-contained, rectangular surface grouping related content and actions about a single subject. |
| [Breadcrumb](components/breadcrumb.md) | A secondary navigation aid showing the user's current location within the site hierarchy. |
| [Pagination](components/pagination.md) | A control for navigating between pages of content in a dataset or list. |
| [Tabs](components/tabs.md) | A set of layered content panels, only one visible at a time, switched via labeled triggers. |
| [Accordion](components/accordion.md) | A vertically stacked set of interactive headings, each revealing or hiding a section of content when clicked. |
| [Collapsible](components/collapsible.md) | A primitive that toggles the visibility of a content section, without the stacked list structure of an Accordion. |
| [Tooltip](components/tooltip.md) | A small, informational popup that appears on hover or focus to describe an element. |
| [Popover](components/popover.md) | A non-modal floating panel anchored to a trigger element for supplementary content. |
| [Hover Card](components/hover-card.md) | A popover that appears on hover over a trigger, used to preview supplementary information. |
| [Toast](components/toast.md) | A brief, auto-dismissing notification that appears to confirm an action or communicate a system event. |
| [Select](components/select.md) | A dropdown control that lets the user choose one option from a predefined list. |
| [Combobox](components/combobox.md) | A composite control combining a text input with a dropdown list, allowing the user to filter and select from available options. |
| [Toggle Group](components/toggle-group.md) | A set of toggle buttons where selecting one option may deselect others. |
| [Scroll Area](components/scroll-area.md) | A container with custom-styled scrollbars that overflows content within constrained dimensions. |
| [Date Picker](components/date-picker.md) | A specialized input that allows users to select a date from a calendar dropdown. |
| [Time Picker](components/time-picker.md) | A specialized input for selecting a time value with hour, minute, and optional AM/PM controls. |
| [Tag](components/tag.md) | A compact label used to categorize, classify, or add metadata to content. |
| [List](components/list.md) | A vertical arrangement of related content items with consistent spacing and structure. |
| [Timeline](components/timeline.md) | A chronological display of events or activities arranged along a vertical or horizontal line. |

## Organisms

*Complex, self-contained components built from atoms and molecules.*

| Component | Purpose |
| --- | --- |
| [Dialog](components/dialog.md) | A modal window that appears over the main content to present information or collect input. |
| [Alert Dialog](components/alert-dialog.md) | A modal overlay that interrupts the user with a critical message requiring an explicit decision before they can continue. |
| [Sheet](components/sheet.md) | A panel that slides in from the edge of the screen, overlaying the main content. |
| [Dropdown Menu](components/dropdown-menu.md) | A toggleable overlay that displays a list of actions or navigation options when triggered by a button or link. |
| [Context Menu](components/context-menu.md) | A floating menu that appears on right-click, providing contextual actions related to the clicked element. |
| [Table](components/table.md) | A structured grid of rows and columns for displaying tabular data. |
| [Calendar](components/calendar.md) | A visual date grid that displays a month at a time, allowing users to view and select dates. |
| [Menubar](components/menubar.md) | A horizontal bar of top-level menu items, each opening a dropdown of actions or sub-menus. |
| [Navigation Menu](components/navigation-menu.md) | A persistent vertical or horizontal menu used for primary site or app-level navigation. |
| [Carousel](components/carousel.md) | A horizontally scrollable set of content panels that cycle through items one or a few at a time. |
| [Data Table](components/data-table.md) | A feature-rich table with sorting, filtering, pagination, and row selection for complex datasets. |
| [Tree View](components/tree-view.md) | A hierarchical display of nested data using expandable and collapsible parent-child nodes. |
| [Form](components/form.md) | A container that groups related inputs, manages validation, and handles data submission. |
| [Toolbar](components/toolbar.md) | A horizontal container that groups related actions, controls, and tools into a compact bar. |

## Appendix: Unclassified

Present in the catalog, absent from `ATOMIC_CATEGORIES`.

| Component | Purpose |
| --- | --- |
| [Empty](components/empty-state.md) | A placeholder UI shown when there is no content to display in a given area. |
| [File Upload](components/file-upload.md) | An input control for selecting and uploading files from the user's device. |
| [Search](components/search.md) | A specialized text input optimized for search queries with optional typeahead and clear functionality. |
| [Link](components/link.md) | An interactive text element that navigates users to another page, section, or resource. |
| [Stepper](components/stepper.md) | A visual indicator showing the user's position in a multi-step process or wizard. |
| [Banner](components/banner.md) | A prominent, full-width message displayed at the top of a page or section to communicate system-wide information. |
| [Meter](components/meter.md) | A visual gauge that represents a scalar value within a known range. |
| [Treegrid](components/treegrid.md) | A tabular grid whose rows can be expanded and collapsed to reveal nested child rows — combining the columns of a table with the hierarchy of a tree. |
| [Window Splitter](components/window-splitter.md) | A draggable bar between two adjacent panels that lets users resize them by clicking and dragging. |
| [Feed](components/feed.md) | A scrollable list of articles or content items loaded incrementally as the user scrolls — with ARIA semantics that let screen readers navigate item-by-item without losing context. |
| [Landmark Regions](components/landmarks.md) | Semantic HTML5 regions (header, nav, main, aside, footer, search) that let screen reader users jump between major sections of a page with a single keystroke. |
