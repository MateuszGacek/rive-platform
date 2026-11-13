# rivé — Design System v0.1

- **Version** — 0.1
- **Status** — Draft / Discovery
- **Source** — Owner-provided brand direction, June 2026
- **Last reviewed** — 2026-11-13

**Quiet Luxury × Forest Wellness × Editorial Minimalism** guides the visual direction for both Public Web and Dashboard / CRM.

## Brand palette

**Confirmed** — The seven colors below are the recovered historical rivé palette. The interface roles are **Proposed**.

| Color | HEX | Proposed role |
| --- | --- | --- |
| Warm Ivory | `#F5F1E8` | Main background and label on the primary action |
| Natural Linen | `#E9E1D6` | Surface background |
| Sand Beige | `#DCCFBE` | Surface background |
| Oak Wood | `#C2A37D` | Accent |
| Sage Green | `#6F7A64` | Accent |
| Forest Green | `#264033` | Primary text and primary action background |
| Water Reflection | `#B9D1CF` | Accent |

Historical variants[^historical-variants] appear in earlier brand material.

[^historical-variants]: Earlier values included Oak `#C2A370` and Sage `#6F7A44`. The table records the values selected for the recovered palette.

**Proposed** — Use Chocolate Brown `#5A3D32` as a warm accent and Light Cocoa `#E8D8CB` as a complementary surface in editorial sections.

**Open question** — Select specific font families and colors for error, success, warning, and focus states.

## Visual principles

**Proposed** — Public Web and Dashboard / CRM share the same brand and adapt it to different tasks.

| Area | Public Web | Dashboard / CRM |
| --- | --- | --- |
| Priority | Atmosphere and conversion | Readability and efficiency |
| Layout | Spacious, editorial layouts | Structured, denser layouts |
| Typography | Serif headings and sans-serif body text | Predominantly sans-serif |
| Color | Natural backgrounds and larger areas of accent color | Neutral backgrounds and sparing use of accents |
| Photography | Central to communication | Secondary |

Favor natural materials, authentic photography of the property, generous space, and restrained compositions. Avoid ostentatious luxury, gold gradients, neon colors, and generic SaaS styling. Label visualizations of spaces that do not yet exist as concepts.

## Accessibility

- Use a minimum contrast ratio of **4.5:1** for normal text and **3:1** for large text. For text over photography, gradients, or overlays, check the rendered background in the least contrasting area behind the text. [WCAG 2.2 SC 1.4.3 — Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)
- Use at least **3:1** contrast against adjacent colors for the visual information needed to identify controls, their states, and meaningful parts of graphics. [WCAG 2.2 SC 1.4.11 — Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html)
- Pair status colors with a text label or another clear visual cue. The Level A use-of-color criterion also applies when targeting Level AA. [WCAG 2.2 SC 1.4.1 — Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html)

| Color on Warm Ivory | Contrast | Meets the minimum for normal text |
| --- | ---: | --- |
| Forest Green | 10.00:1 | Yes |
| Sage Green | 4.01:1 | No |
| Chocolate Brown | 8.67:1 | Yes |

Compare the unrounded ratio with the threshold. These results apply to the listed pairs on solid Warm Ivory.

## Change management

1. Record each new color or pattern as **Proposed**. Move it to **Confirmed** only after the owner explicitly approves it. Record the decision source and date.
2. Maintain the canonical specification in this repository.
3. After the UI library exists, use `/design-sync` from Claude Code as a separate step to import approved changes into Claude Design. Existing designs retain the copy they were created with and need an explicit update. [Claude Help Center](https://support.claude.com/en/articles/14604416-get-started-with-claude-design) · [Claude Academy](https://academy.claude.com/tutorials/create-a-design-system-with-claude)
