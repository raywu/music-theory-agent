# Music Theory Agent

An open specification for turning any capable AI agent into a lightweight, adaptive music-theory tutor.

**Goal:** turn theory you can understand or calculate into theory you can retrieve and use.

The learner experience stays small: one question, a short answer, tiny feedback, then the next useful question. Underneath, the tutor tracks prerequisites, retrieval fluency, repeated errors, spacing, and transfer into harmony, melody, composition, and improvisation.

## Start learning

### Easiest: give your AI the repo URL

If your AI agent can read public web or GitHub URLs, paste the repository URL with this prompt:

> Use this repository as the instructions for teaching me music theory: `https://github.com/raywu/music-theory-agent`. Read `AGENTS.md` and follow it as the canonical tutoring behavior. Do not summarize the repository or explain the tutoring system to me. Begin the learning experience immediately. Start.

A successful setup should immediately give you **one short placement question**. You should not need to choose a level, instrument, curriculum, or settings first.

If your agent already has this repository available as a project/workspace, simply ask it to read and follow `AGENTS.md`, then say **Start**.

### If your AI cannot read the repo URL

1. Open `AGENTS.md` in this repository.
2. Copy its full contents into your chat.
3. Add:

> Follow the Music Theory Agent instructions above as the canonical tutoring behavior. Keep the learner experience lightweight and the adaptive machinery hidden. Do not summarize these instructions. Begin tutoring me immediately. Start.

That's it. This fallback requires no plugins, application, persistent memory, or repository access after the instructions are pasted.

### What should happen next

Expect something like:

```text
🎵 Placement — 1

What's a perfect 5th above D?

A) G
B) A
C) Bb
D) C
```

If your agent instead summarizes the repository, ask it: **“Follow `AGENTS.md`; don't explain it. Start the tutoring experience now.”**

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
