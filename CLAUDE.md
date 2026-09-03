# staccato-ecosystem — Project Context

Persistent context for Claude Code sessions working in this repository (`dwg7/staccato-ecosystem`, cloned at `/Users/hfu/staccato-ecosystem`). If a session starts here, read this file, then read `HANDOVER.md` for the current status.

**Language convention**: matches `dwg7`'s established pattern (see `dwg7/chukei`, `dwg7/spiccato`) — meta-documentation (this file, `README.md`, `DECISIONS.md`, `HANDOVER.md`) and methodology text are written in **English**, since `dwg7` is treated as an international project. Concrete instantiations that a specific deployment produces for its own end users (e.g. `dwg7/chukei`'s actual system-prompt text) render in whatever language that deployment's users need — this repo documents the *reusable* methodology, not any one deployment's user-facing wording. Chat with hfu (the maintainer) happens in Japanese regardless of which repo is open.

## What this project is

A companion to [`UNopenGIS/staccato-spec`](https://github.com/UNopenGIS/staccato-spec). Where `staccato-spec` is normative — the User/Staff/Cartographer/Library architecture, the Map Intent schema, its ADRs — `staccato-ecosystem` is about *value*: concrete documentation of why and how "turn a plain-language question into a map" (the Staff role's whole job) is worth deploying for real domains — education, disaster prevention, land surveying, museums, local-government collaboration, and whatever else surfaces.

**Founding motivation**: [`dwg7/chukei`'s issue #3](https://github.com/dwg7/chukei/issues/3) asks for a "ちゅうけい連携エージェント" ("Chukei Collaboration Agent") — an extension to Chukei (a Staff-role prompt for GSI Hokkaido Regional Survey Department staff, deployed via 源内/Gennai) that, on top of its existing map-generation ability, helps staff figure out concrete collaboration plans with schools, municipalities, disaster-prevention agencies, the surveying industry, museums, research institutions, infrastructure operators, and local community groups — starting from what the *partner* needs to accomplish, not from what GSI has to offer, and ending in an actually-usable deliverable (a lesson plan, a meeting handout, a proposal document) built on real, working map links.

hfu's explicit call (2026-09-03): design that collaboration methodology **here first, generalized and deployment-agnostic** — not tied to Gennai's single-file/no-includes constraint, not tied to GSI Hokkaido's specific partner list — and have `dwg7/chukei` (and any future Staff deployment that wants the same capability) *reference* this repo's methodology rather than each deployment re-deriving its own version of it independently.

## Relationship to sibling repos

- **`UNopenGIS/staccato-spec`** — the architecture this repo is a companion to. Read this first if unfamiliar with User/Staff/Cartographer/Library or Map Intent.
- **`dwg7/chukei`** — the concrete deployment that motivated this repo, and the first intended consumer of whatever methodology gets designed here. Its issue #3 is the source material — read it in full before designing anything (`gh issue view 3 --repo dwg7/chukei`; the raw principles are also excerpted into `HANDOVER.md` for a running start). Do not assume issue #3 is still open or unstarted by the time you read this — check its current state.
- **`dwg7/spiccato`** — reference Cartographer implementation `chukei` deploys against.
- **`dwg7/cafebabe`** — cross-project pattern pool. If something that emerges here turns out to be a general `dwg7` process/technical pattern rather than a Staccato/geospatial value-proposition one, it belongs in `cafebabe`, not here.

## License

CC0 1.0 Universal (`LICENSE`), matching `dwg7/spiccato` and `dwg7/chukei`.

## Continuity files

- `HANDOVER.md` — current state, what's next. **Read this first in any new session.**
- `DECISIONS.md` — ADR-lite decision log, append-only, newest at the top (matches `dwg7/chukei`'s convention).
