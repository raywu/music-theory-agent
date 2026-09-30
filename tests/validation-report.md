# Pre-publication validation report

This report tests the written specification against eight synthetic learner profiles. It is a design-level simulation, not evidence from independent real users or independent model families.

## Acceptance invariant
Normal learner-facing turns should preserve: one primary question; tiny feedback; hidden adaptation; varied retrieval; eventual musical application.

## Persona results

### 1. Complete beginner — PASS with guardrail
Risk: terminology overload. `AGENTS.md` requires behavioral placement, minimum scaffolding, and useful difficulty. The tutor can begin with multiple choice/visual anchors and fade support.

### 2. Intuitive musician — PASS
Risk: patronizing linear curriculum. The dependency graph is traversable, placement is behavioral, and advanced musical reasoning can coexist with weak labels/retrieval.

### 3. Calculator — PASS
Risk: semitone calculation mistaken for fluency. Specification explicitly credits calculation while withholding automatic-retrieval evidence and builds anchors later.

### 4. Memorizer — PASS
Risk: repeated wording creates fake mastery. Representation variation and reverse/transform/application evidence are required.

### 5. Guesser — PASS
Risk: lucky streak inflates mastery. Immediate streak is insufficient; spaced changed-form confirmation is required.

### 6. Uneven learner — PASS
Risk: prerequisite remediation becomes a remedial course. Specification descends only to smallest blocker and mandates return to original higher-level application.

### 7. Confident-but-wrong — PASS with limitation
Risk: fluent explanation contains incorrect theory. Theory guardrails require verification when uncertain, but correctness still depends partly on base-model capability. This cannot be fully solved by prompting.

### 8. Fast learner — PASS
Risk: needless drilling. Placement, evidence dimensions, scaffold fading, and anti-pattern rules support rapid advancement.

## Adversarial findings incorporated

1. **Interleaving overreach:** corrected. The spec now uses interleaving selectively and allows temporary blocked practice for establishing anchors.
2. **Hidden sophistication leakage:** made an explicit UX invariant and behavioral test.
3. **Overdiagnosis:** diagnosis now requires corroborating evidence and at most 1–2 discriminating probes when needed.
4. **Remediation rabbit holes:** return-to-original-skill is mandatory.
5. **Self-report gaming:** behavioral evidence outranks `instant/worked out/guessed` self-report.
6. **Prompt memorization:** mastery requires changed retrieval forms.
7. **Scaffolding dependency:** explicit fading rule added.
8. **Calculation dependency:** fallback calculation is respected but not equated with fluency.

## Remaining uncertainties

- Cross-model fidelity has not yet been measured on independent agent families.
- Mastery timing/spacing thresholds are intentionally qualitative in v1; real usage may justify more explicit scheduling.
- The specification cannot guarantee theory correctness from a weak base model.
- Lightweight XP/streak behavior is intentionally underspecified to avoid making scoring the product; agents may vary cosmetically.

## Release recommendation

The specification is ready for independent clean-context agent trials. Public release should describe v1 as an open behavioral specification, not as experimentally validated learning software.
