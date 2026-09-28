---
name: behavioral-economics-ux
description: Apply behavioral-economics frameworks to UX so intention becomes action. Trigger on behavioral economics, intention-action gap, 3B, COM-B, Fogg, EAST, nudge, friction audit, conversion drop-off, or high intent with low completion. Requires project context (PRD, specs, Figma, screenshots, chat summary, or a project folder). If none is given, stop and run intake questions before analyzing.
metadata:
  version: "1.1"
  source: Distilled from NN/G Behavioral Economics for UX plus COM-B, Fogg, 3B, and EAST
---

# Behavioral Economics for UX

Close the gap between what users intend to do and what they actually do. Usability answers "can they?" Behavioral economics answers "will they?"

Do not lecture users into acting. Change the environment around the action.

## When to use this skill

Use it when a flow has drop-off, abandoned carts, unfinished signup, skipped setup, unused features, or "users said they would" research that does not match behavior.

Do not use it to justify dark patterns, hidden fees, fake scarcity, or forced continuity. If the intervention helps the business and harms the user, reject it.

## Context gate (do this first)

Do not invent a product or flow. Do not run 3B/COM-B/Fogg/EAST on a one-line ask.

**Accepted inputs** — any one can start the work; more is better:

- Chat history or a project summary already in the thread
- PRD, one-pager, or designer/developer spec
- Figma file, frames, or design-system file
- Screenshots or a recording of the full flow
- Project folder with screens, components, and assets
- Analytics, session recordings, or support tickets

Scan the thread and workspace for these before asking. If Figma or a folder is available, inspect the relevant frames/screens first so you do not re-ask what the artifacts already show.

### If context is missing

Stop. Do not produce the 9-section audit.

1. Read `references/intake.md`.
2. Ask a short mixed batch (3–5 questions) — multiple-choice plus one or two open-ended.
3. Prefer a structured question tool (`ask_user_question` or the host equivalent) when it exists.
4. Always offer a way to paste or attach artifacts instead of answering.
5. After answers, write a 5-line **Context lock** (product, surface, target behavior, evidence, open assumptions) and only then start the workflow.

Minimum to proceed: product/surface + one specific target behavior + either a step list or screens to derive one + a stated problem (drop-off, non-start, regret, or unknown).

If the user insists on a generic example, mark every section **provisional** and still force a specific target behavior.

## Choose a framework

Pick one primary lens. Do not stack all four on the first pass.

| Situation | Use |
|-----------|-----|
| Drop-off in a known flow; need a fast audit | 3B (Behavior, Barriers, Benefits) |
| Unclear whether the problem is skill, context, or desire | COM-B |
| Moment-of-action design (prompt, simplify, motivate) | Fogg B=MAP |
| Generating intervention ideas after diagnosis | EAST |

Default to **3B** for product/UX work. Switch to COM-B when the problem is broader than a single screen (capability or social opportunity is in play). Use Fogg when the question is "why didn't this prompt fire?" Use EAST to brainstorm fixes after the diagnosis.

Details live in `references/frameworks.md`.

## Workflow (3B default)

### 1. Define one uncomfortably specific behavior

Write the behavior as who + does what + when + what done looks like.

- Weak: Increase gym memberships.
- Strong: A first-time visitor selects a plan, enters required details, and clicks Start Membership in one session.

One behavior per analysis. Competing behaviors (leave, compare, delay) are barriers, not extra targets.

Then map the actual steps, not the happy path. Include searches, comparisons, policy checks, form fields, and decision pauses. Use analytics and recordings when available; otherwise mark the map as provisional.

A behavior map is not a journey map. It records actions and conditions, not emotions. Emotions appear in the next two steps.

### 2. Name barriers at each step

A barrier is anything that makes the action harder right now. Scan for:

- Attention (never noticed the next step)
- Cognitive load / choice overload
- Unclear value or self-relevance ("is this for me?")
- Status-quo / present bias (later feels safer)
- Uncertainty and commitment anxiety (lock-in, fine print)
- Effort, time, or hassle costs
- Broken mental models
- Social risk (looking foolish, being judged)
- Fear of loss (money, data, options)

Tie each barrier to a specific step. "Users are confused" is not a finding. "At plan comparison, users cannot map amenities to outcomes they care about" is.

### 3. Name benefits at each step

A benefit is why the action feels worth it now. Rank benefits with this matrix:

| | Functional | Emotional |
|---|---|---|
| Later | Save money over a year | Feel proud eventually |
| Now | Get access today | This place is for people like me |

Prioritize now + emotional when motivation is the bottleneck. Future-functional benefits rarely beat present friction.

Look for existing benefits the UI already creates (progress, social proof, endowment, instant preview) before inventing new ones.

### 4. Intervene on one thing

Pick one barrier to remove or one benefit to amplify — the one most likely to move the target behavior.

Write a testable hypothesis:

If we [change] at [step], then [metric on the target behavior] will [direction], because [mechanism].

Design the smallest intervention that tests the mechanism. Honest examples:

- Identity cues and social proof that match the real audience
- Defaults and pre-filled fields that cut effort
- Decision aids that collapse comparison
- Immediate taste of value before commitment
- Reassurance at commitment-anxiety steps (cancel terms in plain language)
- Prompts that fire when ability and motivation are both high

Specify how you will measure it. Pair the target-behavior metric with a counter metric (regret, refunds, support contacts, unsubscribe, time-to-regret) so you do not win by trapping people.

## Other frameworks in one pass

**COM-B** — Behavior happens when Capability, Opportunity, and Motivation are all present.

- Capability: physical + psychological (knowledge, skills, cognitive capacity)
- Opportunity: physical + social (time, access, cues, norms)
- Motivation: reflective (plans, beliefs) + automatic (habit, emotion, impulse)

Diagnose which of the six is missing before designing.

**Fogg B=MAP** — Behavior = Motivation + Ability + Prompt at the same moment. If the action failed, at least one of the three was missing. High motivation + low ability → simplify. High ability + low motivation → do not nag; change the reward or wait for a better moment. No prompt → the behavior never starts.

**EAST** — Make the action Easy, Attractive, Social, and Timely. Use as an idea generator after diagnosis, not as a substitute for it.

## Output format

Start with a **Context lock** (5 lines). Then return work in this order:

1. Target behavior — one specific sentence
2. Behavior map — numbered actual steps
3. Barrier table — step / barrier type / evidence / severity
4. Benefit table — step / benefit type (now-emotional, now-functional, later) / gap
5. Priority — the single barrier or benefit to attack first, with why
6. Intervention — what changes in the UI/copy/flow
7. Hypothesis — if / then / because
8. Measure — primary metric + counter metric + how you will know it worked
9. Ethics check — whose interest this serves; what you refused to do

Keep the writeup short enough to hand to a designer or PM.

## Ethics (non-negotiable)

- Align the target behavior with a user goal they already have, or stop.
- Disclose costs, terms, and commitment before the action, not after.
- Do not manufacture scarcity, social proof, or urgency.
- Prefer removing friction over adding pressure.
- If users would be upset when they notice the tactic, it is sludge, not design.

See `references/ethics-and-sludge.md` when the request smells like persuasion-at-all-costs.

## Avoid

- Running the audit on a one-line ask with no product, screens, or spec
- Inventing screens, copy, or metrics the user did not provide
- Diagnosing "users need more education" as the first answer
- Adding benefits while leaving the biggest barrier in place
- Targeting five behaviors in one pass
- Copying a famous nudge into a different context without a hypothesis
- Treating stated intent (surveys) as behavior
- Recommending dark patterns wrapped in behavioral jargon
