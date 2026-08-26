# Reviewer tests

Run these tests in a fresh conversation with the B2B Messaging Workshop enabled. Fixture files are inside the uploaded plugin under `tests/fixtures/`.

## Positive tests

### 1. Start from scratch

**Prompt:** `Walk me through building a B2B messaging framework for my SaaS from scratch.`

**Expected:** The workshop introduces its four phases, shows Phase 0 guidance, and asks no more than three focused questions. It does not dump the full questionnaire.

### 2. Use research without inventing evidence

Attach `tests/fixtures/interview-notes.md`, then prompt: `Turn these interview notes into a Product Marketing source of truth, and guide me through the gaps.`

**Expected:** It extracts supported facts and sourced quotes, labels inferences and gaps, and begins at the earliest incomplete section. It invents no quote, metric, or proof point.

### 3. Show a fictional example safely

Start a workshop, reach Industry problems, then reply: `example`

**Expected:** It labels the example fictional and illustrative, shows only that section's example, preserves progress, and repeats the unanswered question without saving the example as the user's answer.

### 4. Resume from a checkpoint

Attach `tests/fixtures/resume-checkpoint.md`, then prompt: `Resume my messaging workshop from this checkpoint.`

**Expected:** It summarizes approved answers, hypotheses, and gaps, preserves approved fields, and resumes at Phase 1, Competitive alternatives.

### 5. Pressure-test an existing framework

Attach `tests/fixtures/framework-needing-pressure-test.md`, then prompt: `Pressure-test this B2B messaging framework and help me repair what fails.`

**Expected:** It runs all six checks, identifies generic differentiation and unsupported proof, reports Pass/Fail/Unresolved, and routes the first repair to its source section.

## Negative tests

### 1. One-off social copy

**Prompt:** `Write a LinkedIn post about our new feature.`

**Expected:** The plugin does not activate the full messaging workshop.

### 2. Legal advice

**Prompt:** `Give me legal advice about this contract.`

**Expected:** The plugin does not activate the workshop merely because its fictional example involves legal software.

### 3. Software integration

**Prompt:** `Help me build a Linear integration and issue tracker.`

**Expected:** The plugin does not activate the workshop or expose its internal fictional example.
