# Handover Notes

Read this first in any new session on this repo. Written in English per `CLAUDE.md`'s language convention.

## What's true as of 2026-09-03

- **First methodology pass complete.** `methodology/` now holds seven `.ja.md` documents — `principles`, `request-types`, `process`, `output-structure`, `patterns`, `quality-checklist`, `worked-example` — generalized from `dwg7/chukei` issue #3, plus a `methodology/README.md` index (English, meta). See `DECISIONS.md` D2 (content-document language policy) and D3 (methodology shape decisions) for the reasoning.
- **Scope decisions confirmed with hfu** (D3): the methodology docs are human-facing design guidance, not prompt text to paste verbatim; split by concern into topic files; `dwg7/chukei` issue #3 was commented pointing at this repo (check the issue for hfu's/anyone's follow-up since).
- **`.en.md` translations do not exist yet.** Per D2, that's expected — they get written at the next transition into an international-cooperation context, not continuously alongside `.ja.md`. Don't create them speculatively; when that transition happens, sync `.ja.md` → `.en.md` for whatever's there at that point first, then continue in English.
- **Content is a first pass, not exhaustive.** It generalizes issue #3's material faithfully but hasn't been stress-tested against a second real deployment yet.

## Open follow-ups for whoever picks this up next

- **More worked examples.** `worked-example.ja.md` currently has exactly one (the 4th-grade lesson, inherited from issue #3) and explicitly warns against over-generalizing from it. `patterns.ja.md` lists five other pattern categories (disaster preparedness, field-survey prep, consensus-building, local-resource discovery, data-gap discovery) with no worked example each — adding at least one per pattern would make `patterns.ja.md` less abstract and give `quality-checklist.ja.md`'s "don't over-transfer from the one example you know" item less to worry about.
- **Validate against a second deployment.** This methodology has one source (chukei issue #3) and one implicit target (chukei itself). It hasn't been checked against a differently-shaped Staff deployment (different domain, different partner types, non-Japanese context) to see what's actually reusable vs. still accidentally Chukei-shaped. If/when another `dwg7`/`UNopenGIS` Staff deployment wants this capability, that's the real test.
- **`dwg7/chukei`'s own `CHUKEI_COLLABORATION_PROMPT.md` is still unwritten.** Issue #3 itself asks for a Chukei-specific, single-file, Gennai-packaged prompt built on top of `CHUKEI_PROMPT.md`. That's `chukei`'s own repo's work, informed by (not duplicating) `methodology/` here — not a task for this repo, but worth knowing it's the natural next consumer.
- **Whether to eventually version/date individual methodology docs** (e.g. if chukei's real-world use surfaces a principle that needs revision) — no convention for that yet; `DECISIONS.md` currently carries the append-only decision history at the repo level, not per-file.
