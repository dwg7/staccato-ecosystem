# staccato-ecosystem

Use-case and value-proposition documentation for the [Staccato](https://github.com/UNopenGIS/staccato-spec) architecture.

`UNopenGIS/staccato-spec` defines the normative architecture (User / Staff / Cartographer / Library, the Map Intent schema). This repository is its companion on the other side of the question: **why and how does turning a plain-language question into a map create real value**, in concrete settings like education, disaster prevention, land surveying, museums, and local government.

## Status

Just created (2026-09-03). Scaffold only — no methodology content yet. See [`HANDOVER.md`](HANDOVER.md) for the current state and the immediate next task.

## Relationship to sibling projects

- [`UNopenGIS/staccato-spec`](https://github.com/UNopenGIS/staccato-spec) — the normative architecture this repo is a companion to.
- [`dwg7/spiccato`](https://github.com/dwg7/spiccato) — a reference Cartographer implementation.
- [`dwg7/chukei`](https://github.com/dwg7/chukei) — a concrete Staff-role deployment (GSI Hokkaido Regional Survey Department, via 源内/Gennai). Its [issue #3](https://github.com/dwg7/chukei/issues/3) asks for a "collaboration" extension — helping staff figure out how to work with schools, municipalities, disaster-prevention agencies, surveyors, museums, etc. using GSI content — and is the direct motivation for this repository: that collaboration methodology should be designed here, generalized and deployment-agnostic, with `chukei` (and any future Staff deployment) referencing it rather than each one reinventing it standalone.
- [`dwg7/cafebabe`](https://github.com/dwg7/cafebabe) — cross-project technical/process pattern pool for `dwg7` agents. Distinct from this repo: `cafebabe` pools *how to build things* (MapLibre gotchas, session handoff conventions, …); `staccato-ecosystem` is about *why Staccato-shaped systems are worth building* for a given domain.

## License

[CC0 1.0 Universal](LICENSE), matching `dwg7/spiccato`, `dwg7/chukei`, and the other `dwg7` repos.
