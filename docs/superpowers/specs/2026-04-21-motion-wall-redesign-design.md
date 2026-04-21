# Motion-Led Editorial Portfolio Redesign

Date: 2026-04-21
Project: `muartdev.github.io`
Status: Revised direction approved in chat, awaiting user review before implementation planning

## Summary

This redesign resets the current broken draft and rebuilds the portfolio around two stronger ideas:

1. motion that lives in typography, spacing, and signal elements instead of a mascot
2. a dark textured proof wall that acts as the only major visual contrast moment

The result should feel sharper, more mature, and more controlled than the previous attempt.

## Problem

The last draft failed for two reasons:

1. the moving mascot pushed the site toward a toy-like feeling
2. the proof wall became visually disconnected from the rest of the page

The user feedback is now explicit:

- do not use the mascot direction
- do not keep the current motion style
- keep the idea of movement, but make it smarter and more design-led
- keep the textured wall feeling, but integrate it into a cleaner page

## Goals

- rebuild the hero from scratch
- keep motion, but move it into type, rhythm, and layout choreography
- preserve a strong, tactile dark proof wall
- make the whole page feel intentional instead of decorative
- keep the site static, lightweight, and GitHub Pages friendly

## Non-Goals

- no mascot
- no face-like hero illustration
- no bouncy or cute motion language
- no fake client logos
- no heavy animation libraries
- no over-designed gradients or glass effects

## Chosen Direction

The approved direction is:

`motion-led editorial hero + textured proof wall`

That means:

- the hero becomes typographic first
- the motion becomes structural instead of illustrative
- the proof wall stays strong, but only as one controlled contrast section

## Visual Direction

### Overall feeling

- editorial
- minimal
- sharp
- tactile
- product-minded
- quietly premium

### Section rhythm

The page should deliberately alternate intensity:

- top: light, open, typographic, motion-led
- middle: dark, dense, textured proof moment
- lower sections: clean editorial lists again

This rhythm should create identity without making every section loud.

## Hero Direction

### Hero structure

The first screen should feel like a designed spread:

- minimal top bar
- oversized name and role composition
- short, strong positioning sentence
- restrained proof chips
- compact CTA row
- one motion-led signal element

### Motion language

Motion should come from layout and type, not from a character.

Good candidates:

- a slow sliding signal rail
- a horizontally moving status strip
- staggered hero reveals
- gentle directional shifts on CTAs

Bad candidates:

- bouncing objects
- blinking faces
- floating mascot parts
- motion that demands attention every second

### Hero signal element

The main motion device should be a slim, intelligent element near the hero:

- a line of repeated signals
- a moving strip with product phrases
- a calm ticker-like rhythm
- or a rail that drifts across a masked viewport

Possible copy for the motion rail:

- `shipping across iOS / web / backend`
- `selected work / live products / real systems`
- `product engineer / designer-minded developer / builder`

The rail should be readable enough to feel crafted, but subtle enough to not dominate the hero.

## Proof Wall Direction

### Purpose

The proof wall should turn shipped work into a stronger credibility moment.

It should communicate:

- real projects
- product breadth
- production signals
- stronger professional weight

### Surface style

The wall should feel like:

- a dark studio board
- a textured presentation surface
- a subtle paper / concrete / grain composition

It should feel tactile, but still restrained.

### Content treatment

The wall should use real project names and product names only.

Do not invent logos.
Do not fake client branding.

Instead, use:

- large and small text-mark hierarchy
- varied scale
- deliberate spacing
- occasional outline or contrast treatment

The proof wall should feel curated, not randomly tiled.

## Page Structure

The redesigned page should use this order:

1. Minimal top bar
2. Motion-led editorial hero
3. Proof chips and CTA
4. Textured proof wall
5. Selected work list
6. Approach / about / stack
7. Contact

## Typography

Typography should carry most of the design.

Recommended type logic:

- IBM Plex Mono for body structure, labels, and proof chips
- Space Grotesk for hero name, section titles, and emphasis
- Fraunces italic only as a rare accent if it actually helps

## Color Direction

Use restrained neutrals:

- warm light background
- charcoal or near-black proof wall
- soft off-white wall text

Accent should be limited to one electric note used in:

- the motion rail
- a rule
- a small signal detail

Do not use the accent everywhere.

## Interaction Rules

- hovers stay quiet
- arrow movement can remain subtle
- motion should mostly live near the hero
- the proof wall should stay stable

If the page starts moving everywhere, the concept fails.

## Technical Constraints

- single-file static site
- preserve language toggle
- preserve theme toggle
- avoid dependencies
- keep mobile layout solid
- prevent overflow and horizontal breakage

## Risks

- if the hero motion is too weak, the redesign feels flat
- if the proof wall is too large or too dark, it can overpower the page
- if the motion rail is badly proportioned, it can look like a generic marquee

So the implementation needs strong layout discipline first, motion second.

## Success Criteria

The redesign is successful if:

- the first screen feels more mature immediately
- the motion feels designed rather than playful
- the proof wall looks intentional and proportionate on mobile
- the rest of the page remains readable and calm
- the portfolio feels closer to a real designer-engineer portfolio than to a student demo

## First-Pass Implementation Decisions

The first implementation pass should:

- remove the mascot and current hero experiment entirely
- rebuild the hero from scratch
- add one clean motion rail or signal strip
- keep the proof chips but integrate them into the new hero rhythm
- rebuild the proof wall so it fits the page cleanly on mobile
- keep the rest of the sections simple

And it should explicitly avoid:

- character graphics
- 3D experiments
- fake logos
- multiple competing motion ideas

## Assumptions

- the current branch is still the correct place to continue work
- the user wants a cleaner, more mature site rather than a playful one
- the proof wall should remain part of the concept, but not dominate the whole portfolio
