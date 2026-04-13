# Design System Strategy: MACADAMIA Boutique

## 1. Overview & Creative North Star: "The Tactile Gallery"
This design system is built to transcend the standard e-commerce experience. Our Creative North Star is **"The Tactile Gallery."** We are not building a store; we are creating a digital atelier. The interface must feel like flipping through a high-end, heavy-stock fashion editorial—where the clothes are the art and the UI is the invisible, elegant frame.

We break the "template" look by rejecting rigid, boxy structures. Instead, we use **Intentional Asymmetry** and **Tonal Layering**. Expect large, off-center hero imagery, overlapping typography that bleeds across containers, and a vast use of whitespace to signify luxury and "breathing room."

---

## 2. Colors: The Palette of Organic Warmth
The color strategy avoids the sterility of pure white. Instead, we use a spectrum of macadamia-inspired neutrals to create warmth and approachability without sacrificing elegance.

### Surface Hierarchy & Nesting
To move beyond the "flat web," we treat the UI as physical layers of fine paper. 
- **Base Layer:** Use `surface` (`#faf9f6`) as your canvas.
- **Sectioning:** Never use lines. Use `surface-container-low` (`#f4f4f0`) for large section breaks.
- **Floating Depth:** Use `surface-container-lowest` (`#ffffff`) for elevated cards or menus to create a soft, natural "lift."
- **Interactive Layers:** Use `surface-container-high` (`#e6e9e4`) for hovering states or subtle nested modules.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to separate content. All boundaries must be defined by background color shifts or whitespace. 

### Signature Textures & Gold Accents
- **The "Gold" Touch:** Use `tertiary` (`#745c00`) and its variants for subtle accents (iconography, small labels, or "New Collection" badges). This provides the "subtle gold" requested without looking "tinsel-like."
- **Glassmorphism:** For navigation bars or mobile overlays, use `surface` at 80% opacity with a `20px` backdrop-blur. This allows the high-quality product imagery to bleed through the UI, making the experience feel fluid.

---

## 3. Typography: Editorial Authority
The contrast between our two typefaces creates the "High-End" persona.

- **Display & Headlines (`notoSerif`):** This is our "Editorial" voice. Use `display-lg` for hero sections and `headline-md` for product names. The serif must feel timeless and stylish. To achieve a signature look, use negative letter-spacing (-2%) on large headlines to make them feel tighter and more "designed."
- **Body & Navigation (`manrope`):** This is our "Utility" voice. It provides a clean, modern counter-balance. Use `body-lg` for product descriptions and `label-md` for metadata.
- **The Polish Language Factor:** Ensure line-heights are generous (1.5x - 1.6x) to accommodate Polish diacritics (ą, ć, ę, ł, etc.) without feeling cramped.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are forbidden. We achieve depth through atmospheric light.

- **The Layering Principle:** Depth is "stacked." A card (`surface-container-lowest`) sits on a section (`surface-container-low`), which sits on a page (`surface`).
- **Ambient Shadows:** If a "floating" effect is mandatory (e.g., a "Quick Add to Cart" modal), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(47, 52, 48, 0.05)`. The color is a tinted version of `on-surface` to mimic natural light.
- **The "Ghost Border" Fallback:** For accessibility in form inputs, use `outline-variant` (`#afb3ae`) at **20% opacity**. It should be a suggestion of a border, not a hard line.

---

## 5. Components: Refined Utility

### Buttons (CTA)
- **Primary:** Background: `primary` (`#715a3e`), Text: `on-primary` (`#fff6f0`). Shape: `sm` (0.125rem) for a sharp, architectural look.
- **Secondary:** Background: `transparent`, Border: 1px Ghost Border (`outline-variant` @ 30%).
- **Tertiary:** Text: `primary`, no background. Used for "Learn More" or "View All" links.

### The "Product Card" (Bespoke Component)
- **Rules:** No borders. No shadows.
- **Layout:** High-quality image on `surface-variant`. Product title in `title-md` (manrope) followed by price in `notoSerif`.
- **Interaction:** On hover, the image scales subtly (1.05x) and the background shifts from `surface-variant` to `surface-container-highest`.

### Input Fields
- **Styling:** Minimalist bottom-border only or a subtle `surface-container` background.
- **States:** Error state uses `error` (`#9e422c`) for text, but never a harsh red box. Use soft, legible Polish error messages ("Wymagane pole").

### Navigation (The Curator Bar)
- **Design:** Floating `surface` with backdrop-blur. Links in `label-md` (manrope) with uppercase styling and `0.1rem` letter spacing to feel premium.

---

## 6. Do’s and Don'ts

### Do:
- **Use Large Margins:** A minimum of `80px` padding between sections to allow the brand to breathe.
- **Focus on Polish Typography:** Pay attention to "orphans" in Polish text (e.g., leaving a single letter like "i" or "w" at the end of a line).
- **Embrace Asymmetry:** Place a product image on the left and a headline overlapping its right edge for a custom look.

### Don’t:
- **No Pure Black:** Never use `#000000`. Use `on-surface` (`#2f3430`) for high contrast that remains soft and organic.
- **No Default Grids:** Don't force products into a perfect 4x4 grid. Mix sizes—make some products 2-columns wide to highlight "Staff Picks."
- **No Hard Dividers:** If you feel the urge to draw a line, increase the whitespace or change the background color of the next section instead.

---

## 7. Spacing & Roundedness
- **Roundedness:** Use `sm` (`0.125rem`) or `none` (`0px`) for buttons and containers to maintain a high-fashion, "architectural" feel. Avoid rounded `lg` or `xl` as they feel too "app-like" and casual.
- **The 8px Grid:** While the layout is asymmetrical, the underlying spacing should follow 8px increments to ensure mathematical harmony.