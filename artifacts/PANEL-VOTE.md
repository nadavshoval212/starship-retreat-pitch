# PANEL VOTE · gemini-3.1-pro

| Skill | Job | Steps | Locks | Output | Fail | Vote | One-line evidence |
|---|---|---|---|---|---|---|---|
| W2-1 world-class-cfo | 5 | 3 | 5 | 4 | 5 | FIX | Good locks and job clarity, but lacks actionable steps for the agent to follow. |
| W2-2 nadav-negotiation | 5 | 4 | 5 | 5 | 5 | PASS | Clear PREP/LIVE/DRAFT steps, strong safety locks, and well-defined output shape. |
| W2-3 commandry-brand-book | 3 | 1 | 1 | 2 | 1 | FIX | Essentially just a pointer to Notion; lacks steps, output shape, and safety locks. |
| W2-4 legal-counsel | 5 | 5 | 5 | 5 | 5 | PASS | Excellent clarity, step-by-step intake, strong legal/irreversible action locks, and clear desk splits. |
| W2-5 personal-trainer | 3 | 2 | 3 | 2 | 2 | FIX | Mostly a pointer to Notion; lacks concrete steps and output shape, though it has basic routing/health locks. |

## Top 3 FIX diffs (if any)
1. W2-1 world-class-cfo · Missing actionable execution steps · Add a `## Steps` section detailing exactly how to execute a CFO task (e.g., intake, compute, format, check).
2. W2-3 commandry-brand-book · Missing steps, locks, and output shape · Add `## Absolute` gates, `## Steps` for execution, and an `## Output Shape` to ensure quality even if Notion fetch fails.
3. W2-5 personal-trainer · Missing actionable steps and output shape · Add a `## Steps` section for generating workouts/plans and define the exact `## Output Shape` for the dated plan.

## Disagreement notes
- W2-3 and W2-5 rely heavily on fetching a Notion page. If the Notion fetch fails or is unavailable, the skill provides almost no value. They need fallback instructions or core gates in the markdown file itself.
- W2-1 has strong rules ("Math locks", "Absolute") but doesn't tell the agent *how* to proceed step-by-step, which might lead to inconsistent execution.