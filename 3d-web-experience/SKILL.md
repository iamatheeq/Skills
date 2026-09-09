---
name: 3d-web-experience
description: Build and review production-quality interactive 3D, animated and cinematic experiences for Vite + React applications using Three.js, React Three Fiber, Drei, GLB/glTF, GSAP, Blender, WebGL/WebGPU and optional physics.
---
# 3D Web Experience

## Project Adoption
1. Inspect the existing React/Vite architecture before changing it.
2. Preserve existing design-system, typography and theme tokens.
3. Decide whether 3D genuinely improves the requirement.
4. Prefer Three.js + React Three Fiber for React web 3D.
5. Use Drei for common helpers.
6. Use GLB/glTF for web 3D assets and Blender for authoring/preparation.
7. Use GSAP for advanced choreography when its current license fits the project.
8. Add physics only when physics is actually required.
9. Provide desktop/tablet/mobile behavior and reduced-motion behavior.
10. Measure performance on real devices.

## Architecture
Keep normal UI and 3D concerns separate:
- React: UI, business state, accessibility and forms.
- R3F/Three.js: scene, camera, lights, models and 3D interaction.
- Animation layer: GSAP/timelines or frame-based R3F animation.
- Assets: optimized GLB/glTF.

Prefer focused components such as `HeroScene`, `CameraRig`, `LightingRig`, `ProductModel`, `PostProcessing`, and `InteractionController`.

Avoid one giant Canvas/component containing the entire application.

## Cinematic Rules
Think in shots: establish → approach → reveal → transition.
Control camera composition, lighting, depth, timing, easing and post-processing.
Animation must communicate hierarchy or narrative; do not add motion merely for spectacle.

## Performance
Optimize geometry and textures; lazy-load heavy scenes; cap device pixel ratio; avoid unnecessary React renders and expensive `useFrame` work; reduce effects/object counts on mobile; dispose dynamically replaced resources; provide loading/error states.

## Responsive + Accessibility
Do not simply scale desktop 3D down. Adapt camera, scene complexity, interaction and effects.
Critical information must remain available as semantic HTML. Support keyboard/touch interaction, focus, readable text, and `prefers-reduced-motion`.

## Do / Don't
### Do
- Reuse existing UI/design tokens.
- Use portable GLB/glTF assets.
- Keep 3D modular.
- Use progressive WebGPU adoption when beneficial.
- Validate performance and accessibility.

### Don't
- Don't add 3D where HTML/CSS is better.
- Don't put critical content only inside WebGL.
- Don't use uncontrolled per-frame React state.
- Don't ship unnecessarily huge assets.
- Don't make the application dependent on a proprietary hosted 3D service without a clear reason.

## Delivery
When implementing, provide architecture, packages, files/components, asset requirements, responsive behavior, performance, accessibility, testing and licensing notes.
