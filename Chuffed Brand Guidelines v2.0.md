# Chuffed Brand Guidelines v4.0

## The CORE.120 Muted System
This document outlines the architectural standards for the **CORE.120 Muted** design system. The system is a "Chromatic Monochrome" aesthetic, utilising a desaturated 120° hue (Green) to create a high-fidelity, technical environment focused on clarity, professional depth, and precision.

## 1. Colour Palette

### 1.1 The Primary Atmospheric Base (Hue 120°)
The palette is strictly constrained to **Saturation 4–10%**. Do not use vibrant greens or pure blacks/whites.

| Role | HEX | Description | HSL |
| :--- | :--- | :--- | :--- |
| **Background** | `#0a0b0a` | "Forest Charcoal" - Deepest base layer. | `120, 4%, 4%` |
| **Surface** | `#181a18` | "Deep Timber" - Header strips, card backgrounds. | `120, 4%, 10%` |
| **Border** | `#2c2e2c` | "Moss Slate" - UI outlines, dividers, inputs. | `120, 4%, 18%` |
| **Secondary Text** | `#7d827d` | "Sage Grey" - Body copy and descriptions. | `120, 4%, 50%` |
| **Primary Text** | `#e4e6e4` | "Mist White" - Headings and active states. | `120, 4%, 90%` |
| **Highlight** | `#f8f9f8` | "Frost" - Buttons and high-contrast text. | `120, 4%, 98%` |

### 1.2 The High-Visibility Accent (Hue 300°)
Used only for focal points and core transformations.
- **Accent Coral:** `hsl(343, 93%, 52%)`
- **Usage:** Small markers (dots), specific keywords, and high-priority interactive hover states.

### 1.3 Interactive State Logic
To maintain the "Muted" philosophy, interactive transitions are categorized by priority:
- **High Priority (CTA/Nav):** `Primary Text` $\rightarrow$ `Accent Coral`.
- **Low Priority (Utility/Profile):** `Secondary Text` $\rightarrow$ `Primary Text`. This creates a sophisticated, tiered visual hierarchy.

## 2. Typography
The system pairs high-precision Monospace with high-performance Sans-Serif.

### **JetBrains Mono** (Headings & UI Labels)
- **Use Case:** All `H1–H6`, Navigation, Labels, and Metadata.
- **Style:** `text-transform: uppercase`, `letter-spacing: 0.15em`.
- **Weight:** `Bold (700)` for headings; `Medium (500)` for labels.

### **Inter** (Body & Documentation)
- **Use Case:** Paragraphs, lead-in text, and lists.
- **Style:** `line-height: 1.6`.
- **Weight:** `Light (300)` for lead text; `Regular (400)` for standard body.

## 3. UI Components

### 3.1 The Structured Panel
Panels replace traditional "Terminal" windows to lean into a professional IDE look.
- **Structure:** `#2c2e2c` border (1px) with a `#0a0b0a` background.
- **Header:** A `#181a18` strip containing a label in `JetBrains Mono` (uppercase).
- **Content Layout:** `.panel-content` is a flex column (`gap: 16px`) aligned to `flex-start`.
- **Height Variants:**
    - **Stretch (Default):** Fills the grid row height.
    - **Hug (`.panel-hug`):** Wraps tightly around content using `align-self: start`.

### 3.2 Buttons & Interactivity
- **Primary CTA:** Mist White (`#e4e6e4`) background with Charcoal (`#0a0b0a`) text.
    - **Hover State:** Translate `-1px` vertically and add a solid shadow of the **Accent Coral** (`4px`).
- **Subtle Interaction (`.read-more-btn`):**
    - **Base State:** `Secondary Text`, `text-decoration: none`.
    - **Expanded State:** `Primary Text`.
    - **Constraint:** No box-shadow or transforms on hover to prevent visual noise.
- **External Links:** Represented by a compact, inline SVG "open link" symbol.

### 3.3 The Testimonial System
- **Layout:** Single column (`.grid-single`), max-width `800px`.
- **Content Management:**
    - **Truncation:** Text truncated at 160 characters with an ellipsis.
    - **Interaction:** JavaScript-driven "Read more" / "Read less" toggle.
- **Structure:** `.testimonial-card` containing a `testimonial-header` (Avatar + Name) and truncated text block.

### 3.4 Social Link Cards
- **Global Variant (Footer):** `Primary Text` base $\rightarrow$ `Accent Coral` hover.
- **Profile Variant (Maurice Page):** `Secondary Text` base $\rightarrow$ `Primary Text` hover.
- **Subtle Variant (`.home-link-card`):** Transparent background, border-only, no shadow.

## 4. Layout & Grid

### 4.1 Grid Standards
- **Responsive Grid:** `auto-fit` with `300px` minmax.
- **Single Column Grid (`.grid-single`):**
    - **Testimonials:** `max-width: 800px`.
    - **Profile Pages:** `max-width: 600px`.

### 4.2 Profile Headers
- **Layout:** Flex-row (`flex-wrap: wrap`) containing a profile image and a text block.
- **Alignment:** Centered for a balanced, personal introduction.

## 5. Design Principles

### 1. Atmospheric Neutrality
The design should feel "Professional Grayscale" at first glance. The 120° green tint provides a subconscious "atmospheric" depth.

### 2. Flat Aesthetic (No Gradients)
Avoid all gradients, glows, or blurs. Depth is achieved purely through color value (Lightness) and structural borders.

### 3. Precision Markers
Use "Markers" to draw the eye instead of splashes of color:
- A single `6px` dot in a panel header.
- A period `.` at the end of a heading in the Coral accent.
- A change in color for exactly one word in a headline.

### 4. Subtle Progression
Shift interaction colors from `Secondary` to `Primary` for utility links to guide the user without breaking the muted atmosphere.

### 5. No Technical Flourishes
Avoid "Hacker" clichés (scan lines, glitch effects, faux-terminal logs). The goal is to feel like a **High-End Professional Tool**.

## 6. Spacing System
Use a strict **16px** (4-unit) grid.
- **Internal Padding:** `24px`.
- **Section Gap:** `96px`.
- **Component Gap:** `32px`.
- **Profile Gap:** `24px` (for image-to-text alignment).
