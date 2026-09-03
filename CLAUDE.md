# staccato-ecosystem — Project Context

Persistent context for Claude Code sessions working in this repository (`dwg7/staccato-ecosystem`, cloned at `/Users/hfu/staccato-ecosystem`). If a session starts here, read this file, then read `HANDOVER.md` for the current status.

**Language convention**: matches `dwg7`'s established pattern (see `dwg7/chukei`, `dwg7/spiccato`) — meta-documentation (this file, `README.md`, `DECISIONS.md`, `HANDOVER.md`) is written in **English**, since `dwg7` is treated as an international project. Chat with hfu (the maintainer) happens in Japanese regardless of which repo is open.

**Content-document language policy** (hfu, 2026-09-03 — see `DECISIONS.md` D2): boilerplate files like `LICENSE` are fixed English-only. Everything else this repo produces as substantive content — the value-proposition/methodology documents that are this repo's actual deliverable — is written as a **`.ja.md` / `.en.md` pair per topic**, not a single bilingual file. A bare `.md` filename (no language suffix) means the content hasn't yet been split/localized either way.

This repo's work alternates between two contexts, matching its founding concept of organic linkage between domestic implementation (国内実施) and international cooperation (国際協力):
- **Domestic-implementation context**: `.ja.md` is the primary, actively-written language; a batch of content matures there first.
- **International-cooperation context**: before resuming, sync `.ja.md` → `.en.md` for whatever changed (translation, ja→en direction in practice), then treat `.en.md` as primary and accumulate there.

The two language variants are **not** kept continuously in sync — they're synced at the *transition* between contexts, not on every edit. This is a deliberate, repo-local experiment; it does not apply to other `dwg7`/`UNopenGIS` repos unless explicitly adopted there.

## What this project is

A companion to [`UNopenGIS/staccato-spec`](https://github.com/UNopenGIS/staccato-spec). Where `staccato-spec` is normative — the User/Staff/Cartographer/Library architecture, the Map Intent schema, its ADRs — `staccato-ecosystem` is about *value*: concrete documentation of why and how "turn a plain-language question into a map" (the Staff role's whole job) is worth deploying for real domains — education, disaster prevention, land surveying, museums, local-government collaboration, and whatever else surfaces.

**Founding motivation**: [`dwg7/chukei`'s issue #3](https://github.com/dwg7/chukei/issues/3) asks for a "ちゅうけい連携エージェント" ("Chukei Collaboration Agent") — an extension to Chukei (a Staff-role prompt for GSI Hokkaido Regional Survey Department staff, deployed via 源内/Gennai) that, on top of its existing map-generation ability, helps staff figure out concrete collaboration plans with schools, municipalities, disaster-prevention agencies, the surveying industry, museums, research institutions, infrastructure operators, and local community groups — starting from what the *partner* needs to accomplish, not from what GSI has to offer, and ending in an actually-usable deliverable (a lesson plan, a meeting handout, a proposal document) built on real, working map links.

hfu's explicit call (2026-09-03): design that collaboration methodology **here first, generalized and deployment-agnostic** — not tied to Gennai's single-file/no-includes constraint, not tied to GSI Hokkaido's specific partner list — and have `dwg7/chukei` (and any future Staff deployment that wants the same capability) *reference* this repo's methodology rather than each deployment re-deriving its own version of it independently.

## Relationship to sibling repos

- **`UNopenGIS/staccato-spec`** — the architecture this repo is a companion to. Read this first if unfamiliar with User/Staff/Cartographer/Library or Map Intent.
- **`dwg7/chukei`** — the concrete deployment that motivated this repo, and the first intended consumer of whatever methodology gets designed here. Its issue #3 is the source material — read it in full before designing anything (`gh issue view 3 --repo dwg7/chukei`; the raw principles are also excerpted into `HANDOVER.md` for a running start). Do not assume issue #3 is still open or unstarted by the time you read this — check its current state.
- **`dwg7/spiccato`** — reference Cartographer implementation `chukei` deploys against.
- **`dwg7/cafebabe`** — cross-project pattern pool. If something that emerges here turns out to be a general `dwg7` process/technical pattern rather than a Staccato/geospatial value-proposition one, it belongs in `cafebabe`, not here.
- **`dwg7/ferspas57`** (founded 2026-09-03) — this repo's **international-cooperation counterpart** to `dwg7/chukei`: a technical collaboration connecting Staccato to FERSPAS (FAO's remote-sensing data portal), split off from [`UNopenGIS/7#932`](https://github.com/UNopenGIS/7/issues/932) via founding issue [`UNopenGIS/7#997`](https://github.com/UNopenGIS/7/issues/997). Mostly technical (STAC↔`martin catalog` conversion) and belongs in `staccato-spec` for that half; but the *collaboration-process* learnings from it — how this kind of cross-organization, international connection is actually conducted, in contrast to `chukei`'s domestic pattern — are this repo's to absorb. Nothing has flowed here from it yet (too new); check its `HANDOVER.md` for current status when picking this up.

## License

CC0 1.0 Universal (`LICENSE`), matching `dwg7/spiccato` and `dwg7/chukei`.

## Continuity files

- `HANDOVER.md` — current state, what's next. **Read this first in any new session.**
- `DECISIONS.md` — ADR-lite decision log, append-only, newest at the top (matches `dwg7/chukei`'s convention).
