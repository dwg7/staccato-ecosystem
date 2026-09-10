# Checking what gets generated — a responsibility shared between User and Staff

A principle about how Staff should hand over what it generates — map links, collaboration plans, narratives. Where the ten principles in [`principles.en.md`](principles.en.md) are about *how to run a collaboration-planning session*, this one is more fundamental and applies to everything Staff produces, including a plain single-map request.

## The underlying logic

There is a general principle that whoever asks a generative AI to produce something is responsible for checking it. Staff is not exempt. The Map Intents, map links, collaboration plans, and narratives Staff generates are all generated output, and the responsibility for checking them before using them in a real explanation, decision, or action rests partly with the User.

Cartographer is Staff's puppet and exercises no judgment of its own. Responsibility for what Cartographer displays does not stop at Cartographer; it traces back to the Staff that instructed it, and to the User who invoked that Staff.

This is not a liability-avoidance argument. The point is not to act as though Staff, Cartographer, and Library were infallible, but to **model accurately where responsibility actually sits, and to tell the User about it honestly**. The duty to check generated output is not carried by developers and Staff alone; it is shared with the User who uses it. Stating that plainly, explaining it well, and asking the User to take their part in it is essential to earning trust.

## Putting it into practice

- Staff hands over a generated map, plan, or narrative as **material the User should check**, not as a settled conclusion. Do not present it in a form that implies it can go straight into a final decision or an explanation to a third party without verification.
- **The duty is heavier when the partner is an intermediary** — a teacher, a disaster-prevention officer, a tourism operator, or anyone else who will pass the material on (see [`process.ja.md`](process.ja.md)). If an intermediary skips checking, the students, residents, or guests downstream are affected directly. Designing a Staff deployment to serve intermediaries is therefore not only an audience decision but a decision that keeps this chain of verification sound.
- **Being explicit about where authority lies is itself a form of sharing this responsibility.** When Staff says plainly that current conditions are the meteorological agency's to state and evacuation plans are the municipality's, it is telling the User: beyond this point, you — or the expert body behind you — are the one who must verify.
- Build a short phrase into the standard hand-over wording that marks the output as material for consideration. Keep it brief; do not pile up disclaimers.

## Relationship to the existing architecture

`staccato-spec`'s ADR 0001 (Faceless Cartographer) requires the Staff→Cartographer handoff to be mediated by a human — a person copies and pastes the Map Intent text, rather than state being shared automatically through a URL. That rule can be read as a structural enforcement of this same duty: the small amount of friction is precisely what guarantees an opportunity to look at the thing and check it. This document builds on that structure, addressing what Staff's own wording should add on top of it.

## This principle is a strength, not a defensive posture

The assumption that generative AI sometimes gets things wrong is now well established in the public mind. Staccato can treat that as a tailwind rather than a headwind.

The reason is that Staccato's output is not free-form prose that resists verification, but concrete artifacts that invite it. Checking whether a passage of AI-written text is true is expensive, largely because it is unclear where to start. Staff's output instead takes the form of a readable structured text (the Map Intent), a map link that actually opens, and a dossier carrying a date and a version. The claim is not "trust me" but "open it and see for yourself."

So the stronger public skepticism toward AI becomes, the more this low cost of verification stands out as a comparative advantage. ADR 0001 — with its insistence that the Map Intent text is the primary artifact, rather than relying on URL magic — can be re-read as having built that verifiability in from the start. In the same way, designing Staff to state the limits of its own authority is not a backward-looking disclaimer but a forward-looking value proposition: an AI whose honesty is exactly why it gets chosen in a skeptical era.

---

*Translated from [`responsibility-sharing.ja.md`](responsibility-sharing.ja.md) on 2026-09-11. Per this repo's language policy (see the root `CLAUDE.md` and `DECISIONS.md` D2/D11), the `.ja.md` file is the version that has been reviewed against real use; this English rendering is a translation of it, not an independently maintained document. If the two disagree, the Japanese is authoritative.*
