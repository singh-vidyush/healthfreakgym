# Design System Strategy: Kinetic Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Kinetic Editorial."** 

We are moving away from the "standard gym app" template of heavy shadows and rigid grids. Instead, we are treating the UI like a high-end, motion-focused fitness magazine. The experience must feel fast, expensive, and intentional. We achieve this through **Kinetic Asymmetry**—using the bold `lexend` display type to break out of containers—and **Tonal Depth**, where the energy of the vibrant orange (#FF4500) is balanced by sophisticated, layered blacks. This is not just a utility; it is a performance tool.

---

## 2. Colors: The High-Voltage Palette
Our palette is rooted in high-contrast extremes. We use `primary` (#FFB5A0/Orange tones) as a "heat map" to draw the eye to action, while the `surface` levels provide a deep, immersive environment.

### The "No-Line" Rule
**Standard 1px borders are strictly prohibited.** To section content, you must use background color shifts. For example, a `surface-container-low` (#1B1B1B) section should sit directly against a `surface` (#131313) background. This creates a seamless, modern flow that feels engineered rather than "boxed in."

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. 
- **Base:** `surface` (#131313)
- **Secondary Content:** `surface-container-low` (#1B1B1B)
- **Interactive Cards:** `surface-container-high` (#2A2A2A)
- **Floating Modals:** `surface-bright` (#393939)

### The "Glass & Gradient" Rule
To elevate the "High-Energy" feel, use **Glassmorphism** for floating navigation bars or overlay cards. Use `surface-container-highest` at 60% opacity with a `backdrop-blur` of 20px. 
**Signature Texture:** For Hero CTAs, use a linear gradient: `primary` (#FFB5A0) to `primary-container` (#FF5625) at a 135-degree angle. This mimics the "glow" of high-end gym lighting.

---

## 3. Typography: Athletic Authority
We use a dual-font system to balance "Athletic Power" with "Digital Precision."

*   **Display & Headlines (Lexend):** This is our "Athletic" voice. `lexend` is wide and stable. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero headlines to create a sense of massive physical presence.
*   **Body & Labels (Inter):** This is our "Professional" voice. `inter` provides maximum readability for workout data, reps, and timers.
*   **Hierarchy Note:** Use `headline-lg` in all-caps for section headers to evoke the feeling of stadium signage.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "soft" for a high-energy brand. We define depth through **Tonal Layering**.

*   **The Layering Principle:** A card does not need a shadow to be seen. Place a `surface-container-highest` card on a `surface-container-lowest` background. The 4-5% shift in hex value is enough for the eye to perceive a "lift."
*   **Ambient Shadows:** If a floating element (like a FAB) requires a shadow, use a blurred version of `on-secondary-fixed-variant` (#872101) at 10% opacity. This makes the shadow feel like "ambient orange light" reflecting off the floor, rather than a grey smudge.
*   **The "Ghost Border" Fallback:** For accessibility in form fields, use `outline-variant` (#5D4038) at **15% opacity**. It should be felt, not seen.

---

## 5. Components: Precision Engineering

### Buttons
*   **Primary:** `primary-container` background, `on-primary-container` text. 0.25rem (sm) corner radius. Use `title-md` for button text.
*   **Secondary (Ghost):** No background. `outline` (#AD887E) ghost border at 20% opacity. 
*   **The Kinetic State:** On hover/active, buttons should scale to 98% to feel "under pressure."

### Cards & Lists
*   **Forbid Dividers:** Never use a line to separate list items. Use `8` (2rem) of vertical space or a subtle shift from `surface-container-low` to `surface-container-high`.
*   **Data Visualization:** Use `tertiary` (#A5C8FF) for "recovery" or "rest" metrics to provide a cool visual break from the high-energy orange.

### Input Fields
*   **State:** Default state uses `surface-container-highest`. Focus state transitions the background to `surface-bright` with a 2px `primary` bottom-border only. This maintains the "Editorial" look.

### Fitness-Specific Components
*   **The Pulse Meter:** A custom component using a `primary` to `primary-container` radial gradient to visualize heart rate zones.
*   **Progress Sprints:** Thin, 4px tall bars using `surface-variant` for the track and `primary` for the progress, with no rounded caps (keep them sheer/rectilinear for speed).

---

## 6. Do's and Don'ts

### Do:
*   **Use Intentional Asymmetry:** Let images of athletes bleed off the edge of the screen.
*   **Exaggerate White Space:** Use the `24` (6rem) spacing token between major sections to let the design breathe.
*   **Color-Code Intensity:** Use `primary` for high-intensity zones and `tertiary` for yoga/recovery zones.

### Don't:
*   **Don't use 100% Black:** Avoid `#000000` for backgrounds; use our `surface` (#131313) to allow for depth layering.
*   **Don't use Rounded Corners > 12px:** We are "Athletic and Modern." High roundedness (pills) feels too "soft." Stick to `sm` (0.125rem) and `md` (0.375rem) for a precision-machined look.
*   **Don't Over-Animate:** Transitions should be fast (200ms) and linear-out. No "bouncy" or "cute" easing. This is a high-performance system.