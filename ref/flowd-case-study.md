# Flowd — Case Study
### A Thinking Space for Non-Linear Minds

---

## Case Study Arc

```
Opening Question → Problem Definition → First Thesis (Flowd v1) →
The Crack → The Pivot → The New System → Architecture →
Key Design Decisions → The Build Process → Reflection → Bigger Thesis
```

JD competency signals marked inline as `[JD: ___]`.

---

## SECTION 0 — THE OPENER (Hero)

**Visual direction:** Full-bleed dark canvas. One line of text resolves slowly, like a thought finding its shape.

> *"An idea doesn't arrive finished. It arrives as a fragment — and it needs somewhere to grow."*

No product screenshot. No logo. Just the question underneath the product.

Below it, a single line:

> **Flowd** — A thinking space for non-linear minds.

---

## SECTION 1 — THE ORIGIN

### Headline:
**"What if the tool thought alongside you?"**

### Narrative Copy:

There is a particular kind of frustration that doesn't come from lack of ideas. It comes from the gap between having an idea and being able to do anything with it.

You've felt it. A half-formed thought at midnight that connects something you read three weeks ago to a problem you're stuck on today. The moment you reach for a tool to hold it, the connection slips. The friction of organizing — of deciding where it goes, what it belongs to, how it relates to everything else — is enough to dissolve what was already fragile.

Most productivity tools are built on an assumption so obvious it goes unexamined: that the person using the tool already knows how to organize themselves. That structure is something the user provides, and the tool holds.

But thinking doesn't work that way. Not for everyone.

For people with limited executive function — with ADHD, with the kind of cognitive wiring that generates ideas in bursts and loses threads mid-sentence — the overhead of managing a tool is not a minor inconvenience. It is the thing that makes thinking feel impossible. Research shows that for people sensitive to interstitial friction, the cost of a single context switch can take up to 15 minutes to recover from. The average neurotypical person recovers in under 10 seconds.

I am one of those people.

Which means I had a personal stake in the question: what would a tool look like if structure emerged from the thinking — instead of the thinking being bent around the structure?

`[JD: User empathy rooted in lived experience]`
`[JD: Ambiguity Navigation — defined own problem space without a brief]`

### Visual Callout:
**[VISUAL 1 — The Gap diagram]**
A spare, almost clinical illustration of two timelines. One: the linear tool model — input → organize → retrieve → act. Two: how non-linear thinkers actually move — burst, fragment, connect, lose thread, burst again. The gap between "connect" and "move forward" is where every existing tool fails. No decoration. The emptiness in the diagram is the point.

---

## SECTION 2 — PROBLEM DEFINITION

### Headline:
**"The real failure is not capture. It's connection and momentum."**

### Narrative Copy:

I spent two weeks doing what I've come to call *behavior archaeology* — not surveying users with questionnaires, but watching myself and other non-linear thinkers in their actual environments. Screenshotting my own desktop at random intervals. Journaling where ideas actually lived versus where I intended them to live. Talking to designers, writers, and researchers about the systems they'd tried and why each one had eventually failed them.

Three patterns emerged.

**The Capture Problem.**
Ideas get captured in whatever surface is nearest — a DM to yourself, a voice memo, a sticky note that will outlast its context. The choice is always: slow down and file it correctly, or catch it now and deal with the filing later. Later never comes. Speed of capture beats quality of storage, every time.

**The Connection Problem.**
This was the deeper one. Ideas that belong together live in different places — a note from six weeks ago that's directly relevant to what you're working on today, a decision from a previous session that reframes something you're about to commit to. Non-linear thinkers don't think in silos, but every tool stores things in silos. The connections that would help you move forward never surface, because nothing is watching for them.

**The Forward Motion Problem.**
Most tools are good at holding things. Almost none are good at helping you move. The question "what should I do next?" is rarely answerable from inside a Notion database. The structure is there, but it's inert. It doesn't think with you. It waits.

The insight that reoriented everything:

> *The problem isn't storage. It's momentum. People don't need a better place to put things — they need something that helps them keep going.*

`[JD: Self-directed research, deep user empathy]`
`[JD: Defining the problem, not just solving the given one — Owner mentality]`
`[JD: Rethinking UI primitives — the reframe already challenges what "productivity tools" are for]`

