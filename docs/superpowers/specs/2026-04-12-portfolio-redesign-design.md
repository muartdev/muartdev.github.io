# Portfolio Redesign Design

Date: 2026-04-12
Project: `muartdev.github.io`
Status: Approved direction, ready for implementation planning after review

## Summary

This redesign will reposition the portfolio from a tasteful personal homepage into a sharper product-focused portfolio for Murat: a Computer Engineering student who ships real products across iOS, web, and backend.

The chosen direction is:

- Primary signal: `product engineer`
- Secondary signal: `designer-minded developer`
- Tertiary signal: `freelancer / collaborator`

In practice, the site should feel more intentional, more hireable, and more evidence-driven without losing visual taste.

## Problem

The current site is clean and pleasant, but it undersells Murat in three ways:

1. It reads more like a personal aesthetic statement than a strong professional positioning page.
2. It lists projects, but does not prove enough product depth, execution quality, or real-world signals.
3. It spreads attention evenly instead of creating a clear first impression for employers, collaborators, and freelance clients.

The result is a page that is visually decent but strategically weak.

## Goals

- Make the first screen communicate that Murat builds real products, not just nice interfaces.
- Use a more convincing project presentation format with stronger proof and outcomes.
- Keep the visual language refined and distinctive, but less generic and less “template-clean”.
- Support three outcomes at once:
  - internship / junior job opportunities
  - freelance / collaboration inquiries
  - personal brand and network growth
- Improve narrative clarity so GitHub, CV, and portfolio all tell the same story.

## Non-Goals

- Turning the site into a loud agency landing page
- Building a heavy multi-page marketing website
- Adding fake metrics, fake testimonials, or inflated claims
- Over-explaining every project with long technical essays on the homepage

## Audience Priority

The homepage should optimize for these visitors in this order:

1. Recruiters or founders deciding whether Murat looks like a serious junior/product engineer
2. Technical people checking taste, clarity, and project depth
3. Potential freelance collaborators looking for someone who can ship end to end

## Positioning Statement

The site should communicate a version of this message:

> I build thoughtful digital products across iOS, web, and backend, with attention to product feel, structure, and shipping quality.

This should feel more concrete than poetic. Copy should still sound personal, but always land on capability, ownership, and shipped work.

## Visual Direction

### Core direction

Use a `product-first, taste-forward` aesthetic:

- editorial spacing and typography discipline
- stronger hierarchy and contrast
- less reliance on soft glass cards
- fewer decorative gradients
- more deliberate composition

### Desired feel

- calm
- modern
- capable
- selective
- product-minded

### Avoid

- generic startup gradients
- over-rounded “template” cards everywhere
- copy that sounds vague or overly precious
- overly minimal sections that feel empty instead of intentional
- overly salesy freelancer language above the fold

## Content Strategy

The homepage should not try to say everything at once. It should do this sequence:

1. State who Murat is and what kind of work he does
2. Prove range with concrete, shipped-product signals
3. Show selected projects in a more case-study-like structure
4. Explain how he works and why that matters
5. Convert the visitor into contact, CV view, GitHub click, or deeper interest

## Information Architecture

The page should be reorganized into these sections:

1. Header
2. Hero
3. Proof strip
4. Featured work
5. Selected projects
6. Working style
7. About / stack
8. Contact CTA
9. Footer

## Section Design

### 1. Header

Purpose:
Keep navigation simple and professional while preserving language/theme toggles.

Requirements:

- compact sticky header
- stronger brand treatment than the current version
- navigation should prioritize `Work`, `About`, `Contact`
- include one utility CTA if spacing allows:
  - `CV`
  - or `GitHub`

### 2. Hero

Purpose:
Deliver the clearest possible first impression in under five seconds.

Requirements:

- one stronger headline centered on product-building capability
- one supporting paragraph that connects iOS, web, backend, and product feel
- primary CTAs:
  - `See selected work`
  - `Download CV` or `View GitHub`
- short credibility signals directly in or below hero
- layout should feel more composed and less split into “main copy + random side note”

Recommended copy direction:

- less “I like calm interfaces”
- more “I build thoughtful, production-ready products”

### 3. Proof Strip

Purpose:
Add immediate evidence after the hero.

