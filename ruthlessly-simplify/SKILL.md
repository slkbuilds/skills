---
name: ruthlessly-simplify
description: Lean out an existing skill — cut what the model already knows, rewrite what stays into clear, concise, concrete language, and keep what only the owner knows. Runs three audits in order (existence, inclusion, expression), plays the skill back for confirmation first, proposes a change-list, and writes only after approval. Use when the user says "ruthlessly simplify [skill]", "lean out [skill]", "simplify this skill", "tighten this skill", "trim this skill", "/ruthlessly-simplify", or wants a bloated, verbose, or over-scripted skill cut down. NOT for building a new skill from scratch — that is skill-creator. This only simplifies a skill that already exists.
---

# Ruthlessly Simplify

**The problem.** Skills bloat. They over-instruct what the model already knows: generic method, restated context, scripted steps. Every needless line costs tokens and reduces how reliably the model follows the lines that matter. A bloated skill is expensive to run and worse at its job.

**The goal.** A skill that is highly effective and token-efficient. Say only what is needed, in the fewest words, and trust the model with the rest.

## The one rule above all

Clarity beats brevity. Never delete what only the owner knows: their judgment, their methods, their hard-won lessons. When cutting a word would cost clarity, keep the word.

## The three audits

Run the pass as three questions, in order:

1. **Existence.** Should this section, reference, script, or step exist at all? A step stays only if removing it degrades the output. Caution: an exact instruction may be guarding a fragile operation. Confirm why it is exact before loosening or cutting it.
2. **Inclusion.** Should this line be in it? If the model already knows it, cut it. If it tunes the model toward the owner's approach, knowledge, or position, keep it.
3. **Expression.** Is each surviving line clear, concise, and concrete? Clear: understood on first read. Concise: every line earns its place. Concrete: literal over abstract. When the three conflict, the earlier one wins.

A pass can succeed at one audit and fail another: clear sentences about things the model never needed told, or the right content written unclearly. Run all three.

## Banned patterns

The model's default writing habits. Check every rewrite against this list:

- Metaphors and figurative language. They force the reader to decode before understanding.
- Rhetorical contrast: "it is not X, it is Y". State what it is.
- Em dashes as rhetorical pivots. Use a period, comma, or colon.
- Emphasis tricks: capitalized words, stacked intensifiers.
- Meta-commentary: sentences that describe the document instead of informing the reader.
- Filler: "it is important to note", "carefully", "be thorough".

## Instructions — understand first, then cut

1. **Understand and play back, before touching anything.** Read the whole target (SKILL.md plus every reference it loads). Play it back in two parts and get the user's OK: the **workflow** (what the skill does, in order) and **what to keep** (the parts only the owner knows, grouped into buckets that fit this skill). Cutting before understanding deletes load-bearing steps you did not recognize.
2. **Propose** the new version plus a change-list. Every cut and rewrite names the audit that justified it.
3. **Approve.** The user approves, adjusts, or says cut more.
4. **Commit, then write.** Commit the current version first so it is recoverable, then write the new one.
5. **Re-audit after writing.** An edit pass can introduce the violations it exists to remove.

## Where things go in the folder

A skill is a folder, not a file:

- **SKILL.md** holds what every run needs: trigger, workflow, must-keep guidance. Cap at 100 lines.
- **references/** holds what some runs need: long templates, edge cases, worked examples. One level deep: SKILL.md points to a reference; a reference never points to another. Every reference must be linked from SKILL.md; a reference nothing links to is lost content, so relink it or delete it. A reference over 100 lines starts with a contents list.
- **scripts/** holds fixed, repeatable work: checking, formatting, fetching. Say whether to run a script or read it as reference; running is the default.

Sort content by how often it is needed, not by line count. Moving every-run content into a reference to shrink SKILL.md is cheating. Over 100 lines means something belongs in a reference or script; it never means cram harder.

## The description field

The description is the trigger: the only text the model reads when deciding whether to load the skill.

- Cap at 1024 characters. Write in third person.
- Shape: what it does + when to use it + key capabilities.
- Include the exact trigger words the user actually says, verbatim. The model matches phrasing, and the user's phrasing is data it cannot guess.

## Deeper

`references/playbook.md` — a worked playback, a worked before/after, the failure modes, and how to turn the playback into a test.
