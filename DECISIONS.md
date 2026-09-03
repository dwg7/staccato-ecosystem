# Decisions Log

ADR-lite log for this project. English, per `CLAUDE.md`'s language convention. Append new decisions at the top, oldest at the bottom (matches `dwg7/chukei`'s convention).

---

### D5 — Second field input: real end-user session report folds two new insights into `methodology/`
**Date**: 2026-09-03
**What**: hfu, in the role of GSI Hokkaido Regional Survey Department director actually using the deployed `CHUKEI_COLLABORATION_PROMPT.md` (not in a `staccato-ecosystem`-authoring capacity), ran several real B-type (連携企画依頼) collaboration-planning sessions in a separate chat session and manually relayed a summary report into this repo's session. Three scenarios were worked: a municipal disaster-preparedness briefing, a comparison of a direct student-facing lesson vs. a teacher-training session on the same topic, and a keynote addressing an industry/academia/government audience at once. No bugs or spec/catalog change requests were reported — all map links used real, existing catalog identifiers per `CHUKEI_PROMPT.md`'s existing rules.

Generalized (stripping GSI-specific place names, the reporting person's identity, and real catalog identifiers) and folded into `methodology/`:
- `worked-examples/disaster-preparedness-briefing.ja.md` — new worked example for the existing 防災の共通認識 pattern, plus an optional "想定される質問への対応" section added to `output-structure.ja.md` for high-stakes partners.
- `worked-examples/education-train-the-trainer.ja.md` — new worked example illustrating that a partner who will themselves teach/train others needs a *skill* as their deliverable, not a finished artifact. Added a 最終利用者 vs 展開する立場 distinction to `process.ja.md` step 1.
- `worked-examples/multi-stakeholder-advocacy.ja.md` — new worked example for a **new pattern**, 対外的な説明・アピール, added to `patterns.ja.md`: a single session addressing several distinct stakeholder types at once, each with a different concern, rather than one partner. Added a single-vs-multiple-audience check to `process.ja.md` step 1.
- Restructured `worked-example.ja.md` (singular) into a `worked-examples/` directory with a `README.md` index, since there are now four examples across three patterns rather than one.

**Why**: this is qualitatively different validation from D4 — D4 was an implementer's static design review while building the prompt; D5 is an actual end user's real usage surfacing gaps the original issue #3 material didn't anticipate (the train-the-trainer case, the multi-stakeholder case). Both new additions were real gaps, not speculative extensions — worth keeping the bar there (don't add hypothetical patterns without a real scenario behind them). Still same-deployment/same-person as D4, so `HANDOVER.md`'s "validate against a structurally different deployment" open item stands.

---

### D4 — First validation: `dwg7/chukei` built `CHUKEI_COLLABORATION_PROMPT.md` from `methodology/`, no corrections needed
**Date**: 2026-09-03
**What**: The `dwg7/chukei` session closed issue #3 and pushed `CHUKEI_COLLABORATION_PROMPT.md` (chukei commit `b545c41`), built by adapting `methodology/*.ja.md` into Chukei's concrete vocabulary (コンテンツ→地図/spiccatoリンク, デプロイメント固有規則→`req`/`opt`/`rstyle`/`ostyle`/`basemap` etc.) rather than re-deriving from issue #3's raw text. Reported back over cross-session messaging: no corrections or structural gaps found in the methodology docs while adapting; all 7 of issue #3's acceptance tests passed a static design review against the built prompt; the build script embeds `CHUKEI_PROMPT.md`'s on-disk content verbatim (byte-for-byte) so the two files can't drift apart on the map-generation side.
**Why**: this is the first real test of whether `methodology/` is actually reusable rather than accidentally Chukei-shaped — the open item D3 and `HANDOVER.md` flagged. A clean adapt-with-no-corrections outcome is a good signal, but it's still the *same* deployment the methodology was extracted from, not a structurally different one — see the updated open follow-up in `HANDOVER.md`.

---

### D3 — Methodology shape: human-facing design guidance, split by concern, `methodology/`
**Date**: 2026-09-03
**What**: Confirmed three open questions from `HANDOVER.md` with hfu before starting the methodology write-up: (1) the documents in `methodology/` are **human-facing design guidance** for whoever builds a Staff deployment's collaboration feature, not text meant to be pasted verbatim into a system prompt — adapting this into deployment-specific prompt text is a separate, later step done in that deployment's own repo; (2) content is **split by concern** into topic files (`principles`, `request-types`, `process`, `output-structure`, `patterns`, `quality-checklist`, `worked-example`), matching `dwg7/cafebabe`'s `patterns/` convention, rather than one monolithic file; (3) `dwg7/chukei` issue #3 gets a comment **now**, pointing at this repo, rather than waiting — so the two efforts don't independently diverge while chukei's own `CHUKEI_COLLABORATION_PROMPT.md` work is still unstarted. First pass of all seven `methodology/*.ja.md` files written this session, generalized from issue #3's principles/patterns/process/worked-example, with Chukei/GSI/Gennai-specific packaging (single-file constraint, catalog IDs, fixed response formats) deliberately left out — deployments reference their own Cartographer-specific rules for that.
**Why**: matches D2 (`.ja.md`/`.en.md` content-document policy) — this is the first real content this repo produces, written `.ja.md`-first per the domestic-implementation-context default. Splitting by concern keeps future edits (e.g. adding worked examples for other domains, per the open item this leaves in `HANDOVER.md`) localized rather than requiring edits to one large file.

---

### D2 — Content-document language policy: `.ja.md`/`.en.md` pairs, alternating primary by context
**Date**: 2026-09-03
**What**: Confirmed with hfu that this repo's *content* documents (the value-proposition/methodology deliverables — distinct from meta-docs like this file, `README.md`, `HANDOVER.md`, and boilerplate like `LICENSE`, which stay English-only per the existing convention) are managed as `.ja.md`/`.en.md` pairs per topic rather than single bilingual files. A bare `.md` means not yet split. Work alternates by context rather than staying continuously bilingual: in a domestic-implementation (国内実施) context, `.ja.md` is primary and content accumulates there; when switching to an international-cooperation (国際協力) context, `.ja.md` → `.en.md` is synced (translated) first, then `.en.md` becomes primary for that stretch of work. Sync happens at context transitions, not on every edit.
**Why**: hfu's explicit framing — this repo's founding concept includes organic linkage between domestic implementation and international cooperation as parallel, alternating modes of work, not simultaneous bilingual authoring. Keeping both languages continuously in sync on every edit would slow down whichever mode is currently active; syncing only at the transition matches how the work actually happens. Repo-local experiment, not intended to propagate to other `dwg7`/`UNopenGIS` repos.

---

### D1 — Repo founded: scope is use-case/value-proposition documentation, methodology-first relative to chukei#3
**Date**: 2026-09-03
**What**: Created `dwg7/staccato-ecosystem` (public, CC0 1.0) at hfu's request, made during a `staccato-spec`-session Claude Code conversation. Two scope decisions confirmed directly with hfu before scaffolding: (1) this repo's positioning is a companion to `UNopenGIS/staccato-spec` — where that repo is the normative architecture, this one documents *why/how* it creates real value in concrete domains (education, disaster prevention, surveying, museums, local government); (2) relative to `dwg7/chukei`'s issue #3 (a request for a Gennai-specific "collaboration agent" prompt extension), the generalized, deployment-agnostic version of that collaboration methodology is designed **here first**, with `chukei` (and future Staff deployments) referencing it — not the reverse. Scaffolded with `README.md`, `CLAUDE.md`, `DECISIONS.md`, `HANDOVER.md`, `LICENSE` (CC0 1.0, copied verbatim from `dwg7/chukei`), matching the established `dwg7` per-project convention. `HANDOVER.md` carries the raw principles/patterns extracted from chukei issue #3 as a running start for the actual methodology-design work, which has not started yet.
**Why**: hfu is running this the same way other cross-session `dwg7` handoffs have run (e.g. the `basemap` field's three-way handoff across `spiccato`/`staccato-spec`/`stars` sessions, chukei `DECISIONS.md` D27) — a dedicated session per repo, `HANDOVER.md`/`CLAUDE.md` as the onboarding path for whichever session picks it up next, rather than one session trying to hold every project's context simultaneously.
