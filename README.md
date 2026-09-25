# Behavioral Economics for UX

An agent skill that turns behavioral-economics frameworks into a repeatable UX workflow.

Use it when a flow has high intent and low completion — abandoned carts, unfinished signup, skipped setup, unused features, or research that says "users would" while analytics say they did not.

Usability answers *can they?* This skill answers *will they?*

## What it does

The agent:

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
examples/test-prompts.md          # prompts to try the skill
LICENSE                           # MIT
```

## Install

### Grok

Copy the `SKILL.md` and `references/` folder into:

```
~/.grok/skills/behavioral-economics-ux/
```

or, in this workspace:

```
/home/workdir/.grok/skills/behavioral-economics-ux/
```

The skill loads from its `description` frontmatter. You do not have to @-mention it if the prompt matches the triggers.

### Claude Code / Codex-style agents / Cursor

Clone this repo into the product's skills directory:

```bash
git clone https://github.com/budaykumar754/behavioral-economics-ux.git
```

Then copy or symlink so the agent sees:

```
<skills-root>/behavioral-economics-ux/SKILL.md
<skills-root>/behavioral-economics-ux/references/
```

Any agent that follows the [Agent Skills](https://agentskills.io) layout only needs `SKILL.md` plus the referenced files.

### Manual

Paste `SKILL.md` into the agent's custom instructions and keep `references/` next to it so relative paths resolve.

## Test it

Open `examples/test-prompts.md` and run one prompt against an agent that has the skill loaded. A passing run returns all nine output sections:

1. Target behavior
2. Behavior map
3. Barrier table
4. Benefit table
5. Priority
6. Intervention
7. Hypothesis
8. Measure (primary + counter)
9. Ethics check

If the agent recommends fake urgency, hidden fees, or confirmshaming, the skill is not loaded or is being overridden. Check the description triggers and the ethics file.

## What this is not

- Not a copy of the NN/G article. The article is source material; this skill is an original procedure.
- Not a bias encyclopedia. The model already knows anchoring and loss aversion.
- Not permission to ship dark patterns under academic names.

## Sources

Frameworks used in the skill:

- 3B Framework — Irrational Labs
- COM-B — Michie, Atkins, and West
- Fogg Behavior Model — BJ Fogg
- EAST — Behavioural Insights Team
- Practice framing — Nielsen Norman Group, *The Hidden Why: Behavioral Economics for UX* (Thompson, 2026)

Read the article. Do not paste it into the skill.

## License

MIT. See `LICENSE`.
