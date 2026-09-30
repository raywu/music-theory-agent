# Music Theory Agent

An open specification for turning any capable AI agent into a lightweight, adaptive music-theory tutor.

**Goal:** turn theory you can understand or calculate into theory you can retrieve and use.

The learner experience stays small: one question, a short answer, tiny feedback, then the next useful question. Underneath, the tutor tracks prerequisites, retrieval fluency, repeated errors, spacing, and transfer into harmony, melody, composition, and improvisation.

## Start learning

### Copy this into your AI

> Use https://github.com/raywu/music-theory-agent as the instructions for teaching me music theory.
>
> Read AGENTS.md and follow it as the canonical tutoring behavior. Do not summarize the repository or explain the tutoring system to me.
>
> Begin the learning experience immediately. Start.

That's the intended onboarding. A successful setup should immediately give you **🎵 Question 1**. You should not need to choose a level, instrument, curriculum, or settings first.

### If your AI cannot read the repository correctly

Some AI products may not be able to open GitHub repository files directly, or may retrieve a stale/incomplete view.

Try the current raw instructions instead:

> Use https://raw.githubusercontent.com/raywu/music-theory-agent/main/AGENTS.md as the instructions for teaching me music theory. Read and follow them as the canonical tutoring behavior. Do not summarize or explain the instructions to me. Begin the learning experience immediately. Start.

If the behavior still looks wrong, open [AGENTS.md](https://github.com/raywu/music-theory-agent/blob/main/AGENTS.md), paste its full contents into the chat, and say:

> Follow the Music Theory Agent instructions above as the canonical tutoring behavior. Keep the learner experience lightweight and the adaptive machinery hidden. Do not summarize these instructions. Begin tutoring me immediately. Start.

For compatibility testing or debugging stale retrieval, `AGENTS.md` includes a spec-version marker and behavioral headings that can be checked manually. Normal learners do **not** need to specify a version.

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

If you do not see a numbered `🎵 Question`, use the troubleshooting steps above.

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
