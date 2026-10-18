# Dietitian

**A conversation-first nutrition coaching framework for AI.**

Dietitian helps people understand their goals, everyday eating habits, preferences, and realistic ways to make progress. It is an open-source set of instructions and templates—not an app, medical service, meal plan, or precision food tracker.

## Start here

1. Open [INSTRUCTIONS.md](INSTRUCTIONS.md) and give its contents to your AI assistant as the short core guide (for example, paste it into an AI conversation or supported custom instructions). A GitHub link alone does not automatically load the file.
2. Say something natural, such as **"I'd like help figuring out an approach to eating that works for me."**
3. Talk through goals, favorite meals, dislikes, schedules, and what feels sustainable. You do not need an intake form.
4. Use [CONTEXT_LOADING.md](CONTEXT_LOADING.md) to select context. If your AI can access individual files on demand, it may load [DISCOVERY.md](DISCOVERY.md) or [JOURNALING.md](JOURNALING.md) when relevant. Otherwise, paste the relevant guide only when that activity comes up.
5. Keep any completed personal context outside this repository. [CONTEXT_TEMPLATE.md](CONTEXT_TEMPLATE.md) provides optional headings, not fields you must fill.

A useful first conversation leaves you feeling understood, with one achievable next step—not a completed questionnaire.

**Quick route:** New here? Use the core instructions plus the [discovery guide](DISCOVERY.md) if useful. Talking about today's meals? Bring in the [optional journaling guide](JOURNALING.md). Need to carry preferences across sessions? See [context loading](CONTEXT_LOADING.md) and the [private template](CONTEXT_TEMPLATE.md). There is no need to load all files.

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

## Before you share or publish

Try the first-time steps with a fresh AI conversation. Check that links open the intended files, that onboarding does not require filling a template, and that the assistant does not claim automatic access to private notes. Review **all files and Git history** for personal information before making the repository public. A clean current README does not guarantee a clean commit history.

## Privacy and limitations

Never publish completed context, food logs, health details, or other identifiable information. Review the repository and its commit history for sensitive material before changing visibility to public. AI context and memory behavior differ among products; this repository does not promise automatic memory, complete retrieval, exact nutrition data, or continuity between sessions. Do not present the assistant as a licensed clinician.
