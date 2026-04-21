# Motion Wall Portfolio Redesign Design

Date: 2026-04-21
Project: `muartdev.github.io`
Status: Approved direction, awaiting user review before implementation planning

## Summary

This redesign evolves the current editorial portfolio into a more memorable version built around two new ideas:

1. a motion-led hero with a hybrid mascot/object
2. a dark textured proof wall inspired by portfolio presentation boards and logo sheets

The site should still feel clean and intentional, but it should now carry more personality and visual memory.

## Problem

The current site is quieter and cleaner than before, but it still has two gaps:

1. it does not create a strong visual hook in the first screen
2. it does not yet turn shipped work into a more cinematic proof moment

The user explicitly likes:

- the animated character/object feel from the first reference
- the dark, textured wall feeling from the second reference

So the next iteration should keep the minimal editorial structure while introducing a stronger visual identity.

## Goals

- Add a distinctive animated hero element that feels crafted and memorable
- Add a dark proof wall section that feels tactile and visually strong
- Keep the rest of the site restrained so the motion and proof moments feel intentional
- Preserve the professional positioning:
  - product engineer first
  - designer-minded developer second
  - freelancer / collaborator third
- Keep the implementation lightweight enough for a static GitHub Pages portfolio

## Non-Goals

- Turning the site into a cartoon portfolio
- Using noisy, gimmicky, or excessive 3D effects
- Replacing the whole site with a motion demo
- Adding fake client brands or fabricated logos
- Introducing heavy animation libraries unless absolutely necessary

## Chosen Direction

The approved direction is:

`hybrid mascot + textured proof wall`

That means:

- not a full cute mascot
- not a purely abstract object
- a middle ground that suggests personality without becoming childish

The hero object should feel like a visual identity piece, not an illustration dumped on the page.

## Visual Direction

### Overall feeling

- quiet
- designed
- tactile
- slightly playful
- still credible and sharp

### Composition logic

The page should have stronger contrast between sections:

- top: light, spacious, minimal
- middle: dark, textured, dense proof moment
- lower sections: calm and editorial again

This contrast is what will make the site feel more designed without relying on loud UI tricks everywhere.

## Hero Direction

### Hero structure

The top of the page should become a simple stage:

- minimal top bar
- centered or near-centered animated object
- short greeting / identity line
- one or two short lines of copy
- compact CTA set

The hero should feel more like a visual opening than a standard portfolio intro block.

### Hybrid mascot/object

The object should combine:

- monogram or head-like silhouette
- soft face-like geometry or eye-like forms
- simple rounded construction
- restrained single-accent palette

It should feel adjacent to a mascot, but more like a design system object than a cartoon character.

### Motion behavior

Motion should be idle and tasteful:

- subtle floating
- soft tilt
- gentle blink or eye-state shift

No aggressive bouncing, no fast looping, no game-like behavior.

### Implementation choice

For the first implementation pass, use:

- inline SVG for the hero object
- CSS keyframes for motion

Do not start with canvas, WebGL, or heavy motion libraries.

For the first pass, prefer CSS-only motion. JavaScript-driven animation is out of scope unless a tiny helper is strictly required for blink timing.

## Proof Wall Direction

### Purpose

The proof wall should act as the visual counterweight to the light hero.

It should communicate:

- shipped work
- brand or product breadth
- stronger professional credibility

### Surface style

The wall should feel like:

- dark studio wall
- textured presentation board
- subtle paper / concrete / grain surface

This should not be a flat dark rectangle. It needs tactile depth, but the texture should remain understated.

### Content approach

For the first implementation pass, the wall should contain:

- project names
- product names
- selected work labels
- shipped signals

Because the repo does not currently include a ready logo system, do not fabricate logos. Use refined text marks and structured layout first.

The first pass should treat the proof wall as a text-mark composition, not a real client-logo board.

### Layout

The proof wall should use a grid with enough spacing to feel curated.

Good content candidates:

- MindShelf
- MindShelf Web
- System Monitor
- Mind API
- FoodSuggest
- any real shipped names already supported by the repo or user

The grid should feel like a portfolio proof board, not a dashboard.

## Page Structure

The redesigned page should use this sequence:

1. Minimal top bar
2. Motion hero
3. Short intro copy / CTA
4. Textured proof wall
5. Selected work list
6. About / stack
7. Contact

This keeps the site simple while giving the strongest visual ideas room to lead.

## Typography

The current monospace/editorial foundation is worth keeping.

Recommended type logic:

- monospace for structure and body rhythm
- Space Grotesk for names and section headings
- Fraunces italic only for selective accent moments

Typography should do most of the work after motion and texture.

## Color Direction

Use mostly restrained neutrals:

- warm light background
- dark charcoal proof wall
- white / off-white text on dark sections

Accent should be limited:

- one electric accent for the hero object

Do not spread accent color everywhere.

## Interaction Rules

- hover states stay minimal
- links can keep subtle directional arrow movement
- motion belongs mainly in the hero object
- the textured wall should feel stable, not animated constantly

If the whole page moves, the concept weakens.

## Technical Constraints

- keep it as a single-page static site
- preserve language toggle
- preserve theme toggle
- avoid heavy dependencies
- keep performance high enough for GitHub Pages and mobile

## Risks

- If the mascot side is too literal, the site can feel childish
- If the proof wall is too busy, it can overpower the rest of the page
- If both sections are too strong at once, the site can lose its clean editorial restraint

So implementation should intentionally keep the rest of the page quiet.

## Success Criteria

The redesign is successful if:

- the hero becomes visually memorable within a second or two
- the site still feels professional and not gimmicky
- the proof wall makes shipped work feel more credible and substantial
- the rest of the page still reads clearly and calmly
- the portfolio feels more “crafted” than a standard student site

## First-Pass Implementation Decisions

To keep scope focused, the first implementation pass should do all of these:

- replace the current plain hero with a motion-led hybrid mascot/object
- add one dark textured proof wall section
- keep the rest of the site relatively simple
- use project names / text marks instead of invented logo graphics
- avoid adding any dependency that is not clearly necessary

And it should explicitly avoid these for now:

- full 3D rendering
- external animation tooling
- fake branding systems
- multiple animated sections competing at once

## Assumptions

- The current live `origin/main` version is the correct implementation base.
- The user wants a more memorable portfolio, not a fully playful mascot site.
- The proof wall can start with project-name composition before any real logo asset set exists.
