# Design System: Natural & Grounded Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Sanctuary"**

This design system is a response to the cluttered, high-frequency digital world. It is built to mirror the physical experience of a premium Indian retreat—airy, intentional, and deeply rooted in the landscape. We depart from the "generic SaaS" look by embracing **Editorial Asymmetry**. 

Unlike standard platforms that rely on rigid grids and heavy borders, this system uses expansive whitespace and overlapping elements to create a sense of discovery. We treat the digital screen not as a set of slots, but as a curated gallery where high-end serif typography meets organic, grounded shapes.

---

## 2. Colors
Our palette is derived from the natural materials of the Indian subcontinent: Sage, Terracotta, and Sand. 

### The Palette (Material Design Tokens)
- **Primary (Sage):** `#8A9A86` — Used for grounding actions and key brand moments.
- **Secondary (Terracotta):** `#C87961` — Evoking warmth and craft; used for highlighting and energy.
- **Tertiary (Deep Forest):** `#2C332A` — An additional accent for highlights and decorative elements, echoing deep natural tones.
- **Background (Soft Sand):** `#F4F1EB` — A warm, non-white canvas that reduces eye strain and feels premium.
- **Surface Tiers:** 
  - `surface-container-low`: `#EAE7E2`
  - `surface-container`: `#DFDCD7`
  - `surface-container-high`: `#D4D1CC`

### The "No-Line" Rule
**Explicit Instruction:** Traditional 1px solid borders are strictly prohibited for sectioning or card definition. Boundaries must be established through:
1. **Background Color Shifts:** A `surface-container-low` section sitting directly on a `surface` background.
2. **Generous Whitespace:** Using the `24 (8.5rem)` spacing token to separate distinct narrative blocks.

### Glass & Texture
To prevent the UI from feeling "flat," use **Glassmorphism** for floating navigation and booking bars. Apply a backdrop blur (12px–20px) to semi-transparent surface colors. Use a subtle linear gradient from `primary` to `primary_container` for hero CTAs to give them a "hand-dyed" silk quality rather than a plastic digital feel.

---

## 3. Typography
The typographic hierarchy is designed to feel like a high-end travel monograph.

*   **Display & Headlines (Noto Serif / Recoleta):** These are our "Voice." Large, expressive, and confident. Use `display-lg (3.5rem)` for hero sections with tight letter-spacing to create an authoritative, editorial impact.
*   **Body & Titles (Plus Jakarta Sans / Outfit):** These are our "Utility." Clean, highly legible, and modern. `body-lg (1rem)` is the workhorse for storytelling.
*   **The Narrative Contrast:** Always pair a `headline-lg` Serif with a `label-md` Sans-Serif in all caps (letter-spacing: 0.1em) to create a sophisticated, "Curated" hierarchy.

---

## 4. Elevation & Depth
In this design system, depth is a whisper, not a shout.

*   **The Layering Principle:** Stack surface tiers to create hierarchy. A `surface-container-lowest` card placed on a `surface-container-low` section provides a soft, natural lift that mimics paper sheets.
*   **Ambient Shadows:** For floating elements (like a "Book Now" FAB), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(44, 51, 42, 0.06);`. The shadow color is a tinted version of `Deep Forest`, never a neutral grey.
*   **The Ghost Border:** If a form field or interactive element requires a boundary, use the `outline-variant` token at **15% opacity**. This provides a "hint" of a container without breaking the airy aesthetic.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` color, `24px` (xl) corner radius. Use `title-sm` typography. 
*   **Secondary:** Ghost style using the "Ghost Border" (15% opacity `outline-variant`) with `primary` text.
*   **Tertiary:** Text-only with a `2px` underline that expands on hover.

### Cards & Property Lists
*   **Forbid Dividers:** Never use lines to separate list items. Use the `spacing-6 (2rem)` token to create clear, breathable gutters.
*   **Organic Corners:** All imagery and containers must use `rounded-xl (3rem)` or `rounded-lg (2rem)` to mimic organic, hand-carved edges.

### Interactive Inputs
*   **Currency Fields:** Include the Indian Rupee (₹) symbol as a fixed prefix in `tertiary` color.
*   **States:** Error states use `error` (#BA1A1A) but keep the organic `24px` radius. Focus states should use a soft `secondary_container` (#F8C8BD) glow rather than a harsh border.

### Contextual Components: "The Retreat Suite"
*   **The Availability Calendar:** Use a `surface-container-low` background with `secondary` (#C87961) dots for selected dates. Avoid grids; use white space to define weeks.
*   **Location Badges:** Small selection chips with `surface-variant` backgrounds and `24px` rounding, used for "Himalayas," "Goa," or "Kerala."

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical image layouts. Overlap a `headline-md` over the edge of a `rounded-xl` image to break the grid.
*   **Do** prioritize the Indian Rupee (₹) token in all pricing displays, using `title-lg` for the value and `label-sm` for the "per night" suffix.
*   **Do** use "Soft Sand" (#F4F1EB) as the default background instead of pure white to maintain the grounded, natural feel.

### Don't
*   **Don't** use 1px solid borders to separate content. It shatters the "airy" destination feel.
*   **Don't** use sharp 90-degree corners. Everything in nature is rounded; our UI should be too.
*   **Don't** use high-opacity black shadows. They feel heavy and "techy." Stick to the low-opacity, tinted Ambient Shadows.
*   **Don't** crowd the screen. If you feel like you need a divider, you likely just need more whitespace.