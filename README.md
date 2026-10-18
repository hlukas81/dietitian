# Dietitian

**A conversation-first nutrition coaching framework for AI.**

Dietitian helps people understand their goals, everyday eating habits, preferences, and realistic ways to make progress. It is an open-source set of instructions and templates—not an app, medical service, meal plan, or precision food tracker.

## Start here

1. Give your AI assistant [INSTRUCTIONS.md](INSTRUCTIONS.md) as its short, persistent guide.
2. Say something natural, such as **"I'd like help figuring out an approach to eating that works for me."**
3. Talk through goals, favorite meals, dislikes, schedules, and what feels sustainable. You do not need an intake form.
4. If your AI environment can access individual files on demand, follow [CONTEXT_LOADING.md](CONTEXT_LOADING.md) to retrieve only the relevant private context and instructions.
5. Keep any completed personal context outside this repository. [CONTEXT_TEMPLATE.md](CONTEXT_TEMPLATE.md) provides optional headings, not fields you must fill.

A useful first conversation leaves you feeling understood, with one achievable next step—not a completed questionnaire.

## Philosophy

**Build around food people enjoy. Change what matters, not everything.**

- Ask one relevant question at a time, as a thoughtful, direct friend would.
- Learn how the person actually eats before recommending changes.
- Treat enjoyment, convenience, routines, and tradeoffs as legitimate design constraints.
- Offer useful ideas early instead of requiring onboarding completion.
- Let people discover their own goals and obstacles through conversation.
- Notice patterns over time, but never turn one meal into a permanent preference.
- Respect reported clinician guidance. Do not diagnose or prescribe treatment.

## Optional conversational food journaling

If it naturally comes up, someone can describe food casually throughout the day. Dietitian can estimate roughly and help spot patterns; it should not demand weighed portions or meticulous data entry. Estimates are imperfect, and conversational logs are not a reliable permanent food database. Food journaling is entirely optional.

## Layered context and token use

| Layer | When used | Content |
| --- | --- | --- |
| Core | Every session | [INSTRUCTIONS.md](INSTRUCTIONS.md) |
| Relevant private context | Only as needed, subject to essential safety constraints | Goals, preferences, nutrition targets, constraints, and today's working notes |
| Task guide | Only for that activity | [DISCOVERY.md](DISCOVERY.md) or [JOURNALING.md](JOURNALING.md) |
| Examples/reference | Occasionally | [EXAMPLES.md](EXAMPLES.md), blank [CONTEXT_TEMPLATE.md](CONTEXT_TEMPLATE.md) |

**Minimum sufficient context, not minimum tokens.** Never omit a material constraint simply to save tokens. The framework cannot automatically fetch files unless the user's AI environment supports it. If selective retrieval is unavailable, supply a concise core and relevant manually selected context. Read [CONTEXT_LOADING.md](CONTEXT_LOADING.md) for the practical rules and limitations.

## Repository files

- [INSTRUCTIONS.md](INSTRUCTIONS.md): canonical short core instructions.
- [DISCOVERY.md](DISCOVERY.md): gentle, preference-first conversation guidance for new users.
- [CONTEXT_LOADING.md](CONTEXT_LOADING.md): layered context, retrieval checks, and token discipline.
- [JOURNALING.md](JOURNALING.md): optional, approximate conversational food journaling.
- [CONTEXT_TEMPLATE.md](CONTEXT_TEMPLATE.md): private durable-context template.
- [EXAMPLES.md](EXAMPLES.md): fictional examples, not persistent prompt material.

## Privacy and limitations

Never publish completed context, food logs, health details, or other identifiable information. Review the repository and its commit history for sensitive material before changing visibility to public. AI context and memory behavior differ among products; this repository does not promise automatic memory, complete retrieval, exact nutrition data, or continuity between sessions. Do not present the assistant as a licensed clinician.
