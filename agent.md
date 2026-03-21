# AGENT.md — Website Project Operating Guide

## Purpose

This project is a website product and marketing surface.  
The agent’s job is to help design, build, refine, and maintain the site in a way that keeps the experience coherent, elegant, and production-ready.

The agent should optimize for:
- clarity of communication
- strong visual hierarchy
- high-quality implementation
- consistency across sections
- responsiveness
- performance
- preserving the intended brand feel

This is not a scratchpad for random experimentation.
The website should feel intentional.

---

## Product Intro

Product definition:
Flowd is a thinking space built around a single continuous conversation per project. The user talks through ideas, decisions, questions, progress, references, and completed work. An AI agent listens and organizes everything into a living project board in real time. Conversation is the input. The board is the output. They happen simultaneously, side by side.

Core concepts to communicate:
- one continuous conversation per project
- no chat sessions to manage
- AI automatically creates and maintains workstreams
- cards are created from conversation: notes, decisions, questions, todos, links, images, docs
- wrapping up a workstream generates a summary document
- not a chat app with a board attached
- not a board with a chat panel
- one coherent product

Creative direction:
- calm, cinematic, editorial
- premium product storytelling
- centered on a poetic 3D landscape world: pale sky, grassy hills, still water, minimal architecture, subtle atmosphere
- the landscape should feel like project terrain / living memory / workstreams emerging over time
- visually distinct from typical AI SaaS sites
- humane, spacious, quiet, precise

Required sections:
1. Hero
2. Conversation in, structure out
3. Not chat + board
4. One continuous conversation per project
5. Workstreams emerge automatically
6. Cards created from what you say
7. Wrap up into docs
8. Why it feels different
9. Final CTA

Hero requirements:
- large full-screen or near-full-screen landscape visual
- integrated device mockup or UI frame inside the environment
- clear product UI showing thread on one side and board on the other
- large headline over negative sky space
- subtle ambient motion and UI movement
- premium restrained navbar

Motion requirements:
- slow, refined, cinematic
- no bouncy transitions
- use fade, blur, slight translate, soft parallax
- hero should feel alive but calm
- product demo sections should clearly show board updating from conversation

Design requirements:
- responsive desktop/mobile
- large typography
- generous spacing
- sparse but clear copy
- muted palette: pale gray sky, moss/sage greens, straw tones, soft neutrals
- minimal rounded cards and clean UI
- avoid generic SaaS visuals, bright blue accents, or enterprise dashboard styling

Implementation notes:
- use reusable React components for each section
- prioritize clarity of product explanation while preserving strong art direction
- use placeholder assets where needed
- hero may use a prerendered image/video background instead of full realtime 3D if it improves visual quality and performance


## Core principles

### 1. Protect the concept
Do not make changes that weaken the site’s core identity.

Before changing layout, visuals, interaction, or copy, first infer:
- what the site is trying to communicate
- what emotional tone it is aiming for
- what visual system it is using
- what makes it distinctive

Preserve the concept unless explicitly asked to change direction.

### 2. Structure before decoration
Do not add effects, animations, gradients, cards, or components unless they support the structure and message.

Prioritize:
1. information hierarchy
2. layout rhythm
3. spacing
4. typography
5. interaction clarity
6. motion polish

### 3. Keep the site coherent
Every new section or component must feel like it belongs to the same website.

Match:
- spacing scale
- border radius system
- typography system
- tone of copy
- motion language
- visual density
- color usage

Do not introduce unrelated styles.

### 4. Prefer refinement over reinvention
When improving the site, first try:
- better spacing
- better alignment
- better hierarchy
- simpler code
- clearer copy
- more consistent styling

Do not rewrite large parts of the site unless necessary.

### 5. Make the website feel premium
Default toward:
- restraint
- clarity
- breathing room
- fewer, stronger elements
- careful typography
- smooth motion
- polished responsive behavior

Avoid:
- visual clutter
- unnecessary components
- generic SaaS styling
- excessive effects
- over-explaining
- inconsistent spacing
- accidental “template” feeling

---

## Related product source

Webapp project path (source of truth):
`/Users/ariax/Documents/GitHub/80HD`

This website is built for that webapp.
The webapp is the source of truth for product UI, screen structure, interaction patterns, visual styling, states, and behavior. It is also the source for Design system / style tokens for website. 

When building website product screens, mockups, demos, or reconstructed UI:
- use screens from the webapp project
- match the webapp exactly
- do not invent alternate UI patterns
- do not restyle the product for the marketing site
- do not simplify product behavior in a way that changes meaning
- do not create “inspired by” versions of the interface

If the website needs a product screen shown in a hero, feature section, demo block, mockup, animation, or visual composition, the agent should rebuild it directly from the webapp project and follow that project strictly.

The website may frame, crop, animate, or place the product UI in a marketing context, but the product UI itself should look and behave exactly like the webapp.

If there is any conflict between the current website and the webapp project, follow the webapp project.



## Source of truth

When reconstructing context or making decisions, use this order:

1. Current project files
2. Design system / style tokens / reusable components in the repo
3. Existing page structure and implemented behavior
4. Explicit user instructions in the current task
5. Earlier notes or docs in the repo
6. Chat history

Chat history is not the source of truth if the files say otherwise.

---

## What this agent should do

The agent may help with:

### Design-aware implementation
- build sections and pages
- refine layout and hierarchy
- improve responsive behavior
- improve typography and spacing
- implement polished interactions
- preserve visual consistency

### Frontend engineering
- create reusable components
- simplify overly complex UI code
- improve maintainability
- fix styling bugs
- fix layout bugs
- fix responsiveness issues
- improve performance where practical

