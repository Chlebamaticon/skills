# UX Components Atomic Glossary (research)

Extracted for a coding-agent skill from the UX Components catalog and Atomic view. Classifications are taken from site JS (`ATOMIC_CATEGORIES`); descriptions from catalog `desc` fields. Do not invent placements.

## Sources

| Source | Role |
| --- | --- |
| [Atomic view](https://www.ux-components.com/components/atomic) | Browse mode that groups catalog components as Atoms / Molecules / Organisms |
| [components-data.js](https://www.ux-components.com/js/components-data.js) | Canonical `COMPONENTS[]` (id, name, category, desc, use, …) — **66** entries at fetch time |
| [components.js](https://www.ux-components.com/js/components.js) | `ATOMIC_CATEGORIES` id lists + level blurbs; renders Atomic view |
| [i18n/en.js](https://www.ux-components.com/js/i18n/en.js) | Localized `catdesc.Atoms` / `Molecules` / `Organisms` (same English blurbs) |
| [glossary.html](https://www.ux-components.com/glossary.html) | Site glossary; Atomic Design term points at Brad Frost’s five levels |
| [About](https://www.ux-components.com/about.html) | Acknowledges Brad Frost; Atomic view = Atoms, Molecules, Organisms only |
| [MCP docs](https://www.ux-components.com/mcp) | `lookup` / `recommend` via `POST https://www.ux-components.com/api/mcp` (not needed for classification) |
| [Brad Frost, Atomic Design ch. 2](https://atomicdesign.bradfrost.com/chapter-2/) | Methodology baseline for Templates / Pages (omitted by UX Components Atomic view) |

**Classification rule (site):** Atomic placement is a hard-coded id list in `ATOMIC_CATEGORIES` inside `components.js`, not a field on each `COMPONENTS` entry. Default browse mode uses functional `category` (Action, Form, …). CSV export adds an “Atomic Category” column via the same lookup. ([components.js](https://www.ux-components.com/js/components.js))

## Level definitions (Atoms / Molecules / Organisms)

### UX Components Atomic view (primary)

| Level | Purpose (site copy) | Source |
| --- | --- | --- |
| **Atoms** | Basic, indivisible UI elements — the smallest functional building blocks. | [components.js](https://www.ux-components.com/js/components.js), [i18n/en.js](https://www.ux-components.com/js/i18n/en.js) `catdesc.Atoms` |
| **Molecules** | Simple combinations of atoms that form distinct, reusable UI patterns. | same, `catdesc.Molecules` |
| **Organisms** | Complex, self-contained components built from atoms and molecules. | same, `catdesc.Organisms` |

About page: Atomic view organizes components into Atoms, Molecules, and Organisms as a Brad Frost–inspired hierarchy from smallest indivisible elements to self-contained interface sections. ([about.html](https://www.ux-components.com/about.html))

Site glossary “Atomic Design” names five levels (atoms, molecules, organisms, **templates**, **pages**) but the product Atomic browse mode only implements the first three. ([glossary.html](https://www.ux-components.com/glossary.html))

### Brad Frost baseline (templates / pages only — UX Components omits these in Atomic view)

| Level | Purpose (methodology) | Source |
| --- | --- | --- |
| **Atoms** | Foundational UI building blocks that can’t be broken down further without ceasing to be functional (e.g. labels, inputs, buttons). | [Chapter 2](https://atomicdesign.bradfrost.com/chapter-2/) |
| **Molecules** | Relatively simple groups of UI elements functioning together as a unit (e.g. search form = label + input + button). | same |
| **Organisms** | Relatively complex components of molecules and/or atoms (and/or other organisms) that form distinct interface sections (e.g. header). | same |
| **Templates** | Page-level objects that place components into a layout and articulate content structure. | same — **not used** in UX Components Atomic lists |
| **Pages** | Specific instances of templates with real representative content. | same — **not used** in UX Components Atomic lists |

## Atoms

21 components. Level desc: *Basic, indivisible UI elements — the smallest functional building blocks.* ([components.js](https://www.ux-components.com/js/components.js))

| Name | id | Purpose (catalog `desc`) |
| --- | --- | --- |
| Avatar | `avatar` | A visual representation of a user or entity, typically shown as a photo, initials, or a fallback icon. |
| Badge | `badge` | A small visual indicator, typically a number or short text, used to highlight a count, status, or label. |
| Button | `button` | The primary mechanism for user-initiated actions. |
| Checkbox | `checkbox` | A binary control that lets the user toggle an option on or off independently of other choices. |
| Chip | `chip` | A compact, interactive element representing an input, attribute, or action in a condensed form. |
| Color Picker | `color-picker` | A specialized input that lets users select a color value from a spectrum, swatches, or by entering a hex/RGB code. |
| Icon | `icon` | A symbolic graphic element used for visual communication, labeling, and wayfinding. |
| Image | `image` | A component for displaying responsive, accessible images with optional captions and fallback states. |
| Input | `input` | A single-line text field that accepts typed user input. |
| Label | `label` | A text element that identifies and describes a form control for both sighted users and assistive technology. |
| Number Input | `number-input` | A text field restricted to numeric values with optional increment and decrement controls. |
| Progress | `progress` | A visual indicator of completion percentage for a determinate task or process. |
| Radio Group | `radio-group` | A set of mutually exclusive options where selecting one deselects the others. |
| Rating | `rating` | An interactive or read-only star-based control for providing or displaying a score. |
| Separator | `separator` | A visual divider used to separate sections of content or groups of related items. |
| Skeleton | `skeleton` | A placeholder that mimics the shape and layout of content while it is loading. |
| Slider | `slider` | A control for selecting a numeric value by dragging a thumb along a track. |
| Spinner | `spinner` | An animated loading indicator that signals an ongoing process with an indeterminate duration. |
| Switch | `switch` | A toggle control for instantly switching between two mutually exclusive states. |
| Textarea | `textarea` | A multi-line text input for longer-form content like comments or descriptions. |
| Toggle | `toggle` | A button that switches between two states (on/off, active/inactive) and visually reflects the current state. |

Source for rows: [components-data.js](https://www.ux-components.com/js/components-data.js); placement: [components.js](https://www.ux-components.com/js/components.js) `ATOMIC_CATEGORIES.Atoms.ids`.

## Molecules

20 components. Level desc: *Simple combinations of atoms that form distinct, reusable UI patterns.* ([components.js](https://www.ux-components.com/js/components.js))

| Name | id | Purpose (catalog `desc`) |
| --- | --- | --- |
| Accordion | `accordion` | A vertically stacked set of interactive headings, each revealing or hiding a section of content when clicked. |
| Alert | `alert` | A static, non-interactive message that communicates important information, feedback, or status to the user. |
| Breadcrumb | `breadcrumb` | A secondary navigation aid showing the user's current location within the site hierarchy. |
| Card | `card` | A self-contained, rectangular surface grouping related content and actions about a single subject. |
| Collapsible | `collapsible` | A primitive that toggles the visibility of a content section, without the stacked list structure of an Accordion. |
| Combobox | `combobox` | A composite control combining a text input with a dropdown list, allowing the user to filter and select from available options. |
| Date Picker | `date-picker` | A specialized input that allows users to select a date from a calendar dropdown. |
| Hover Card | `hover-card` | A popover that appears on hover over a trigger, used to preview supplementary information. |
| List | `list` | A vertical arrangement of related content items with consistent spacing and structure. |
| Pagination | `pagination` | A control for navigating between pages of content in a dataset or list. |
| Popover | `popover` | A non-modal floating panel anchored to a trigger element for supplementary content. |
| Scroll Area | `scroll-area` | A container with custom-styled scrollbars that overflows content within constrained dimensions. |
| Select | `select` | A dropdown control that lets the user choose one option from a predefined list. |
| Tabs | `tabs` | A set of layered content panels, only one visible at a time, switched via labeled triggers. |
| Tag | `tag` | A compact label used to categorize, classify, or add metadata to content. |
| Time Picker | `time-picker` | A specialized input for selecting a time value with hour, minute, and optional AM/PM controls. |
| Timeline | `timeline` | A chronological display of events or activities arranged along a vertical or horizontal line. |
| Toast | `toast` | A brief, auto-dismissing notification that appears to confirm an action or communicate a system event. |
| Toggle Group | `toggle-group` | A set of toggle buttons where selecting one option may deselect others. |
| Tooltip | `tooltip` | A small, informational popup that appears on hover or focus to describe an element. |

Source for rows: [components-data.js](https://www.ux-components.com/js/components-data.js); placement: [components.js](https://www.ux-components.com/js/components.js) `ATOMIC_CATEGORIES.Molecules.ids`.

## Organisms

14 components. Level desc: *Complex, self-contained components built from atoms and molecules.* ([components.js](https://www.ux-components.com/js/components.js))

| Name | id | Purpose (catalog `desc`) |
| --- | --- | --- |
| Alert Dialog | `alert-dialog` | A modal overlay that interrupts the user with a critical message requiring an explicit decision before they can continue. |
| Calendar | `calendar` | A visual date grid that displays a month at a time, allowing users to view and select dates. |
| Carousel | `carousel` | A horizontally scrollable set of content panels that cycle through items one or a few at a time. |
| Context Menu | `context-menu` | A floating menu that appears on right-click, providing contextual actions related to the clicked element. |
| Data Table | `data-table` | A feature-rich table with sorting, filtering, pagination, and row selection for complex datasets. |
| Dialog | `dialog` | A modal window that appears over the main content to present information or collect input. |
| Dropdown Menu | `dropdown-menu` | A toggleable overlay that displays a list of actions or navigation options when triggered by a button or link. |
| Form | `form` | A container that groups related inputs, manages validation, and handles data submission. |
| Menubar | `menubar` | A horizontal bar of top-level menu items, each opening a dropdown of actions or sub-menus. |
| Navigation Menu | `navigation-menu` | A persistent vertical or horizontal menu used for primary site or app-level navigation. |
| Sheet | `sheet` | A panel that slides in from the edge of the screen, overlaying the main content. |
| Table | `table` | A structured grid of rows and columns for displaying tabular data. |
| Toolbar | `toolbar` | A horizontal container that groups related actions, controls, and tools into a compact bar. |
| Tree View | `tree-view` | A hierarchical display of nested data using expandable and collapsible parent-child nodes. |

Source for rows: [components-data.js](https://www.ux-components.com/js/components-data.js); placement: [components.js](https://www.ux-components.com/js/components.js) `ATOMIC_CATEGORIES.Organisms.ids`.

## Notes / gaps

### Catalog vs Atomic coverage

- **`COMPONENTS` length:** 66. **Atomic-assigned:** 55 (21 + 20 + 14). **No duplicates** across levels; every Atomic id resolves in the catalog. ([components-data.js](https://www.ux-components.com/js/components-data.js), [components.js](https://www.ux-components.com/js/components.js))
- **Unmapped in Atomic view** (present in catalog, absent from `ATOMIC_CATEGORIES` — do not invent a level):

| Name | id | Default category | Purpose (catalog `desc`) |
| --- | --- | --- | --- |
| Banner | `banner` | Feedback | A prominent, full-width message displayed at the top of a page or section to communicate system-wide information. |
| Empty | `empty-state` | Feedback | A placeholder UI shown when there is no content to display in a given area. |
| Feed | `feed` | Data Display | A scrollable list of articles or content items loaded incrementally as the user scrolls — with ARIA semantics that let screen readers navigate item-by-item without losing context. |
| File Upload | `file-upload` | Form | An input control for selecting and uploading files from the user's device. |
| Landmark Regions | `landmarks` | Layout | Semantic HTML5 regions (header, nav, main, aside, footer, search) that let screen reader users jump between major sections of a page with a single keystroke. |
| Link | `link` | Navigation | An interactive text element that navigates users to another page, section, or resource. |
| Meter | `meter` | Feedback | A visual gauge that represents a scalar value within a known range. |
| Search | `search` | Form | A specialized text input optimized for search queries with optional typeahead and clear functionality. |
| Stepper | `stepper` | Navigation | A visual indicator showing the user's position in a multi-step process or wizard. |
| Treegrid | `treegrid` | Data Display | A tabular grid whose rows can be expanded and collapsed to reveal nested child rows — combining the columns of a table with the hierarchy of a tree. |
| Window Splitter | `window-splitter` | Layout | A draggable bar between two adjacent panels that lets users resize them by clicking and dragging. |

### Templates / pages

- UX Components Atomic browse mode does **not** define Templates or Pages buckets. Glossary and About still reference Brad Frost’s broader model; use Frost ch. 2 if a skill needs those two levels. ([glossary.html](https://www.ux-components.com/glossary.html), [about.html](https://www.ux-components.com/about.html), [Chapter 2](https://atomicdesign.bradfrost.com/chapter-2/))

### Count inconsistencies (site copy vs data)

- About / i18n copy still says “59 components across 9 categories”; live `COMPONENTS` has **66**. MCP marketing page cites “62 components”. Prefer the JS array over marketing counts when building a skill. ([about.html](https://www.ux-components.com/about.html), [mcp](https://www.ux-components.com/mcp), [components-data.js](https://www.ux-components.com/js/components-data.js))

### SPA / tooling notes

- Atomic HTML shell is thin; grouping is client-side from `components.js` after `components-data.js` loads. Empty “no match” snapshots from crawlers are expected without JS execution. ([components/atomic](https://www.ux-components.com/components/atomic))
- `shared.js` / `index.js` handle theme, search chrome, landing counts — **not** Atomic classification. Classification lives only in `ATOMIC_CATEGORIES` in `components.js`.
- MCP `lookup` / `recommend` can enrich usage advice; they are not the source of Atomic labels. Endpoint is POST-only (`GET /api/mcp` → 405). ([mcp](https://www.ux-components.com/mcp))

### Skill takeaway

When recommending or labeling components atomically for this catalog: use the three site lists above; leave the 11 unmapped ids unclassified (or fall back to Default `category`) rather than guessing Atoms/Molecules/Organisms.
