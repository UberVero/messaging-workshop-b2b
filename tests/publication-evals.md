# Publication evals

These fixtures are designed for reviewer reproduction without private context. The plugin is skills-only, so expected behavior refers to the `run-b2b-messaging-workshop` skill rather than an MCP tool.

## Five positive tests

### 1. Start from scratch

**Prompt:** “Walk me through building a B2B messaging framework for my SaaS from scratch.”

**Expected behavior:** Activate the workshop, explain the four phases, show the original Phase 0 guidance, and ask for the company or product name together with the first focused questions.

**Expected result shape:** A single current step with `What to write here`, `Your question`, and the reply choices. It must not dump the full questionnaire.

**Fixture:** None.

### 2. Use supplied research without inventing evidence

**Prompt:** “Turn these interview notes into a Product Marketing source of truth, and guide me through the gaps: [attach or paste notes].”

**Expected behavior:** Extract only supported facts and sourced quotes, label inferences and gaps, begin at the earliest incomplete template section, and request approval section by section.

**Expected result shape:** A workshop ledger summary followed by one guided step. No fabricated quote, metric, or proof point.

**Fixture:** Use `fixtures/interview-notes.md`.

### 3. Show an example without contaminating state

**Prompt sequence:** Start a workshop, reach Industry problems, then reply “See an example.”

**Expected behavior:** Show only the fictional Industry problems answer, label it illustrative, keep the same progress indicator, and ask the original unanswered question again.

**Expected result shape:** `Fictional example — illustrative only, not your answer`, one section example, then the same unanswered question. No draft or approval prompt.

**Fixture:** Company name `Acme Ops`; no industry-problem answer supplied.

### 4. Resume from a checkpoint

**Prompt:** “Resume my messaging workshop from this checkpoint: [paste fixture].”

**Expected behavior:** Parse the checkpoint, summarize approved answers, hypotheses, and gaps, confirm the recorded next step, then display that step's exact guidance.

**Expected result shape:** Resume summary followed by Phase 1, Competitive alternatives. Approved fields remain unchanged.

**Fixture:** Use `fixtures/resume-checkpoint.md`.

### 5. Pressure-test an existing framework

**Prompt:** “Pressure-test this B2B messaging framework and help me repair what fails: [paste fixture].”

**Expected behavior:** Start Phase 3, run all six canonical checks, identify generic differentiation and unsupported proof, and route repairs to the correct Phase 1/2 sections.

**Expected result shape:** A six-row Pass/Fail/Unresolved summary plus the first failed source section's guidance and a focused repair question.

**Fixture:** Use `fixtures/framework-needing-pressure-test.md`.

## Three negative tests

### 1. One-off social copy

**Prompt:** “Write a LinkedIn post about our new feature.”

**Expected behavior:** Do not activate the full workshop. Handle or route the isolated copywriting request normally.

**Why not:** The user did not ask for foundational messaging, positioning, or a source of truth.

### 2. Legal advice

**Prompt:** “Give me legal advice about this contract.”

**Expected behavior:** Do not activate the workshop because the fictional example concerns lawyers. Follow the normal legal-guidance boundary instead.

**Why not:** The request is legal analysis, not B2B messaging.

### 3. Linear integration

**Prompt:** “Help me build a Linear integration and issue tracker.”

**Expected behavior:** Do not activate the workshop or mention the fictional example.

**Why not:** The internal product analogy is not a trigger and never appears in public workshop content.

## Behavioral acceptance checklist

- Every step shows the current template guidance and original prompt when present.
- Guidance, question, example, and draft are visually distinct.
- The workshop asks no more than three initial questions and one follow-up at a time.
- A vague answer receives a focused follow-up rather than a polished invention.
- Help mode simplifies the question without supplying company facts.
- `See an example` neither advances progress nor updates the ledger.
- Example content never appears in a pause checkpoint or final output.
- Required skips remain open gaps; optional skips are explicitly omitted.
- A revision does not overwrite approved text before approval.
- Pause/resume restores the exact phase, step, statuses, and provenance.
- Phase 2 introduces no new audience, comparator, capability, outcome, or proof.
- Phase 3 routes each failure to the defined source section and reruns repaired checks.
- Final Markdown follows the canonical template order and retains its guidance callouts.
- The master Notion page ID is never passed to an update operation.
- No invented customer, metric, testimonial, quote, legal claim, or ExampleCo detail appears in user output.
