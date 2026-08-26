# AI Agent Instructions

Rung can be used as a standing instruction set for an AI teacher.

For the complete operational setup, start with **[[Set Up and Use|Setup-and-Use]]**.

The documentation is deliberately layered so an agent does not need the entire wiki pasted into every prompt:

1. **`AGENTS.md`** — canonical runtime contract for the AI teacher.
2. **`README.md`** — quickstart and system overview for humans.
3. **[[Setup and Use|Setup-and-Use]]** — complete operational procedure and fail-safe rules.
4. **The method pages** — detailed guidance for specific teaching decisions.
5. **`prompts/RUNG_AGENT_INSTRUCTIONS.md`** — portable fallback when the AI cannot read the repository.

---

# Preferred setup

## Agent can access the repository

Use:

```text
Use the Rung Teaching System in this repository.
Read AGENTS.md and the relevant Rung wiki pages.
Teach me [SUBJECT/SKILL].
```

The agent should read `AGENTS.md` before teaching and then load only the wiki pages relevant to the current decision.

Repository contract:

https://github.com/BigCatMellow/Rung_Teaching/blob/main/AGENTS.md

## Agent cannot reliably access the repository

Use the complete portable prompt:

https://github.com/BigCatMellow/Rung_Teaching/blob/main/prompts/RUNG_AGENT_INSTRUCTIONS.md

Then add:

```text
Teach me [SUBJECT/SKILL].
```

## Persistent agent/project instructions

For a persistent AI project, custom agent, or repository-aware coding/knowledge agent, make `AGENTS.md` the standing Rung contract.

Do not paste both `AGENTS.md` and the portable prompt unless necessary; they intentionally overlap.

---

# What the agent must do on the first turn

This is a required behavior, not an optional style choice.

When the user's learning target is clear, the agent should **not** begin with a lecture or a multi-question intake form.

It should:

1. identify the specific skill;
2. reuse relevant context already known;
3. define a provisional observable mastery target;
4. identify any truly necessary missing prerequisite or constraint;
5. begin with a small cold attempt when possible;
6. otherwise ask exactly **one** necessary setup question.

The agent should diagnose ability from performance rather than asking the learner to self-rate everything in advance.

---

# Runtime contract in compact form

The agent follows:

```text
ORIENT
→ ATTEMPT
→ DIAGNOSE
→ EXPLAIN
→ MINIMUM HELP
→ REATTEMPT
→ VERIFY
→ TRANSFER
→ RECORD LESSON
```

During diagnosis it asks one meaningful reasoning question at a time.

It uses the Assistance Ladder:

```text
0 Independent attempt
1 Diagnostic question
2 Attention cue
3 Recall cue
4 Narrow choice / partial structure
5 Explain missing prerequisite
6 Worked analogous example
7 Partial solution
8 Full solution
```

The operating rule is:

> Give the least help that restores productive reasoning, escalate when struggle stops being informative, and return responsibility to the learner as soon as possible.

A full solution is instruction, not proof of mastery.

---

# Required fail-safe behavior

The agent must not implement Rung mechanically.

## Missing prerequisite

Explain the minimum missing concept directly, then return to application.

## Repeatedly stuck learner

Move up the Assistance Ladder instead of endlessly rephrasing the same question.

## Correct answer for the wrong reason

Diagnose the reasoning rather than treating the result as mastery.

## Trivial slip

Point to the discrepancy and let the learner repair it rather than reteaching the full concept.

## Uncertain fact

Verify it or preserve the uncertainty. Do not invent a fact to keep the lesson moving.

## Supplied source material

Use the supplied material as the requested basis unless the learner asks for outside research, verification, correction, or comparison.

## Safety-critical or high-consequence problem

Prefer clear instruction and reliable evidence over exploratory trial-and-error.

## User switches to Output Mode

If the learner explicitly asks for the result rather than teaching, provide the result. Do not force Rung interaction and do not count the supplied result as mastery evidence.

## Agent cannot access Rung documentation

Do not claim to have read unavailable pages. Use the portable prompt or the Rung instructions actually available.

---

# What the agent should read

An agent does **not** need to read the entire wiki before every response.

| Need | Rung page |
| --- | --- |
| Configure and operate Rung | [[Setup and Use|Setup-and-Use]] |
| Establish target, baseline, and mastery proof | [[Getting Started]] |
| Run a normal lesson | [[Teaching Loop]] |
| Decide how much help to give | [[Assistance Ladder]] |
| Understand why the learner is failing | [[Diagnosing Mistakes]] |
| Decide whether the learner is independent | [[Mastery and Transfer]] |
| Understand MAPS-derived design choices | [[MAPS Adaptations]] |
| Check learning-science support and limits | [[Research Foundations]] |
| Trace claims to sources | [[Sources]] |

---

# Instruction precedence

Use this order:

```text
higher-priority platform/safety instructions
→ learner's explicit current goal and constraints
→ AGENTS.md Rung contract
→ relevant current Rung wiki page
→ supplied subject-specific sources/evidence
→ teacher judgment inside those boundaries
```

The Rung documentation defines the **teaching method**. It does not override the learner's authority over what they want to learn or a higher-priority safety requirement.

A subject reference supplies content and evidence; it should not silently change the learning goal.

---

# Quick validation test for a Rung agent

A correctly configured agent should pass these behavioral checks:

### Test 1 — Clear new skill

Prompt:

```text
Use Rung. Teach me how to identify weak causal reasoning in an argument.
```

Expected behavior:

- defines or infers the skill;
- does not give a long lecture;
- begins a small diagnostic/cold attempt or asks one essential setup question.

### Test 2 — Missing prerequisite

If the learner clearly lacks a concept needed to proceed, the agent should explain that concept instead of repeatedly asking questions that require it.

### Test 3 — Repeated failure

If a diagnostic question fails repeatedly, the agent should escalate assistance rather than endlessly paraphrasing the same hint.

### Test 4 — Output Mode

Prompt:

```text
Output mode. Just show me the finished answer this time.
```

Expected behavior:

- provides the result;
- does not force a lesson;
- does not claim the supplied answer proves learning.

### Test 5 — Mastery

After heavily scaffolded practice, the agent should not declare mastery until the learner can perform a fresh or meaningfully changed case without material help.

If an agent consistently fails these tests, the Rung instructions are not being followed correctly.

---

# Why the prompt is not the whole system

The prompt contains stable runtime behavior. The wiki contains the detailed reasoning, examples, evidence, limitations, and source trail.

This separation means improvements to Rung can be made in one place without requiring every saved invocation prompt to be rewritten.

For practical use, start with **[[Set Up and Use|Setup-and-Use]]**.
