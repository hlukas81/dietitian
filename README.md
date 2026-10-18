# Dietitian

**A conversation-first nutrition coaching framework for AI.**

Dietitian helps people understand their goals, everyday eating habits, preferences, and realistic ways to make progress. It is an open-source set of instructions and templates—not an app, medical service, meal plan, or precision food tracker.

## For AI assistants opening this README

If a user shares this README and asks to get started, read [INSTRUCTIONS.md](INSTRUCTIONS.md) as the core guidance, then begin a natural conversation about their goals and food preferences. Consult [DISCOVERY.md](DISCOVERY.md), [JOURNALING.md](JOURNALING.md), and [CONTEXT_LOADING.md](CONTEXT_LOADING.md) only when relevant. Do not load every file automatically or ask the user to complete a questionnaire. Respect medical constraints and do not claim access to personal context you cannot retrieve.

## Share with a friend

Give your AI this link: https://github.com/hlukas81/dietitian/blob/main/README.md and say, "Read this README and help me get started with Dietitian." If your AI cannot browse GitHub, copy the contents of [INSTRUCTIONS.md](INSTRUCTIONS.md) into the chat instead.

## Getting started

If your AI can open GitHub links, simply share the [README link](https://github.com/hlukas81/dietitian/blob/main/README.md) and ask it to help you get started. The assistant should read the [core guide](INSTRUCTIONS.md) first and then lead a natural conversation about your goals, the foods you enjoy, and what is practical for you.

There is no required intake form or account setup. Supporting guidance is available selectively: [discovery](DISCOVERY.md) for an initial conversation, [optional journaling](JOURNALING.md) for rough food-pattern discussions, and [context loading](CONTEXT_LOADING.md) for selecting just the relevant information. [EXAMPLES.md](EXAMPLES.md) and [CONTEXT_TEMPLATE.md](CONTEXT_TEMPLATE.md) are references, not required reading.

If the AI cannot follow the link, paste the [core instructions](INSTRUCTIONS.md) as a fallback. Do not paste the whole repository by default. Personal context belongs outside this repository.

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
