# Decisions Log

ADR-lite log for this project. English, per `CLAUDE.md`'s language convention. Append new decisions at the top, oldest at the bottom (matches `dwg7/chukei`'s convention).

---

### D1 — Repo founded: scope is use-case/value-proposition documentation, methodology-first relative to chukei#3
**Date**: 2026-09-03
**What**: Created `dwg7/staccato-ecosystem` (public, CC0 1.0) at hfu's request, made during a `staccato-spec`-session Claude Code conversation. Two scope decisions confirmed directly with hfu before scaffolding: (1) this repo's positioning is a companion to `UNopenGIS/staccato-spec` — where that repo is the normative architecture, this one documents *why/how* it creates real value in concrete domains (education, disaster prevention, surveying, museums, local government); (2) relative to `dwg7/chukei`'s issue #3 (a request for a Gennai-specific "collaboration agent" prompt extension), the generalized, deployment-agnostic version of that collaboration methodology is designed **here first**, with `chukei` (and future Staff deployments) referencing it — not the reverse. Scaffolded with `README.md`, `CLAUDE.md`, `DECISIONS.md`, `HANDOVER.md`, `LICENSE` (CC0 1.0, copied verbatim from `dwg7/chukei`), matching the established `dwg7` per-project convention. `HANDOVER.md` carries the raw principles/patterns extracted from chukei issue #3 as a running start for the actual methodology-design work, which has not started yet.
**Why**: hfu is running this the same way other cross-session `dwg7` handoffs have run (e.g. the `basemap` field's three-way handoff across `spiccato`/`staccato-spec`/`stars` sessions, chukei `DECISIONS.md` D27) — a dedicated session per repo, `HANDOVER.md`/`CLAUDE.md` as the onboarding path for whichever session picks it up next, rather than one session trying to hold every project's context simultaneously.
