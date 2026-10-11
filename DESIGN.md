# Design System Document: Edén Terrassa Visual Identity

## 1. Overview & Creative North Star
**Creative North Star: "The Sacred Sanctuary"**
This design system moves away from the "corporate church" aesthetic and toward a digital experience that feels like an organic extension of a spiritual community. We reject rigid, boxed-in layouts in favor of **Soft Minimalism**—an approach that uses expansive breathing room, tonal depth, and intentional asymmetry to guide the user’s soul through the interface. 

The goal is to create a "Curated Editorial" feel. By utilizing high-contrast typography scales and overlapping layered elements, we break the "template" look to offer something that feels bespoke, premium, and inherently welcoming.

---

## 2. Colors & Tonal Atmosphere
The palette is rooted in the organic `#78866B` Sage Green, evoking growth and peace. This is balanced by warm, creamy neutrals that prevent the interface from feeling clinical.

### The "No-Line" Rule
To maintain a high-end editorial feel, **1px solid borders for sectioning are strictly prohibited.** Boundaries must be defined solely through background color shifts. For example, a `surface-container-low` section should sit directly against a `background` section to create a soft, sophisticated transition.

### Surface Hierarchy & Nesting
Treat the UI as a physical space with layered materials.
*   **Base:** Use `surface` (#fbf9f5) for the primary background.
*   **Nesting:** Place `surface-container-lowest` cards on a `surface-container-low` section to create a natural, "sun-drenched" lift.
*   **Signature Textures:** For Hero backgrounds and high-impact CTAs, use a subtle linear gradient transitioning from `primary` (#536047) to `primary_container` (#6b795f) at a 135-degree angle. This adds a "soul" to the color that flat hex codes cannot achieve.

### The Glass Rule
Floating elements (navigation bars, modal overlays) should utilize **Glassmorphism**. Apply a semi-transparent `surface` color with a `backdrop-blur` (12px-20px) to allow the organic colors of the site to bleed through, creating a "frosted glass" effect.

---

## 3. Typography
We use **Manrope** as our foundational typeface. It is a modern, clean sans-serif that balances high-impact authority with a friendly, open geometric structure.

*   **Display (lg/md/sm):** Used for primary landing headers. Use `display-lg` (3.5rem) with a `font-weight: 800` to create an editorial "magazine" feel. Letter spacing should be set to `-0.02em`.
*   **Headline (lg/md/sm):** Reserved for section titles. These should lead the eye and provide clear SEO-friendly structure (H2, H3).
*   **Body (lg/md):** Use `on_surface_variant` (#454840) for body text to ensure a softer, more organic reading experience than pure black.
*   **Labels:** Use `label-md` for small utility text. These should be all-caps with a `+0.05em` letter-spacing to maintain legibility.

---

## 4. Elevation & Depth
Depth is achieved through **Tonal Layering** rather than traditional drop shadows.

*   **The Layering Principle:** Stack `surface-container` tiers. A `surface-container-highest` element on a `surface` background provides all the hierarchy needed without visual clutter.
*   **Ambient Shadows:** If a card must "float" (e.g., a featured event card), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(27, 28, 26, 0.05)`. The color is a tinted version of `on-surface`, mimicking natural light.
*   **The Ghost Border:** If a boundary is required for accessibility, use the `outline-variant` token (#c5c8bd) at **15% opacity**. This creates a "suggestion" of a line rather than a hard break.

---

## 5. Components

### Buttons
*   **Primary:** `primary` background with `on_primary` text. Use `xl` (1.5rem) roundedness for a soft, pill-like feel. 
*   **Secondary:** `surface-container-high` background. No border.
*   **Tertiary:** Text-only with a subtle `primary` underline that expands on hover.

### Inputs & Fields
*   **Styling:** Use `surface-container-lowest` for the input background. On focus, shift the background to `surface` and apply a 1px "Ghost Border" using the `primary` color at 40% opacity.
*   **Roundedness:** All inputs follow the `md` (0.75rem) scale.

### Cards & Lists
*   **Forbid Dividers:** Never use a horizontal line to separate list items. Use the **Spacing Scale** (e.g., `8` or `10` units) to create "White Space Dividers."
*   **Community Chips:** For categorizing sermons or events, use selection chips in `secondary_container` with `on_secondary_container` text. Use `full` (9999px) roundedness.

### Specialty: The "Sanctuary" Hero
A unique component for this system: A full-bleed image container that uses a `primary` to transparent gradient overlay at the bottom, allowing `display-lg` typography to sit half-on and half-off the image for a high-end editorial overlap.

---

## 6. Do's and Don'ts

### Do
*   **DO** use intentional asymmetry. Place a small `title-sm` caption to the far left and the `headline-lg` shifted slightly to the right to create visual interest.
*   **DO** prioritize "Negative Space." If a section feels crowded, double the spacing using the `20` (7rem) token.
*   **DO** use high-quality photography with organic, warm filters to match the Sage Green palette.

### Don't
*   **DON'T** use 100% black (#000000). Always use `on_surface` or `on_background` charcoal tones.
*   **DON'T** use standard 1px borders. If you feel the need for a line, use a background color change instead.
*   **DON'T** use sharp corners. The `none` and `sm` roundedness scales should be avoided to maintain the "Organic" personality of the design system.
*   **DON'T** clutter the navigation. Use a "Less is More" approach to ensure a welcoming, non-overwhelming user experience.