# Motion Wall Redesign Plan

Date: 2026-04-21
Branch: `codex/motion-wall-redesign`
Spec: `docs/superpowers/specs/2026-04-21-motion-wall-redesign-design.md`

## Goal

Implement the approved motion-wall direction on top of the current live editorial portfolio without adding dependencies.

## Work

1. Extend the existing visual system in `index.html`
   - keep the current editorial typography and controls
   - add new tokens for the electric hero accent and dark proof wall surface

2. Replace the current plain hero opening
   - build a centered motion stage
   - add an inline SVG hybrid mascot/object
   - animate with lightweight CSS only

3. Add the textured proof wall section
   - use a full-width breakout section
   - create a tactile dark wall with layered CSS texture
   - use real project names and shipped-signal text marks

4. Preserve product-site basics
   - keep language toggle working
   - keep theme toggle working
   - keep the rest of the page clean and readable

5. Verify before finishing
   - inspect for missing translation keys
   - preview locally in the browser
   - check git diff for accidental regressions

## Notes

- First pass stays static-site friendly for GitHub Pages.
- No fake brand logos, no heavy animation libraries, no glassy UI effects.