Content examples:

- shipped iOS + web projects
- deploy and release experience
- subscriptions / backend integrations / CMS / Supabase / StoreKit
- English and Turkish

Design notes:

- this should feel like a confidence layer, not a stats section
- use concise proof chips or short statement blocks

### 4. Featured Work

Purpose:
Give one flagship project room to prove product depth.

Recommended lead project:

- `MindShelf`

Required structure:

- what it is
- what Murat built
- why it matters
- stack / product signals
- repo link
- reserve visual space for a later case study link, but do not require it in the first implementation pass

This section should be more than a card. It should feel like the clearest proof of product thinking and execution.

### 5. Selected Projects

Purpose:
Show breadth without becoming a long repo list.

Candidate projects:

- MindShelf Web
- VogeRidersTR
- System Monitor
- Mind API
- FoodSuggest
- portfolio itself only if it adds value, not as filler

For each project, include:

- short label
- one-line purpose
- what kind of work Murat owned
- repo or live link

Design notes:

- move away from plain table/list presentation
- create cleaner modular rows with clearer hierarchy

### 6. Working Style

Purpose:
Translate Murat’s taste into a professional working method.

Suggested themes:

- shapes the product, not just the UI
- works across interface, backend glue, and shipping
- values clarity, restraint, and coherent execution

This section should make “designer-minded developer” feel like a strength, not fluff.

### 7. About / Stack

Purpose:
Keep personal context and technical range visible without making this the main story.

Requirements:

- shorter than current version
- tighter wording
- stack grouped by role, not by buzzword volume
- emphasize practical range:
  - frontend
  - Apple
  - backend / deployment

### 8. Contact CTA

Purpose:
Convert all three audience types with a cleaner final ask.

Requirements:

- one stronger closing statement
- make it clear Murat is open to opportunities, collaborations, and thoughtful product work
- include direct actions:
  - email
  - GitHub
  - X
  - CV if practical

Tone:

- confident
- warm
- not needy

## Copy Principles

- Write like a thoughtful builder, not a branding agency.
- Prefer concrete capability over abstract personality.
- Keep the tone personal, but every section should still move toward proof.
- Remove lines that are aesthetically nice but strategically weak.
- Keep bilingual support, but make both language versions feel equally sharp.

## Interaction and Motion

- retain subtle reveal motion
- reduce motion that feels ornamental
- make hover states cleaner and more intentional
- preserve theme toggle and language toggle
- keep performance strong because this is a static portfolio

## Responsive Behavior

- mobile hero must keep headline, proof, and CTA strong above the fold
- avoid stacked layouts that feel like unrelated cards
- featured project must remain readable and premium on small screens
- contact actions should still be easy to tap and not become cluttered

## Content Priorities for Implementation

During implementation, prioritize these content improvements over surface styling:

1. stronger headline and intro copy
2. better project framing
3. proof signals near the top
4. cleaner section hierarchy
5. better CTA strategy
6. final visual polish

## Constraints

- single-page static site
- existing language toggle should remain
- existing dark mode should remain
- should work well without adding heavy dependencies
- should be implementable inside the current `index.html` architecture unless restructuring becomes clearly worth it

## Risks

- If the page becomes too product-focused, it can lose personality.
- If it leans too editorial, it will still undersell employability.
- If too many projects are shown with equal weight, the page will feel noisy and unfocused.

The implementation should keep `MindShelf` as the main anchor and use the rest to support range.

## Success Criteria

The redesign is successful if a first-time visitor quickly understands:

- Murat ships real products
- Murat has both taste and technical range
- Murat is a credible internship, junior, freelance, or collaboration candidate
- The site feels more distinctive and more strategic than a typical student portfolio

## Implementation Direction

When implementation planning starts, the redesign should focus on:

- restructuring the hero
- replacing the side-note pattern
- adding a proof layer near the top
- upgrading project presentation into stronger product storytelling
- tightening About and Contact copy
- improving hierarchy, spacing, and visual rhythm across the page

## Assumptions

- Default priority order is:
  - `product engineer`
  - `designer-minded developer`
  - `freelancer / collaborator`
- The homepage remains a single-page portfolio.
- Existing projects are enough to support this narrative without inventing new case studies.
