# B2B Messaging Workshop

A self-guided B2B messaging workshop that produces your Product Marketing Source of Truth.

The plugin guides a founder or product marketer through the Eldur Studio framework one section at a time:

1. Company snapshot
2. Product marketing strategy
3. Positioning
4. Pressure test

At every step it shows the template's original guidance, asks focused questions, and checks the answer for specificity and evidence. `See an example` reveals one clearly fictional ExampleCo Legal answer without advancing the workshop or changing the user's work.

## What v1 includes

- A free, skills-only plugin with no hosted server, account, database, or telemetry.
- Conversational reply choices: `Answer naturally`, `See an example`, `Help me think`, `Skip`, `Back`, and `Pause`.
- Copyable checkpoints that preserve progress, approved answers, hypotheses, and gaps.
- Evidence and provenance rules that keep invented claims out of the result.
- Phase 2 synthesis from approved inputs and a six-part pressure test.
- A complete Markdown copy of the original template, filled with approved answers.
- Optional creation of a separate Notion page when Notion is connected and the user confirms the write.

V1 uses text replies rather than custom interface buttons. It never changes the canonical Notion template.

## Starter prompts

- `Start my B2B messaging workshop.`
- `Resume my messaging workshop from this checkpoint: ...`
- `Pressure-test my existing B2B messaging framework.`

## Repository structure

- `.codex-plugin/plugin.json` — plugin identity and starter prompts.
- `skills/run-b2b-messaging-workshop/` — the guided workshop skill.
- `skills/run-b2b-messaging-workshop/references/` — canonical template, question bank, synthesis rules, fictional examples, and evidence rules.
- `tests/publication-evals.md` — five positive, three negative, and behavioral publication checks.
- `tests/fixtures/` — reproducible research, checkpoint, and pressure-test fixtures.

## Validate locally

Run the OpenAI plugin and skill validators from their installed creator skills, then exercise the publication prompts in fresh conversations. The full expected behavior is documented in `tests/publication-evals.md`.

Public submission also requires verified publisher identity, a logo, website, support contact, privacy-policy and terms URLs, availability regions, and release notes. Those distribution details are intentionally not fabricated in this repository.

The canonical template and its guidance are owned by Eldur Studio LLC. Copyright Eldur Studio LLC 2026.
