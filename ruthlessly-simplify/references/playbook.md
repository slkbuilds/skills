# Ruthlessly Simplify — Playbook

Depth for the simplify run. Read when you want the playback format, the worked before/after, the failure modes, or the test-seed. The SKILL.md is enough to operate; this is the "sometimes" layer.

## Worked playback

Two parts: what the skill does in order, then what to keep (the parts only the owner knows) grouped into buckets that fit the skill. This is a real playback of a weekly project-review skill — note the buckets are chosen for *this* skill, not a fixed template:

> **What this skill does:**
> Confirm the week → silently load the execution data → present the planned-vs-actual picture with an honest per-project assessment → Shawn reflects → check patterns against past reviews → score against goals → write the review doc.
> *ALFRED does the homework; Shawn does the thinking.*
>
> **The key pieces to hold:**
> - **The stance** — silent aggregation, present don't quiz; gaps are data, not failures.
> - **The frame & metric** — planned-vs-actual mapping; NN-hit-rate is the headline.
> - **The judgment rules** — learnings stay direction-level ("does this matter for where we're going?"); no fabrication; real dates only.
> - **The wiring** — turn-gated (one question per turn); Live projects from `_index.md` at runtime; domain layer out of scope; score feeds Weekly Review.

A thinking skill's buckets would be different — e.g. *the discipline · the lens · the output shape*. Pick buckets that make what-to-keep scannable for the skill in front of you.

## Worked before/after — cut AND rewrite

A bloated fragment from a hypothetical `weekly-review`:

> **Before:**
> "Begin by carefully reading through each of the session logs from the past week one at a time. As you read, think step by step and be thorough and rigorous. Then synthesize the key themes — remember that synthesis means finding patterns across multiple sources. Shawn prefers that you don't lead with generic praise; he wants the hard read first, and he calibrates from pattern recognition, so engage his reasoning before offering caution."

- *Cut (generic method):* "one at a time", "think step by step", "be thorough and rigorous", "synthesis means finding patterns" — the model does this by default.
- *Keep (only the owner knows this):* the calibration — hard read before praise, engage reasoning before caution.
- *Rewrite (the survivors, into instructional form):*

> **After:**
> "Read the week's session logs and surface the themes. Lead with the hard read, not praise — Shawn calibrates from pattern recognition, so engage his reasoning before offering caution."

~75 words → ~30, and it reads *clearer*, not just shorter. The cut removed generic method; the rewrite turned what stayed into a plain instruction.

## Anti-patterns — how a simplify run betrays itself

- **Cutting what only the owner knows to hit a count.** The worst mistake. The count serves clarity; it never overrides what only they could have written.
- **Cutting before understanding.** Applying "fewest steps" without a confirmed read of the workflow — you delete a load-bearing step you didn't recognize. The play-back step exists to prevent exactly this.
- **Compressing into jargon or abstraction.** Winning "every token earns its place" by losing "literal over abstract." Shorter *and worse*. If a leaner line needs decoding, it failed.
- **Cutting the calibration that keeps it from over-scripting.** Remove it and the model falls back to its generic default — the bloat you were removing.
- **Loosening an exact instruction that guards a fragile operation.** "Trust the model" applied to a step that was exact on purpose. Confirm why an instruction is rigid before relaxing it.

If a proposed change matches one of these, it's not a change. Put it back.

## Test-seed — the playback is the test spec

The playback forces a statement of the target skill's **workflow** and **what to keep**. That statement is the per-skill test. To check any future edit didn't damage the skill, verify against it:

1. **Job intact?** Does the edited skill still do the same job, end to end?
2. **What-to-keep intact?** Is every held piece still present — stance, metrics, rules, wiring, the hard-won specifics?
3. **Keystones held?** Clearer or equal on clarity; fewer-or-equal steps on design.

Capture the playback statement in the run's output so it can seed a real eval later — the bridge to bolting evals onto the skill suite.