### Visual Callout:
**[VISUAL 2 — Three Failure Points map]**
A project lifecycle diagram with three clearly marked collapse points: Capture (friction dissolves the thought), Connection (related ideas never find each other), Forward Motion (structure exists but nothing moves). Each failure point carries a real quote from your conversations — short, unattributed, human. Spare and diagnostic. Not a pitch. A finding.

---

## SECTION 3 — FIRST THESIS: DRIFT (v1)

### Headline:
**"My first answer was too obvious."**

### Narrative Copy:

The first version was called Flowd — the idea that thoughts could flowd across a surface rather than be placed precisely. The primary surface was a freeform spatial board: cards of different types — notes, decisions, documents, chat summaries — scattered across an open canvas, draggable, repositionable, owned entirely by the user. Spatial, tactile, yours to arrange.

The AI lived at the edges. A chat drawer collapsed against the side, opened on demand. A separate NOW tab that generated an AI-organized reading of the board — Framing, Open questions, Journey — each section synthesized from what existed on the canvas.

The logic held up on paper. The board as the primary thinking surface. The AI as interpreter and summarizer, reading what the user had built and reflecting it back in structured form. Chat as an on-ramp: talk to Flowd, get a card, place it where it belongs.

I built it in React with a live Claude API integration. Real drag behaviors, real card types, real AI responses. I used it every day for three weeks.

`[JD: Code prototyping — React, live API, real drag interaction from day one]`
`[JD: AI product design — live model integration, not simulated responses]`

### Visual Callout:
**[VISUAL 3 — Flowd v1: THE SPACE]**
Screenshot of the freeform board (Image 1). Cards scattered across the canvas — yellow notes, dark decision cards, blue chat summaries, document cards. The spatial freedom is visible. Below it, a second frame showing the NOW view (Image 2) — AI-organized sections: Framing, Open, Journey. These two states side by side, with the chat drawer marked as collapsed. The full picture of what v1 was.

---

## SECTION 3B — THE INTERMEDIATE STEP

### Headline:
**"Tighter structure. Same problem."**

### Narrative Copy:

Before the full pivot, there was a middle version. I removed the freeform drag — cards no longer floated freely but snapped into a horizontal scroll container, organized by workstream. More legible, less spatially demanding.

But the interaction model was unchanged. The board was still the primary surface. Chat was still a drawer. The user was still the one deciding what went where.

The container structure made the board easier to read. It did not make it easier to maintain. Tidier ≠ automatic. The organizing burden had just been given better furniture.

This iteration taught me something important: I had been treating the symptom, not the cause. The problem wasn't that the board was spatially chaotic. The problem was that the board required the user to be its curator — and curating a board is not thinking.

`[JD: Ambiguity navigation — recognized that structural iteration wasn't solving the right problem]`

### Visual Callout:
**[VISUAL 3B — Flowd v2: container-based board]**
The horizontal scroll layout. Cards in columns, more organized. Chat drawer still visible but secondary. The improvement is visible — and so is the underlying model that hasn't changed.

---

## SECTION 4 — THE CRACK

### Headline:
**"I had been asking all the wrong questions."**

### Narrative Copy:

The NOW view was the tell.

In theory, NOW was the answer to the forward motion problem — an AI-generated synthesis of everything on the board, organized into readable sections: where you are, what's open, how you got here. It was genuinely useful. When I came back to a project after a break, NOW gave me context faster than anything else in the product.

But it was a read surface, not a working surface. You landed on NOW to get oriented, then switched to THE SPACE to do anything with that orientation. Two modes. Two mental contexts. A seam running through every session.

And THE SPACE — even in the container-based version — was still a thing I had to tend. Cards accumulated. Decisions needed placing. Notes needed categorizing. The overhead was lower than a Miro board, but the fundamental job was the same: be the curator of your own thinking in order to think.

*The board was asking me to organize in order to create. But organizing and creating are competing states of mind.*

For a non-linear thinker, that competition is fatal. The moment the tool demands curation, it becomes the reason you leave. Not because you're lazy. Because the cognitive cost of switching into organizational mode while in creative mode is genuinely prohibitive — and then you don't come back.

I had built a tool that was most useful when you used it consistently — and most likely to be abandoned the moment you stopped.

