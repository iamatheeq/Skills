---
name: typography-system
description: Establish and enforce a reusable, accessible typography system across web, desktop, tablet, mobile and native-platform projects, while asking the user for font selection when no approved font exists.
---
# Typography System

## Project Adoption
1. Inspect existing fonts/tokens before changing anything.
2. Preserve an established typography system unless replacement is requested.
3. If no font is defined, ask the user to select/approve a font.
4. Ask whether one family or separate body/display families are wanted.
5. Check licensing, embedding, Unicode coverage and loading strategy.
6. Define semantic roles before component-specific styling.
7. Test responsive, accessibility and localization behavior.

## Font Selection Questions
Ask:
- Which font/family should be used?
- One family or body + display?
- Is a licensed brand font available?
- Self-host or hosted font?
- Offline requirement?
- Required languages/scripts?
- Variable font required?

If recommendations are requested, compare readability, coverage, weights, variable-font support, performance and licensing.

## Standard Semantic Roles
Use:
`display-xl`, `display-lg`, `display-md`, `h1`, `h2`, `h3`, `h4`, `body-lg`, `body`, `body-sm`, `label`, `caption`, `code`.

Each role defines family, size, weight, line-height and letter-spacing.

## Cross Platform
Keep semantic hierarchy consistent, but allow platform-native sizing/scaling:
- Web: responsive CSS and zoom.
- iOS: respect Dynamic Type.
- Android: respect user font/display scaling.
- Windows/macOS/Linux: use robust fallback stacks and platform-aware rendering.
- Mobile/tablet: prioritize readable wrapping and touch context.

## Accessibility + Localization
Support zoom/text scaling, reduced motion for animated text, RTL, CJK, Indic scripts and long translations. Never assume one Latin font covers every language.

## Tailwind CSS v4+
Use CSS-first tokens with `@theme` and semantic utilities. Example:
```css
@import "tailwindcss";
@theme {
  --font-sans: "Inter", ui-sans-serif, system-ui, sans-serif;
  --text-body: 1rem;
  --text-body--line-height: 1.5;
}
```
Avoid scattering arbitrary typography values when a semantic token exists.

## Do / Don't
### Do
- Do ask for font selection when undefined.
- Do verify font licensing.
- Do use semantic typography tokens.
- Do support responsive sizing and accessibility.
- Do preserve readable HTML text in 3D experiences.

### Don't
- Don't silently choose a brand font.
- Don't force identical pixel values onto every platform.
- Don't load unnecessary weights.
- Don't put critical text only inside WebGL.
- Don't sacrifice readability for cinematic effects.

## Review
Check font approval, license, hierarchy, responsive behavior, fallback, localization, accessibility and Tailwind v4+ token usage.
