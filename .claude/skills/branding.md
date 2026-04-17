# Branding Skill

Apply consistent visual branding to the project's UI: colors, typography, logo/name placement, and tone.

## When to use

Invoke this skill when the user asks to:
- Add or update a logo, app name, or tagline
- Apply a color palette or brand theme
- Ensure consistent fonts and visual identity
- Rebrand or rename the project

## How to apply branding

1. **Identify brand elements** — ask the user for (or infer from existing code):
   - Primary and accent colors
   - App/product name and tagline
   - Logo (URL, emoji, or SVG)
   - Font preferences

2. **Update CSS variables** — centralize brand tokens in `:root` so every component inherits them:
   ```css
   :root {
     --brand-primary:  #<color>;
     --brand-accent:   #<color>;
     --brand-bg:       #<color>;
     --brand-text:     #<color>;
     --brand-font:     '<font-stack>';
     --brand-radius:   <px>;
   }
   ```

3. **Apply name & logo** — update `<title>`, any heading/hero text, and favicon or emoji icon in `<head>`.

4. **Tone consistency** — update button labels, status messages, and placeholder text to match the brand voice (playful, professional, minimal, etc.).

5. **Test visually** — after changes, verify the golden path screens (home/setup, main game/app, win/success) look cohesive.

## Constraints

- Do not introduce new dependencies (external fonts via CDN are acceptable if the user agrees).
- Keep all brand tokens in `:root` — never scatter magic color values through the CSS.
- Preserve existing functionality; branding is purely visual/copy.