`[JD: Ambiguity navigation — named the fundamental flaw rather than continuing to iterate around it]`
`[JD: Owner mentality — willingness to question the core model, not just its execution]`

### Visual Callout:
**[VISUAL 4 — The Seam]**
A simple diagram showing the NOW → SPACE → CHAT DRAWER movement. Three surfaces, three mode switches, just to do one thing. Each transition marked. The seam is the product's real architecture — and it's visible when you draw it out.

---

## SECTION 5 — THE PIVOT

### Headline:
**"What if the board built itself?"**

### Narrative Copy:

My breakthrough came when I stopped asking how to improve the board and started asking whether the board should be the primary surface at all.

Every version of Flowd had inherited the same assumption from the tools I was trying to replace: that structure is the product, and thinking is what you do to fill it. The board is the destination. The conversation is the road to get there.

What if that was exactly backwards?

The most alive moments in Flowd were never on the board. They were in the chat drawer — when a thought was forming in real time, when a question led somewhere unexpected, when the AI pushed back on something and a better idea emerged from that friction. The board was where thinking went to be preserved. The conversation was where thinking was actually happening.

So: invert it.

What if the user just talked — ideas, decisions, questions, progress, things found, things completed — and an AI agent listened, thought alongside them, and built the board from the conversation in real time? The board becomes the output, not the workspace. It builds itself while you think. The user never curates it.

This isn't a UI adjustment. It's a different theory of what a thinking tool is.

The new model:

> *Conversation is the input. The board is the output. They happen simultaneously, side by side.*

The closest feeling: iMessage with a very smart collaborator who has read everything, remembers everything, and keeps the project organized while you talk. No mode switching. No curation. You think out loud. The system keeps up.

`[JD: Rethinking UI primitives — questioning the inherited assumption that structure is the primary surface]`
`[JD: AI product design intuition — designing around what AI actually does well: reading, remembering, connecting across time]`

### Visual Callout:
**[VISUAL 5 — The inversion diagram]**
Three columns showing the model shift. Column 1: Flowd v1 — board is primary, chat is drawer, NOW is a separate tab, user curates everything. Column 2: Flowd v2 — board is tidier but model unchanged. Column 3: Flowd — conversation is primary, board auto-generates alongside it, user curates nothing. The arrow of the whole story runs left to right. Red markers on columns 1 and 2 at the points where user effort is required. Column 3 is clean.

---

## SECTION 6 — THE NEW SYSTEM

### Headline:
**"Designing for a system that understands where you are."**

### Narrative Copy:

Flowd's interface is deliberately quiet: a chat view and a workspace board, side by side. You mainly talk. Sometimes you glance at the board. The board is never the job — it is the byproduct of the job.

What is complex is what the AI is doing while you work.

I designed the system around three behaviors:

**Recognition.**
The AI reads the conversation not just to respond, but to understand. When a topic shifts, when a new idea surfaces that connects to something said sessions ago, when a decision is being made — the AI recognizes these patterns and acts on them. This is the connection engine. It's what Flowd never had.

**Materialization.**
When recognition fires, content appears on the board — softly. Cards materialize without interrupting the conversation. The board grows at the periphery of attention, not in the center of it. The experience: the system is quietly keeping up.

**Contextual Continuity.**
Because the AI has read everything — every message, every card — it can always hold the implicit question underneath any conversation: *where are we, and what matters right now?* This is not search. Not a summary. It is active awareness. The AI knows what's unresolved. It knows what connects. It surfaces those things without being asked.

These three behaviors map directly to the three failure points from the research:

- Recognition → solves the Connection Problem
- Materialization → solves the Capture Problem
- Contextual Continuity → solves the Forward Motion Problem

`[JD: Agentic experience design — three distinct AI behaviors, each designed separately]`
`[JD: Understanding model boundaries — recognition has explicit fallback states for ambiguity]`

### Visual Callout:
**[VISUAL 6 — System behavior diagram]**
Three frames of the same project at different moments. Frame 1: early conversation, board sparse. Frame 2: mid-conversation, first cluster has formed from an uninterrupted thread. Frame 3: mature project — multiple workstreams on the board, conversation still flowing, none of the board content placed by the user. Arrow chain below: Recognition → Materialization → Board State. The user is never in that chain.

