---
name: theme-system
description: Establish and enforce a reusable semantic color and visual theme for 3D web experiences using Tailwind CSS v4+, including light, dark, system and combined modes.
---
# Theme System

## Project Adoption
1. Inspect existing tokens, CSS, Tailwind version and components.
2. Preserve an established theme unless replacement is requested.
3. If no theme exists, ask the user to choose a mode.
4. Ask the user to select/approve the color direction/palette.
5. Define semantic tokens.
6. Map tokens to Tailwind CSS v4+ CSS-first theme variables.
7. Validate contrast and interactive states.
8. Ensure 3D lighting harmonizes with, but is not rigidly coupled to, UI colors.

## Theme Mode Selection
Ask the user to choose:
1. Dark only
2. Light only
3. System only
4. Both light and dark
5. All/advanced: light + dark + system preference + explicit override

Never silently choose a mode.

## Color Selection
If undefined, ask for/offer choices for:
- brand/primary
- accent
- background
- surface
- text
- muted text
- border
- success
- warning
- error
- info

## Semantic Tokens
Use roles such as:
`background`, `surface`, `surface-elevated`, `surface-muted`, `text`, `text-muted`, `border`, `border-strong`, `brand`, `brand-hover`, `brand-active`, `on-brand`, `focus`, `success`, `warning`, `error`, `info`.

Define hover, active, focus, disabled and selected states.

## Tailwind CSS v4+
Prefer:
```css
@import "tailwindcss";
@theme {
  --color-background: oklch(0.98 0 0);
  --color-surface: oklch(1 0 0);
  --color-text: oklch(0.2 0 0);
  --color-brand: oklch(0.55 0.2 280);
}
```
Use semantic utilities rather than arbitrary colors throughout components.

## Accessibility
Check text/control contrast, focus visibility, dark-mode readability and color-blind usability. Never use color as the only state indicator.

## 3D Relationship
Keep UI theme and 3D visual language coherent through controlled relationships among background, environment, key/fill/rim lighting, materials, shadows and post-processing. Do not make every 3D object the brand color.

## Do / Don't
### Do
- Do ask for mode selection.
- Do ask for palette selection.
- Do use semantic tokens.
- Do support system preference and explicit override when selected.
- Do use Tailwind v4+ CSS-first theme tokens.
- Do validate contrast.

### Don't
- Don't invent random per-component colors.
- Don't silently choose light/dark mode.
- Don't mix raw colors with semantic tokens unnecessarily.
- Don't use color alone to communicate status.
- Don't replace an existing brand theme without approval.

## Review
Check mode strategy, palette approval, semantic tokens, interactive states, contrast, Tailwind v4+, component consistency and 3D harmony.
