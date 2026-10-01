# Dietitian

Dietitian is an open context framework for using a large language model as a practical nutrition and behavior coach.

It is not a diet program, medical service, diagnosis tool, or treatment system. Its purpose is to help an LLM learn how a person actually eats, what they are trying to accomplish, what patterns matter, and how they want to be coached.

The framework is deliberately small enough that the important rules can be supplied to an LLM together rather than scattered across a large knowledge base.

## Core model

Dietitian separates three things:

1. **Framework rules** — general instructions for how the LLM should behave.
2. **Personal context** — user-specific goals, preferences, routines, constraints, and coaching preferences.
3. **Current conversation** — today's meals, questions, decisions, and short-term circumstances.

The open-source repository contains only the framework. Personal context belongs to the individual user and should remain private.

## Files

- `INSTRUCTIONS.md` — canonical operating rules for the LLM.
- `DISCOVERY.md` — how the LLM should learn about a user over time.
- `CONTEXT_TEMPLATE.md` — template for a user's private durable context.
- `EXAMPLES.md` — fictional examples showing intended behavior.
- `.gitignore` — helps prevent private context and logs from being committed.
- `LICENSE` — open-source license.

## How to use it

1. Give your LLM `INSTRUCTIONS.md`.
2. Use `DISCOVERY.md` while establishing your initial context.
3. Copy `CONTEXT_TEMPLATE.md` into a private file such as `CONTEXT.md`.
4. Fill that private context progressively through conversation.
5. Supply the framework instructions, your private context, and the current conversation to the LLM.
6. Update durable context only when something is genuinely stable or explicitly chosen.

## Design principles

Dietitian is built around a few principles:

- Keep the rule set small and explicit.
- Prefer sustainable behavior change over temporary restriction.
- Treat food neutrally rather than morally.
- Separate intentional choices from automatic behavior.
- Use meaningful protein, satiety, energy, enjoyment, and adherence as practical anchors.
- Learn a person's preferences instead of forcing a generic meal plan.
- Do not turn one unusual meal into a permanent preference.
- Do not invent missing user facts.
- Do not provide medical advice.

## Privacy

Do not commit personal nutrition context, medical information, food logs, body measurements, or other private user information to this repository.

The template is public. The completed user context is not.

## Status

This repository is intentionally starting small. The framework should grow only when a new file or rule solves a real recurring problem without duplicating existing instructions.