**[VISUAL 7 — Core UI: chat + workspace]**
Clean side-by-side product view. Left: workspace board with auto-generated cards. Right: chat view, active conversation. The relationship visible — what's being talked about is reflected in the board — but the chat never pauses for the board to update. One coherent product, not two tools next to each other.

---

## SECTION 7 — THE ARCHITECTURE

### Headline:
**"I wrote the PRD. Then I wrote the soul."**

### Narrative Copy:

As the product model solidified, I needed two documents that don't usually coexist.

The first was a technical AI system architecture PRD — the recognition engine, the materialization rules, the workstream graph model, the memory architecture. Precise, structured, written to anticipate edge cases and guide implementation. The system as mechanism.

The second was SOUL.md.

SOUL.md is a character specification for Flowd's AI — not what it can do, but how it should be. How it should behave as a thinking partner across different kinds of projects. A messy early-stage exploration needs a different posture than a focused execution sprint. A solo creative project has different rhythms than a technical planning session. The AI needs to know the difference — and calibrate accordingly.

Writing SOUL.md required articulating something that had been implicit throughout the entire design process: **the AI in this product is not a feature. It is a collaborator. And collaborators need a defined perspective — not just capabilities.**

A collaborator without perspective is autocomplete. A collaborator with the right perspective is the reason you trust the product.

When should the AI speak up versus stay quiet? When has it earned the right to reorganize something? How does it hold uncertainty without breaking the user's confidence in it? These are not engineering questions. They are design questions. And they have to be answered before a single line of logic is written.

`[JD: AI believer — thinking at the model-character level, not just the interface level]`
`[JD: Trust/safety — when AI acts vs. waits is a design decision]`
`[JD: End-to-end ownership — PRD + architecture + AI character spec, one designer]`

### Visual Callout:
**[VISUAL 8 — SOUL.md excerpt]**
A typeset excerpt from the actual SOUL.md. Dark background, serif font. 5–6 lines capturing the AI's stated posture — something about uncertainty, or when it chooses to stay quiet. The contrast between the form (technical spec) and the register (almost philosophical) is intentional. This is a different kind of design artifact.

**[VISUAL 9 — PRD architecture diagram]**
Conversation Layer → Recognition Engine → Workstream Graph → Board State. Clean system diagram. Technical, precise. Proof of systems thinking, not just screen design.

---

## SECTION 8 — KEY DESIGN DECISIONS

### Headline:
**"Every choice was an argument."**

---

### A — The Board Is Not the Job

The most important design decision in Flowd is one the user never sees made: they don't manage the board.

This sounds simple. It isn't. It means refusing the entire interaction model that Miro, Notion, and almost every spatial thinking tool is built on — the model where the board is the primary surface, and the user's job is to tend it.

I spent time in Flowd v1 watching what actually happened when people used a freeform spatial board. Cards accumulated fast. Within a few sessions, the canvas was dense — notes, decisions, summaries, images, all floating at roughly equal visual weight, each one isolated from the others. There was no relation between them, no sense of a project moving. It felt less like a thinking space and more like a parking lot. A place to leave things, not work with them.

*Miro fails because it's too granular and too arbitrary.* Every card stands alone. The whole board doesn't read as a project — it reads as a collection of objects. To understand the state of the work, you have to read each card individually and reconstruct the project in your head. For a non-linear thinker who's already managing too much cognitive load, that reconstruction cost is prohibitive. You look at the board, feel overwhelmed, and leave.

*Notion fails for the opposite reason.* It's rigid and hierarchical — pages inside pages, structures inside structures. Creating a clean space for a new idea feels good in the moment, but three days later that page is buried. You'd have to remember it exists, navigate to it, open it. It's hidden by design. The flexibility is real, but the discoverability is not.

The model Flowd needed was neither. Not arbitrary scatter, not hidden hierarchy. Something fluid — a system that, as Mercury OS put it, responds to the intentions of its user rather than asking the user to modify their thinking around arbitrary containers.

In Flowd, the board builds itself from the conversation. Cards are grouped by workstream automatically — not because the user filed them, but because the AI recognized the thread they belong to. The user never drags a card, never decides a column, never categorizes anything. They just talk. The board is the system's output, not their responsibility.

