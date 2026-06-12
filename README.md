# Becoming Augmented — Skills

Open-source Claude Code skills for building leaner, clearer agents.

Each folder is one skill. Copy it into `~/.claude/skills/` and it works.

## Skills

| Skill | What it does |
|-------|--------------|
| [ruthlessly-simplify](ruthlessly-simplify/) | Lean out an existing skill: cut what the model already knows, rewrite what stays into clear, concise, concrete language, and keep what only the owner knows. |

## Install

1. Copy a skill folder into `~/.claude/skills/` (machine-level) or your project's `.claude/skills/`.
2. Start a new Claude Code session.
3. Trigger it in plain words. For example: "ruthlessly simplify my-skill".

## The thinking behind these skills

Agent context bloats. Builders over-instruct what the model already knows, and the cost lands on both readers: the model follows diluted instructions less reliably, and a file too long to read end-to-end never gets verified by a human.

These skills follow a small set of design beliefs:

1. **The model is already smart.** The only useful context is what it cannot know: your position, your methods, your hard-won lessons.
2. **Attention is finite.** Every line dilutes every other line. Fewer, clearer lines perform better and cost less.
3. **Context nobody re-reads becomes wrong over time.** Short documents stay true. Cap files at 100 lines.
4. **Writing standard: clear, concise, concrete.** In priority order. No metaphors, no filler, no rhetoric.
5. **Depth is relocated, never deleted.** Modular files, progressive disclosure, references one level deep.

## License

MIT
