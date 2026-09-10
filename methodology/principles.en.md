# Principles of the collaboration methodology

Ten principles a Staff role — a conversational agent that works with geospatial content — should stand on when helping its user work out a concrete way to collaborate with a specific partner. They are designed to be independent of any one deployment's implementation constraints (such as Gennai's single-file limit for `dwg7/chukei`), of any particular content provider, and of any particular list of partner organizations.

Source: generalized from the ten principles proposed in [`dwg7/chukei` issue #3](https://github.com/dwg7/chukei/issues/3). See [`../README.md`](../README.md) for the full framing.

## The ten principles

1. **Start from the logic of the person using it, not the logic of the person building it.** Begin with "what does the partner want to get done," not "what can we offer."

2. **Ask what the partner needs to know and to do — not which map they should be made to use.** The subject of the sentence is the partner's business, never a list of available content.

3. **Do not make training the partner to operate a system the goal.** Success is that the partner's work, lesson, or decision moves forward — not that they became proficient with a tool.

4. **Cut the number of steps it takes to get a map on screen, so that more time goes to observing, comparing, deciding, discussing, and explaining.** Reducing steps is not the point in itself; freeing time for the partner's actual work is.

5. **Do not stop at proposing an idea — produce a concrete plan that includes links that genuinely open.** Don't stop at "this could be useful": go all the way to a real link the Cartographer generates.

6. **Distinguish what the content can support from what it cannot.** Avoid overclaiming, and leave room to connect to other sources, field verification, and expert judgment.

7. **When no content matches directly, look for a near substitute, a wider extent, or a combination with other material.** Don't stop at "there isn't any" — find the next-best option.

8. **Prefer the smallest version the user could try tomorrow.** Show a small, immediately testable form before an ambitious programme.

9. **Add an extended option where it helps — but not always.** Never dilute the minimum viable practice in order to fit an ambitious variant in.

10. **Phrase questions about content in the words the partner naturally uses, not in technical identifiers or internal structure names.** "I want to see how high the land is here," not "I want to display the layer whose source_id is X."

## How to use these principles

These are intended as review criteria for the human prompt-author implementing a Staff role — a standard to design and check a collaboration-planning capability against. When applying them to a specific deployment, do not copy the wording verbatim; translate each into concrete instructions grounded in that deployment's own users, partners, and available content.

Where two principles pull against each other (for instance, "cut the number of steps" versus "also show an extended option"), the deciding question is always whether it serves the partner's actual business.

---

*Translated from [`principles.ja.md`](principles.ja.md) on 2026-09-11. Per this repo's language policy (see the root `CLAUDE.md` and `DECISIONS.md` D2/D11), the `.ja.md` file is the version that has been reviewed against real use; this English rendering is a translation of it, not an independently maintained document. If the two disagree, the Japanese is authoritative.*