*The board is not the job. It's proof that the job is happening.*

`[JD: Rethinking UI primitives — rejected the inherited assumption that users should manage their own board]`
`[JD: AI product design intuition — the AI does the work that every other tool offloads to the user]`
`[JD: Ambiguity navigation — naming the failure modes of the reference category (Miro, Notion) before designing past them]`

### Visual Callout:
**[VISUAL 10 — Three mental models compared]**
Three columns: Miro (freeform, granular, arbitrary — cards scattered, no thread, overwhelming), Notion (hierarchical, rigid, hidden — pages inside pages, buried), Flowd (workstream-grouped, auto-built, conversation-primary). Not a competitive teardown — a conceptual diagram showing three different theories of what a project surface is for.

---

### B — One View

The other decision that shaped everything was surface reduction.

Flowd v1 had three distinct views: THE SPACE (the freeform board), NOW (an AI-generated synthesis of the project state), and the chat drawer (collapsed by default, opened on demand). Three mental models. Three modes to navigate between.

NOW was genuinely useful — when you returned to a project after a break, it gave you orientation fast. But it was a read surface. You couldn't work in it. So the workflow was: land on NOW to orient, switch to THE SPACE to do anything. Every session started with a mode switch before a single thought was captured.

The chat drawer had the opposite problem. It was the most alive part of the product — where real thinking happened, where the AI pushed back, where ideas formed in real time. But it was hidden. Collapsed by default. A tool you had to remember to open.

I cut from three views to two: removed NOW entirely, made chat always visible. Better — but still a seam. Two surfaces, two modes, a context switch every time the conversation and the board had to relate to each other.

So I cut again. One view.

Chat and workspace side by side, always. Chat is wider — not a visual accident but a deliberate signal: this is the primary entry point. The board is the right column. It's always visible, always current, never demanding. You don't navigate to it. You glance at it.

The logic behind every cut: *every additional view is a tax on attention.* For non-linear thinkers, that tax compounds fast. The fewer modes a product has, the less working memory it consumes — and the more cognitive space is left for actual thinking.

Mercury OS described it better than I could: rather than asking people to modify their thinking around arbitrary containers, the system should respond fluidly to the intentions of its user. Each view cut was a step toward that. One view is the answer.

`[JD: Rethinking UI primitives — reduced three views to one through principled subtraction]`
`[JD: Craft — the width ratio between chat and board is a design decision, not a default]`
`[JD: Owner mentality — every cut made against the instinct to add]`

### Visual Callout:
**[VISUAL 11 — View reduction diagram]**
Three frames in sequence. Frame 1: Flowd v1 — THE SPACE, NOW tab, chat drawer (collapsed). Three surfaces marked. Frame 2: Flowd v2 — NOW removed, chat visible. Two surfaces. Frame 3: Flowd current — one view, chat wider on left, board on right, always together. Each frame has a single annotation marking how many modes the user must hold in their head: 3 → 2 → 1. The story of the whole design process in one diagram.

---

## SECTION 9 — THE BUILD PROCESS

### Headline:
**"I prototyped in code because I had to."**

### Narrative Copy:

Flowd cannot be Figma-prototyped. The core experience — a conversation that builds structure in real time, connections surfacing that the user didn't request — only reveals itself when the AI is actually running. Static screens cannot show what it feels like when a workstream appears at the edge of your attention without you placing it there.

Every significant design decision in this project was made inside a live prototype. React throughout — useState for conversation state, component-level props for board card generation, live Claude API calls for the recognition engine. The code was a design instrument, not a deliverable.

This forced a discipline that static tools don't require: every state has to be reachable. You cannot draw an edge case and skip its behavior. If I wanted to design the moment where the AI is uncertain — where recognition might misfire — I had to build the condition that triggers it, and then design into that condition. The edge case is where trust is either built or broken. It is not optional.

`[JD: Code prototyping — explicit, with a reason specific to this product]`
`[JD: AI product design — designing for model uncertainty, not model perfection]`

### Visual Callout:
**[VISUAL 12 — Code + Design side by side]**
Left: a React component — the conversation state management or workstream recognition logic, clean, ~20 lines. Right: the rendered UI it produces. No explanation. The pairing is the argument.

---

