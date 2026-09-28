# Behavioral Economics for UX

An agent skill that turns behavioral-economics frameworks into a repeatable UX workflow.

Use it when a flow has high intent and low completion — abandoned carts, unfinished signup, skipped setup, unused features, or research that says "users would" while analytics say they did not.

Usability answers *can they?* This skill answers *will they?*

## Prerequisites

The skill will **not** invent a product. Give it at least one of these, or it will stop and ask:

- Chat history or a short project summary
- PRD, one-pager, or designer / developer spec
- Figma file, frames, or design-system file
- Screenshots or a recording of the full flow
- Project folder with screens, components, and assets
- Analytics, session recordings, or support tickets

A one-line ask such as "audit my signup" is not enough. The agent should return mixed multiple-choice and open-ended questions (see `references/intake.md`) until it can lock:

1. Product / surface
2. One specific target behavior
3. A step list *or* screens to derive one
4. The problem type (drop-off, non-start, regret, or unknown)

## What it does

Once context is locked, the agent:

1. Forces one uncomfortably specific target behavior
2. Maps actual steps, not the happy path
3. Tags barriers and benefits per step
4. Changes **one** barrier or one benefit
5. Writes a testable hypothesis
6. Pairs a success metric with a counter metric (regret, refunds, support)
7. Refuses sludge and dark patterns

Default framework is **3B** (Behavior, Barriers, Benefits). COM-B, Fogg `B=MAP`, and EAST are included for diagnosis and idea generation.

## Repo layout

```
SKILL.md                          # loaded by the agent
references/frameworks.md          # 3B, COM-B, Fogg, EAST
references/ethics-and-sludge.md   # nudge vs sludge
references/intake.md              # context gate and question bank
examples/test-prompts.md          # prompts to try the skill
LICENSE                           # MIT
```

## Install

### Grok

Copy `SKILL.md` and `references/` into:

```
/home/workdir/.grok/skills/behavioral-economics-ux/
```

The skill loads from its `description` frontmatter.

### Claude Code / Codex-style agents / Cursor

```bash
git clone https://github.com/budaykumar754/behavioral-economics-ux.git
```

Place the folder so the agent sees:

```
<skills-root>/behavioral-economics-ux/SKILL.md
<skills-root>/behavioral-economics-ux/references/
```

## Test it

Open `examples/test-prompts.md`. Prompt 0 (no context) should produce intake questions, not an audit. Prompts with a full brief should return a Context lock plus all nine output sections.

If the agent recommends fake urgency, hidden fees, or confirmshaming, the skill is not loaded.

## Sources

- 3B Framework — Irrational Labs
- COM-B — Michie, Atkins, and West
- Fogg Behavior Model — BJ Fogg
- EAST — Behavioural Insights Team
- Practice framing — Nielsen Norman Group, *The Hidden Why: Behavioral Economics for UX* (Thompson, 2026)

## License

MIT. See `LICENSE`.
