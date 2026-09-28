# Context intake

Read this before asking questions. Do not invent a product, flow, or audience to fill gaps.

## Accepted inputs (any one can start the work)

The user does not need all of these. One artifact plus answers to the missing slots is enough.

| Input | What to extract |
|-------|-----------------|
| Chat history or project summary | Product name, users, the flow under discussion, prior decisions |
| PRD or one-pager | Problem, goals, non-goals, target user, success metric |
| Designer or developer spec | Constraints, states, edge cases, what is already built |
| Figma file, frames, or design-system file | Actual screens, components, copy, tokens, variants |
| Screenshots or recording of a full flow | Real step order, fields, errors, dead ends |
| Project folder (screens, components, assets) | Implemented UI vs intended UI |
| Analytics, session recordings, support tickets | Where intention dies |

If Figma is connected and the user pastes a file URL, inspect the frames for the named flow before asking questions you can already answer from the file.

If a project folder exists in the workspace, list screens and read the ones that match the flow before asking.

## How to ask

Prefer a structured question tool (`ask_user_question` or the host's equivalent) so choices are tappable.

Rules:

- Ask only what the artifacts do not already answer.
- Batch 3–5 questions per turn. Never dump 15.
- Mix multiple-choice (fast) with one or two open-ended (precise).
- Always include an "Other / I'll paste it" style option so the user can attach a file instead of typing.
- After the first batch, summarize what you now believe in 5 lines and ask them to correct it. Then run the 3B (or other) workflow.

If the user says "just guess" or "generic example," label the output **provisional** and keep every step marked as assumed. Still ask for the target behavior in one sentence.

## Question bank

Use the smallest set that fills the empty slots.

### Round 1 — what are we looking at

**Q1. What can you share right now?** (multi-select)

- Chat history or a short project summary
- PRD / one-pager / spec
- Figma link or design-system file
- Screenshots or a loom of the full flow
- Repo or folder with screens, components, assets
- Analytics or support quotes
- Nothing yet — ask me questions

**Q2. What kind of surface is this?** (single)

- Marketing / landing
- Signup or onboarding
- Core app task (the job they came to do)
- Checkout / upgrade / paywall
- Settings, cancel, or account
- Email, push, or other prompt
- Other (I'll describe)

**Q3. What is going wrong?** (single)

- People start and do not finish
- People never start
- People finish and regret it (refunds, cancel, support)
- People say they will, behavior says they don't
- We do not know yet — we need a diagnosis
- Other (I'll describe)

**Q4. Open.** In one sentence, who is the user and what should they have done when they are "done"?

### Round 2 — only if still thin

**Q5. Who is in motion?** (single)

- First-time visitor
- Signed-up but not activated
- Returning customer
- Internal user (staff, ops)
- Mixed / not sure

**Q6. What evidence exists?** (multi-select)

- Funnel or drop-off numbers
- Session recordings
- Usability test notes
- Support tickets / store reviews
- Stakeholder opinion only
- None

**Q7. How high-stakes is the action?** (single)

- Casual and reversible
- Money or contract
- Health, legal, or identity
- Not sure

**Q8. Open.** What must we not do (brand, legal, ethics)? What is already off the table?

**Q9. Open.** Paste the current step list, or say "map it from the screens I'll attach."

### Round 3 — Figma / folder present but flow unnamed

**Q10.** Which flow should I audit? (single or short list built from frame names you actually saw)

**Q11.** Is the live product different from these designs? (single)

- Designs are source of truth
- Live product is source of truth
- Audit both and call out drift

## Minimum to proceed

Do not write the 9-section audit until you have:

1. Product or surface (even a one-line description)
2. One target behavior written as who + does what + when + done
3. Either a step list or screens/screenshots/Figma frames to derive one
4. A stated problem (drop-off, non-start, regret, or unknown)

If 3 is missing, stop and ask for screens or a step list. A barrier table invented from a blank page is worse than no audit.

## After they answer

Write a 5-line **Context lock** at the top of the audit:

- Product and audience
- Surface / flow
- Target behavior
- Evidence used (artifact names, not vibes)
- Assumptions still open

Then run the workflow in SKILL.md.
