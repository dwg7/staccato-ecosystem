# Collaboration methodology

Deployment-agnostic design guidance for a Staff role's *collaboration-planning* capability: helping a Staff deployment's users move from "I have geospatial content" to "here's a concrete collaboration plan with a specific partner, grounded in real map links." Distinct from — and layered on top of — the Staff role's core map-generation capability (User question → Map Intent → Cartographer link), which each deployment already implements on its own terms.

This directory holds the *reusable* methodology, not any one deployment's prompt text. See `CLAUDE.md`'s content-document language policy: each topic here is a `.ja.md`/`.en.md` pair (or `.ja.md` only, until a translation pass happens at the next domestic↔international transition — see `HANDOVER.md` for current status).

**Origin**: extracted and generalized from [`dwg7/chukei` issue #3](https://github.com/dwg7/chukei/issues/3), a request for a Gennai-specific, single-file, Japanese-only `CHUKEI_COLLABORATION_PROMPT.md`. That issue's concrete deliverable stays scoped to Chukei's own hard constraints (self-contained single file, GSI Hokkaido's specific partner list, embeds `CHUKEI_PROMPT.md` verbatim); this directory is the generalized core that deliverable — and any future Staff deployment wanting the same capability — should be built from, rather than each deployment re-deriving its own version independently.

**Audience and shape**: these are human-facing design documents that a prompt-author (or anyone designing a Staff deployment's collaboration feature) reads and adapts — not text meant to be pasted verbatim into a system prompt. Adapting this into deployment-specific prompt text (in whatever language and packaging that deployment needs) is a separate, later step, done in that deployment's own repo.

## Contents

- [`principles.ja.md`](principles.ja.md) — the 10 basic principles a collaboration-planning capability should follow.
- [`request-types.ja.md`](request-types.ja.md) — the three kinds of request a Staff-plus-collaboration deployment needs to tell apart, and why.
- [`process.ja.md`](process.ja.md) — the 7-step process for turning a collaboration request into a concrete plan.
- [`output-structure.ja.md`](output-structure.ja.md) — a default document structure for presenting a collaboration plan.
- [`patterns.ja.md`](patterns.ja.md) — representative collaboration patterns across domains (education, disaster preparedness, field survey, consensus-building, local-resource discovery, data-gap discovery, external advocacy to a mixed audience), offered as inspiration rather than a checklist.
- [`quality-checklist.ja.md`](quality-checklist.ja.md) — a self-check list to run before presenting a plan.
- [`responsibility-sharing.ja.md`](responsibility-sharing.ja.md) — how Staff should communicate that checking its output before acting on or forwarding it is a responsibility shared with the User, not Staff/Cartographer/Library's alone to bear. Applies beyond collaboration-planning, to Staff's core map-generation output too.
- [`worked-examples/`](worked-examples/README.md) — concrete worked examples, one or more per pattern where available, each with an explicit warning against over-generalizing from it. Some patterns still have none — see that directory's own README for which.
