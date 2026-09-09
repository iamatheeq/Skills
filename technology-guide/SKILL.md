---
name: technology-guide
description: Select and compare technologies for Vite + React projects involving 3D, animation, cinematography, graphics, assets, physics, licensing and long-term maintainability.
---
# Technology Guide

## Mission
Answer “what technology should we use?” before implementation.

## Project Adoption
Inspect the current stack first. Identify the actual requirement. Prefer mature, self-hostable technologies, open standards, healthy ecosystems and permissive licenses where practical. Verify current licenses before release.

## Default Choices
- Application/build: React + Vite
- Browser 3D: Three.js
- React 3D integration: React Three Fiber
- Helpers: Drei
- 3D assets: glTF/GLB
- Authoring: Blender
- Advanced animation: GSAP when licensing fits
- Physics: Rapier when needed
- Browser graphics: WebGL with progressive WebGPU adoption
- Alternatives: Babylon.js or PlayCanvas when their engine model better fits the requirement.

## Evaluation Criteria
Compare candidates by:
1. License/commercial terms
2. Maintenance/activity
3. Browser/platform support
4. Performance
5. Bundle/runtime cost
6. Ecosystem
7. Portability
8. Vendor lock-in
9. Migration path
10. Team skill level

## Do / Don't
### Do
- Do recommend technology from requirements.
- Do verify current upstream licensing.
- Do distinguish library licenses from asset licenses.
- Do consider mobile and low-power hardware.
- Do document significant technology decisions.

### Don't
- Don't select a library merely because it is popular.
- Don't claim open-source assets are automatically reusable.
- Don't make proprietary hosted tooling a core dependency without justification.
- Don't assume today's license or API will never change.

## Project Output
Give a recommended choice, alternatives, reasons, trade-offs, license considerations and migration implications.
