# Frameworks cheat sheet

Use this file when SKILL.md is not enough. Pick one primary framework per analysis.

## 3B — Behavior, Barriers, Benefits (Irrational Labs)

Best default for product UX. Three questions:

1. **Behavior** — What exact action, by whom, when, and what does done look like?
2. **Barriers** — What makes that action harder in this context?
3. **Benefits** — What makes it feel worth doing *now*?

Then intervene on one barrier or one benefit.

Get uncomfortably specific. "Increase retention" is not a behavior. "Returning free users complete one saved-search alert setup within 24 hours of second visit" is.

Barrier categories that show up constantly in digital products:

- Attention and noticeability
- Cognitive load and choice overload
- Self-relevance / identity mismatch
- Unclear value
- Status quo and present bias
- Commitment anxiety and loss aversion
- Effort, time, hassle
- Mental-model mismatch
- Social risk
- Trust and privacy fear

Benefit types that actually move action:

- Immediate functional (access, speed, money now)
- Immediate emotional (belonging, relief, competence, pride)
- Later functional (savings over a year)
- Later emotional (future self)

Present bias means later-functional benefits lose to small present barriers. If the flow asks for commitment now and pays off later, add a now-benefit or cut a now-barrier.

## COM-B — Capability, Opportunity, Motivation → Behavior (Michie, Atkins, West)

Use when the stuck behavior is bigger than one form.

| Component | Sub | UX questions |
|-----------|-----|----------------|
| Capability | Physical | Can their body / device / assistive tech do this? |
| Capability | Psychological | Do they know how? Can they hold the steps in mind? |
| Opportunity | Physical | Is there time, access, money, a working path? |
| Opportunity | Social | Do norms, other people, or culture support it? |
| Motivation | Reflective | Do they plan to do it? Does it fit their goals? |
| Motivation | Automatic | Does habit, emotion, or impulse pull toward or away? |

All six can be present and the behavior still fails if a competing behavior wins at that moment. Diagnose the missing piece; do not assume motivation.

COM-B is a diagnosis model. After diagnosis, design the intervention and test it. The Behaviour Change Wheel maps deficits to intervention functions (education, persuasion, incentivization, coercion, training, restriction, environmental restructuring, modeling, enablement). For product UX, environmental restructuring and enablement are usually the honest first tools.

## Fogg Behavior Model — B = MAP (BJ Fogg)

A behavior happens when Motivation, Ability, and a Prompt converge *at the same instant*.

- **Motivation** — hope/fear, pleasure/pain, social acceptance/rejection in that moment
- **Ability** — simplicity. Time, money, physical effort, mental effort, social deviance, non-routine
- **Prompt** — the cue that says "do it now"

If the behavior did not happen, name which element was missing.

| State | What to do |
|-------|------------|
| High motivation, low ability | Make it easier. Do not add pep talks. |
| High ability, low motivation | Do not spam prompts. Change timing or the now-benefit. |
| Both high, no prompt | Add a prompt at that moment. |
| Both low | Do not prompt. You will train people to ignore you. |

Prompt types:

- Spark — used when motivation is low (use sparingly; easy to become sludge)
- Facilitator — used when ability is low (the prompt also makes the action easier)
- Signal — used when motivation and ability are already high (reminder only)

Tiny Behaviors: if ability cannot be raised enough, shrink the behavior until it is easy (one field, one click, one saved item).

## EAST — Easy, Attractive, Social, Timely (Behavioural Insights Team)

Use after diagnosis to generate options. Not a diagnosis by itself.

- **Easy** — defaults, fewer steps, pre-fill, plain language, remove optional fields
- **Attractive** — salience, rewards designed for now, attractive framing
- **Social** — show what people like the user do; commitments; make the action visible when that helps
- **Timely** — prompt when the user is already in motion; help them plan the next action; respect present bias

EAST ideas still need a hypothesis and a counter metric.

## How they relate

```
COM-B          why the behavior system is incomplete
3B             what to inspect in a product flow
Fogg           whether this moment can produce the action
EAST           how to rewrite the environment
```

A clean pass: COM-B or 3B to diagnose → Fogg to check the moment → EAST to draft the intervention → test.

## Common failure modes

- Treating education as the intervention when the barrier is effort or anxiety
- Adding more benefits (badges, points, copy) on top of a broken path
- Copying a nudge from another product without matching context
- Measuring clicks instead of the specified target behavior
- Ignoring competing behaviors (compare, postpone, ask a friend, leave)
