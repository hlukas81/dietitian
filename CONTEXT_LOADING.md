# Layered Context: Minimum Sufficient Information

This guide specifies **what** context to select. Automatic retrieval only works if the host assistant or app actually supports searching/loading private files or memory; Markdown instructions cannot create those capabilities.

## Three practical layers

1. **Always-present core:** `INSTRUCTIONS.md`; keep concise and stable.
2. **Selective private context:** the smallest relevant sections of an individual's private profile, plus any essential safety constraints. Load when needed, not all at every turn.
3. **Task module:** `DISCOVERY.md` during discovery; `JOURNALING.md` for an optional rough food journal; examples as reference only.

The template is not the user's profile. Do not send the blank template or all example cases with each message.

## Before responding

1. Identify the user's actual task: goal-setting, ordinary question, meal mention, rough journaling, or substantial nutrition change.
2. Use context already available in the live conversation. Avoid redundant re-fetching.
3. Identify potentially outcome-changing facts: relevant allergies, medical/clinician constraints, restrictions, goals, chosen targets, preferences, and activity as appropriate.
4. Retrieve the relevant private sections if supported. For important recommendations, widen the retrieval scope when confidence is low. **Missing evidence is not evidence of absence.**
5. If a necessary fact cannot be accessed, ask one targeted question or qualify the recommendation. Never invent.
6. Reply concisely. Only offer additional depth if useful.

## Suggested task routing

| Task | Usually relevant | Usually unnecessary |
| --- | --- | --- |
| Initial conversation | Core + discovery guide; emerging goals/preferences | Whole profile, all examples |
| Ordinary meal question | Core + relevant preferences, constraints | Full discovery guide and historical logs |
| Casual food mention | Core; today's notes only if useful | Exhaustive history and precision calculations |
| Rough daily journal | Core + journaling guide + today's working notes + user-chosen targets | Full biography |
| Exercise fueling | Core + relevant activity, eating pattern, restrictions | Unrelated food likes and historical logs |
| Substantial change to diet | Core + broader goal, medical constraints, preferences, current routines | Irrelevant transcripts |

## Working notes versus durable profile

- **Durable:** stable goals, chosen rules/targets, likes/dislikes, relevant routines, user-reported clinician guidance, communication preferences. Store privately, with consent and product support.
- **Transient:** daily meals, rough estimates, one-off deviations, pending corrections, today's totals. Keep in the current conversation or appropriately private daily notes, if supported.
- Update durable context only for explicit decisions or verified patterns; do not automatically promote casual food entries.
- If a new day is explicit, reset the daily working log. Do not erase lasting preferences.

## Budgeting without missing important information

Optimize for **minimum sufficient context**, not a strict token ceiling. Keep core concise, route to one appropriate guide, and use short structured summaries of relevant private facts. If a retrieval or safety check needs more context, expand without a preset cutoff. Do not omit known relevant constraints to hit a token target.

A model may lose previous messages to context-window limits, and some environments cannot reliably retrieve external private context. Be candid about those limits. Where retrieval is unavailable, users can provide or paste a short relevant profile themselves. Do not imply seamless memory.

## Privacy

Never include sensitive personal context in this repository or example commits. Keep personal notes in the user's chosen private storage and load only for authorized use. Before sharing any repository publicly, inspect files **and commit history** for private information.
