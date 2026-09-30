# Music Theory Agent

An open specification for turning any capable AI agent into a lightweight, adaptive music-theory tutor.

**Goal:** turn theory you can understand or calculate into theory you can retrieve and use.

The learner experience stays small: one question, a short answer, tiny feedback, then the next useful question. Underneath, the tutor tracks prerequisites, retrieval fluency, repeated errors, spacing, and transfer into harmony, melody, composition, and improvisation.

## Start learning

### Easiest: load the current tutor spec directly

If your AI agent can read public web URLs, paste this prompt:

> Read the current tutor instructions at https://raw.githubusercontent.com/raywu/music-theory-agent/main/AGENTS.md. Confirm internally that the file says **Spec version: 1.0.1** and contains the heading **Question counter — REQUIRED STATE**. If either is missing, tell me you could not load the current spec and stop. If both are present, follow AGENTS.md as the canonical tutoring behavior. Do not summarize the instructions or explain the tutoring system. Begin immediately with **🎵 Question 1**.

The verification is intentional: some AI products may use a cached/indexed repository view instead of the latest file.

A successful setup should immediately give you a numbered question headed **🎵 Question 1**. You should not need to choose a level, instrument, curriculum, or settings first.

### If your AI cannot verify the current spec

1. Open the current [AGENTS.md](https://github.com/raywu/music-theory-agent/blob/main/AGENTS.md).
2. Copy its full contents into your chat.
3. Add:

> Follow the Music Theory Agent instructions above as the canonical tutoring behavior. Keep the learner experience lightweight and the adaptive machinery hidden. Do not summarize these instructions. Begin tutoring me immediately with **🎵 Question 1**.

That's it. This copy/paste path is the most reliable fallback because it does not depend on the AI product's GitHub retrieval or cache.

### What should happen next

Expect something like:

```text
🎵 Question 1

What's a perfect 5th above D?

A) G
B) A
C) Bb
D) C
```

If you do not see **🎵 Question 1**, the agent is not following the current presentation contract. Use the copy/paste fallback above.

## What it should feel like

```text
🎵 Question
Root = G. What's the ♭3?

> Bb

✅ Correct — G → Bb = ♭3.
🔥 6 · XP 42

What's the perfect 5th of G?
```

Not a textbook. Not a worksheet. Not an LMS.

## Repository
- `AGENTS.md` — canonical tutor behavior
- `docs/` — pedagogy, curriculum, adaptation, visualization, case study
- `schemas/learner-state.schema.json` — optional portable state
- `tests/` — examples, behavioral acceptance tests, adversarial tests, and pre-publication validation notes

## Scope
V1 covers foundational intervals, thirds/fifths, major/minor/diminished triads, scale degrees, diatonic harmony, Roman numerals, circle-of-fifths relationships, natural minor, introductory modes, voice leading, tension/resolution, melody vs harmony, and basic composition/improvisation reasoning.

Instrument-agnostic; no notation, MIDI, audio, or dedicated app required.

## Contributions
Issues and PRs are welcome for clearer instructions, better tests, theory corrections, exercise transformations, accessibility, and evidence-supported pedagogy.

## License
MIT.