## SECTION 10 — REFLECTION

### Headline:
**"The interface is not the product."**

### Narrative Copy:

Building Flowd without a team collapsed every part of the product design process into a single continuous loop. I was the user, the researcher, the designer, the builder, the person who decided when the thesis was wrong and what the next one should be.

That compression is clarifying.

The most important thing it taught me: when AI is in the loop, the design problem is never only the interface. It is the relationship between the model's behavior and the user's trust in that behavior.

Every time Flowd's AI connected two ideas correctly — surfaced a thread the user would have missed — trust accumulated. Every time it was wrong, some of that trust eroded. Designing the recognition behavior — when to fire, when to hold back, how to make reasoning legible at the moments it mattered — was as much a design problem as any layout decision. More so.

This is why SOUL.md exists. Not because the AI needed a personality. Because the product needed a stable perspective about when to act and when to wait. That perspective creates predictability. Predictability creates trust. And trust is the product.

When should AI act versus wait? That question is a design decision. I think it is the design decision that will define the next decade of AI products.

`[JD: AI believer — design philosophy, not feature preference]`
`[JD: Trust/safety thinking — articulated as a product mechanism]`

---

## SECTION 11 — THE BIGGER THESIS

### Headline:
**"Every tool I've used was designed for someone who already knows how they think."**

### Closing Copy:

Notion assumes you can decide where things go. Linear assumes you can define the task. Even most AI tools assume you can write the right prompt.

Flowd's bet is different.

**The user's job is to think. The system's job is everything else.**

That's not a feature decision. It is a position on what AI is for.

The reason Flowd feels different — the reason I keep building it — is the same reason working with a great collaborator feels different from working alone. Not because they do more tasks. But because in their presence, you think better. You move faster. You make connections you wouldn't have made alone.

That is what I am building toward. Not a smarter interface. A product that is the relationship between human intent and AI understanding — and a UI that is simply the surface where those two things touch.

Flowd is the first thing I've made that feels true to that. It is not finished. But it knows what it is.

`[JD: Why Anthropic — mission connection, earned through the work rather than stated]`
`[JD: Rethinking UI primitives — the final frame for the entire case study]`

---

## SECTION 12 — ARTIFACT TRAIL

End-to-end ownership proof. One project. One designer. Full chain.

| Artifact | What It Shows |
|---|---|
| Behavioral archaeology notes | Self-directed research, lived domain expertise |
| Flowd v1 prototype (React, live Claude API) | Code prototyping, AI product design from day one |
| Pivot decision doc | Ambiguity navigation, willingness to invalidate own work |
| Flowd PRD + AI system architecture | Systems thinking, technical depth, full product ownership |
| SOUL.md — AI character specification | Model-level thinking, trust design, novel artifact type |
| React codebase (key components) | Production-quality code prototyping |
| Landing page (designed + built) | Craft at word and pixel level, end-to-end delivery |

---

## JD COMPETENCY COVERAGE

| JD Signal | Sections |
|---|---|
| AI product design intuition + model understanding | §3, §6, §7, §10 |
| Code prototyping | §3, §9, §12 |
| Extreme craft | §8A, §8B, §8C |
| Ambiguity navigation | §1, §4, §5, §8C |
| Rethinking UI primitives | §2, §5, §6, §8C, §11 |
| Owner mentality | §1, §4, §7, §12 |
| AI believer (not just user) | §7, §10, §11 |
| Trust / safety thinking | §8A, §10 |
| Agentic UX design | §6, §7 |
| End-to-end execution | §12 |

---

## PRODUCTION NOTES

**Format:** Long editorial scroll. Not a slide deck. The narrative needs room to breathe — Flowd is a thinking product, the case study should feel like thinking, not presenting.

**Typography:** Georgia for section narratives — mirrors Flowd's own language, a choice that's consistent rather than accidental. Tight grotesque for headers and labels.

**Palette:** Flowd's moss/sage throughout. Dark backgrounds for §10 and §11 — the darkness builds as the thinking deepens.

**Opening:** Don't open with the final product. Open with the question.

**Closing:** Don't end with metrics you don't have. End with the thesis — it's stronger than a number.

**The case study is itself proof of craft.** Every typographic decision, every visual, every word is evidence. Treat it accordingly.
