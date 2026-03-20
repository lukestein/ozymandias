# Design System Document: The Desert Archive

## 1. Overview & Creative North Star
**Creative North Star: "The Resurrected Manuscript"**

This design system rejects the clinical coldness of modern "SaaS" interfaces in favor of a digital experience that feels like a curated exhibition of ancient wisdom. We are moving away from the rigid, boxed-in layouts of the early web. Instead, the "Resurrected Manuscript" approach treats the browser as an expansive, tactile landscape. 

By utilizing intentional asymmetry, expansive negative space (using our `24` and `16` spacing tokens), and overlapping editorial elements, we create a sense of discovery. The goal is to make the user feel like a scholar unearthing a hidden text—one that is prestigious, weathered, yet impeccably preserved through modern technology.

---

## 2. Colors & Surface Philosophy
The palette is a dialogue between the sun-bleached desert (`surface`) and the deep, permanent stains of ancient ink (`primary`).

### The "No-Line" Rule
To maintain a high-end editorial feel, **1px solid borders are strictly prohibited for sectioning.** Use tonal transitions to define boundaries. A side-bar or a content block should be distinguished by shifting from `surface` (#fbfbe2) to `surface-container-low` (#f5f5dc). This creates a "soft edge" that feels architectural rather than digital.

### Surface Hierarchy & Nesting
Treat the interface as layers of parchment and stone. 
- **Base Layer:** `surface` (#fbfbe2) for the wide expanse.
- **Content Blocks:** Use `surface-container` (#efefd7) for primary reading areas.
- **Nested Focus:** For callouts or interactive cards, use `surface-container-highest` (#e4e4cc) to pull the element forward.

### Signature Textures: The "Sunlight Gradient"
To avoid the flatness of generic UI, use subtle linear gradients for large background sections or Hero CTAs. Transition from `primary` (#446464) to `primary_container` (#bfe2e1) at a 135-degree angle. This mimics the way light hits weathered stone—dark in the crevices, shimmering on the edges.

---

## 3. Typography
Our typography is a balance of the poetic (Serif) and the functional (Sans-Serif).

*   **The Voice (Serif - Newsreader):** Used for all literary content and high-level headings. It is our "Scholar" font.
    *   **Display-LG (3.5rem):** Reserved for poem titles and major thematic headers. Use `-0.02em` letter spacing for a tighter, premium feel.
    *   **Headline-MD (1.75rem):** For stanza headers or critical essay titles.
    *   **Body-LG (1.0rem):** The gold standard for reading. Use a generous line-height (1.6 - 1.8) to allow the text to breathe like a classic printed page.

*   **The Tool (Sans-Serif - Plus Jakarta Sans):** Used for navigation, metadata, and interface controls.
    *   **Label-MD (0.75rem):** Use all-caps with `0.1em` letter spacing for "Metadata" tags (e.g., DATE, AUTHOR, ERA). This creates an "archival" aesthetic.

---

## 4. Elevation & Depth
Depth in this system is achieved through light and atmospheric perspective, not heavy drop shadows.

*   **The Layering Principle:** Instead of a shadow, place a `surface-container-lowest` (#ffffff) card on a `surface-container-low` (#f5f5dc) background. The subtle 2% shift in brightness provides all the separation needed.
*   **Ambient Shadows:** For floating menus or modals, use an extra-diffused shadow: `0px 20px 40px rgba(74, 71, 56, 0.06)`. Note that the shadow color is a tinted version of `on-surface-variant`, never pure black.
*   **Glassmorphism (The "Vellum" Effect):** For sticky headers or hovering tooltips, use `surface` at 80% opacity with a `20px` backdrop-blur. This mimics the look of translucent vellum paper, allowing the text beneath to be felt but not seen.

---

## 5. Components

### Buttons
- **Primary:** Background `primary` (#446464), Text `on-primary` (#ffffff). Use `rounded-sm` (0.125rem) for a sharp, chiseled stone look.
- **Tertiary (The "Invisible" Button):** No background. Text `primary`. Underline on hover with a 1px stroke of `tertiary`.

### Cards & Lists
- **The "No-Divider" Rule:** Never use a horizontal line to separate list items. Use spacing token `6` (2rem) to create separation, or a alternating background shift to `surface-container-low`.
- **Card Styling:** No borders. Use `surface-container-highest` for the card body and `rounded-md` for the corners.

### Literary Annotations (Custom Component)
- **The "Ink Drop" Chip:** For highlighting specific text in a poem. Use `tertiary_container` (#eedc82) with `on-tertiary-container` (#6d6012). It should feel like a highlighter pen used on an old manuscript.

### Input Fields
- **Editorial Style:** Only a bottom border using `outline-variant` (#cdc6b3) at 40% opacity. When focused, the border transitions to `primary` (#446464) and the background subtly shifts to `surface-container-highest`.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical margins. If the text is centered, let the metadata sit 2 units to the right to break the "grid" feel.
*   **Do** use the `24` (8.5rem) spacing token for top-of-page margins to create a sense of monumental scale.
*   **Do** mix the fonts: a Sans-Serif `label-sm` metadata tag sitting right above a Serif `headline-lg` title.

### Don't
*   **Don't** use pure black (#000000). Always use `on-surface` (#1b1d0e) for text to maintain the "deep ink" aesthetic.
*   **Don't** use `rounded-full` for anything other than a circular icon button. Our aesthetic is based on ruins and stone; it needs subtle angles, not bubbles.
*   **Don't** use high-contrast borders. If you can see the line clearly, it's too heavy. Soften it.