### Product communication
- sharpen landing page structure
- refine feature presentation
- improve CTA hierarchy
- reduce clutter
- clarify copy flow
- better align visuals and messaging

### QA and polish
- inspect broken layouts
- catch spacing inconsistencies
- fix overlap / overflow / stacking problems
- ensure mobile quality
- ensure sections connect cleanly
- reduce rough edges before shipping

---

## What this agent should not do

### Do not invent a new brand direction without being asked
If the site already has a clear visual identity, work within it.

### Do not overwrite user-authored copy carelessly
Refine only when needed. Preserve tone and meaning.

### Do not add trendy effects just because they are possible
Motion, 3D, blur, gradients, sticky scroll, parallax, and glass effects must serve the concept.

### Do not over-engineer
Prefer simple, legible solutions over clever abstractions.

### Do not silently change product meaning
If a headline, feature description, or layout change alters the product story, flag it.

### Do not break responsiveness while optimizing desktop
Mobile quality is required.

### Do not treat the site like an app dashboard
For website work, prioritize presentation, narrative, and conversion clarity.

---

## Working style

### For any non-trivial task, follow this process

#### 1. Read first
Inspect the relevant files and understand:
- page structure
- component relationships
- styling patterns
- animation patterns
- layout system
- content hierarchy

Do not edit blind.

#### 2. Infer intent
Before changing anything, identify:
- what this section is supposed to do
- what feels off
- whether the issue is structural, visual, copy-related, or technical

#### 3. Make the smallest effective change
Prefer precise edits over broad rewrites.

#### 4. Verify after changes
Check for:
- build errors
- broken imports
- layout regressions
- mobile issues
- overlapping content
- inconsistent spacing
- visual mismatch with adjacent sections

#### 5. Summarize clearly
After edits, explain:
- what changed
- why it changed
- any tradeoffs
- anything still unresolved

---

## Website-specific standards

### Layout
- Use consistent container widths
- Use deliberate vertical rhythm
- Keep section spacing generous and intentional
- Avoid cramped compositions
- Avoid arbitrary shifts in alignment from section to section

### Typography
- Respect the project’s font system
- Keep headings clear and strong
- Preserve readable line length
- Avoid overly dense body copy
- Use serif/sans contrast only if it fits the design direction

### Components
- Reuse existing components when possible
- If creating a new component, make it reusable and stylistically aligned
- Do not create one-off component logic unless necessary

### Motion
- Motion should support hierarchy and feel
- Prefer subtle, smooth transitions
- Avoid noisy animation
- Avoid excessive durations or distracting loops
- Ensure motion does not harm usability

### Responsive behavior
Every change should be checked for:
- desktop
- tablet
- mobile

Especially verify:
- wrapping
- stacking
- overflow
- text readability
- tap targets
- sticky elements
- image cropping
- section padding

### Performance
Prefer:
- optimized images
- minimal unnecessary JS
- lightweight interaction patterns
- avoiding wasteful rerenders
- avoiding huge dependency additions without reason

---

## Copy handling rules

When editing website copy:

### Preserve the intended tone
Possible tones include:
- editorial
- premium
- calm
- technical
- minimal
- poetic
- direct

Match what is already there.

### Improve by subtraction first
Try removing clutter before adding more words.

### Headlines
- should be clear and distinctive
- should not sound generic
- should not be bloated

### Body copy
- should support the headline
- should be easy to scan
- should not repeat what the UI already shows

### CTA copy
- should be specific and intentional
- should fit the site’s tone
- should not sound aggressive unless the brand calls for it

---

## Code quality rules

- Prefer clear component structure
- Keep files readable
- Avoid deeply tangled JSX
- Avoid duplicated layout logic when reusable abstractions are obvious
- Avoid magic numbers unless visually necessary
- Keep class names and variables understandable
- Preserve consistency with existing patterns
- Do not introduce a new framework or major dependency without strong reason

If using animation libraries:
- keep motion centralized and understandable
- avoid stacking multiple systems unnecessarily

If editing CSS / Tailwind:
- preserve the spacing and sizing system
- avoid scattered ad hoc overrides
- avoid fighting the existing design language

---

## When handling landing pages

For landing page work, always think in this order:

1. What is the core promise?
2. Is the hero communicating it clearly?
3. Does the page have a good narrative flow?
4. Are sections distinct but connected?
5. Is the product shown clearly enough?
6. Is the page visually memorable?
7. Is the CTA hierarchy clear?

Do not let feature lists overpower the story.

---

## When handling design-heavy pages

If the site uses strong visuals, 3D, renders, or art direction:

- treat visuals as part of the product story, not decoration
- preserve image quality and composition
- avoid covering key visuals with noisy UI
- make overlays legible but restrained
- maintain atmosphere while improving usability

If choosing between “more dramatic” and “more coherent,” prefer coherent.

---

## If something is unclear

If a task is ambiguous, do not immediately redesign the page.
First determine whether the user likely wants:
- a bug fix
- a polish pass
- a structural redesign
- a copy rewrite
- a new section
- a full visual direction shift

If the requested change would affect brand, layout system, or page narrative, call that out.

---

## Definition of done

A task is not done just because code was changed.

It is done when:
- the implementation works
- the page still feels coherent
- the intended message is clearer or stronger
- the design quality is maintained or improved
- no obvious responsive regressions remain
- the result feels intentional, not merely functional

---

## Preferred mindset

Act like a hybrid of:
- thoughtful frontend engineer
- product-minded designer
- detail-oriented creative director
- careful UX editor

Build with taste.
Refine with restraint.
Protect the concept.