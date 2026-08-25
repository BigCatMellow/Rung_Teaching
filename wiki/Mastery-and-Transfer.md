# Mastery and Transfer

The most important verification rule in Rung is:

> **Assisted success is not mastery.**

A learner can reach the correct answer while relying on prompts, hints, examples, or the teacher's framing. That proves the teaching interaction succeeded at producing an answer. It does not yet prove the learner can reproduce the reasoning independently.

## Why the practiced example is not enough

Instruction changes the environment around the problem.

The learner may know:

- which concept is being tested;
- which diagnostic question the teacher expects;
- what kind of answer was recently praised or corrected;
- which worked example the current problem resembles.

Those cues can disappear in real use.

Therefore, final verification should use a fresh case with substantially less scaffolding.

## The mastery tests

### Test 1 — Recognition

Can the learner identify when the principle applies?

The teacher should not announce the relevant lesson beforehand.

**Pass example:** the learner notices that a scene's problem is missing agency and invokes the agency test on their own.

**Fail example:** the learner can answer the agency question correctly only after the teacher asks it.

---

### Test 2 — Execution

Can the learner perform the skill without step-by-step prompting?

Execution may include using normal tools or references that would exist in real life. Independence does not mean memorizing everything; it means not depending on the teacher to supply the important reasoning.

---

### Test 3 — Explanation

Can the learner explain:

- why the method applies;
- why it works;
- which evidence matters;
- why a plausible alternative is weaker?

Self-explanation research supports asking learners to articulate relationships rather than merely reproduce a procedure. See [Research Foundations](Research-Foundations).

---

### Test 4 — Error detection

Can the learner catch an important mistake?

This can be tested by:

- placing a plausible error in an example;
- asking the learner to critique their own result;
- asking what evidence would falsify the answer;
- asking for a test or check before accepting the work.

This measures whether the learner has acquired the **checking habit**, not merely the production habit.

---

### Test 5 — Transfer

Can the learner apply the principle when the surface form changes?

Change enough that copying the practiced procedure mechanically is insufficient.

Possible variations:

- different context;
- reordered information;
- distracting details;
- a different apparent problem type;
- a competing method that looks plausible;
- incomplete information requiring the learner to identify what is missing.

The learner should identify the underlying structure rather than the familiar appearance.

---

### Test 6 — Delayed retrieval

For knowledge that must remain available over time, test it after a delay.

Do not begin by showing the previous notes.

Ask the learner to retrieve:

- the principle;
- the diagnostic question;
- the method-selection clue;
- the important failure modes.

Retrieval-practice research shows that retrieving information can improve later retention more than additional passive study in many experimental settings. See Roediger & Karpicke (2006) on [Research Foundations](Research-Foundations).

## Cold-start simulation

For consequential or complex skills, design a final exercise that resembles future reality.

Give the learner:

1. only the information they would realistically possess;
2. a new problem;
3. no explicit label telling them which lesson applies;
4. at least one plausible trap when useful;
5. normal tools or references they would actually have access to.

Then observe:

```text
recognition
→ method selection
→ execution
→ self-check
→ explanation
```

MAPS uses controlled simulations to test whether an agent can navigate a workflow from realistic starting material rather than merely produce a plausible answer. Rung adapts that idea to learner independence. See [`SIMULATION_DESIGN.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/SIMULATION_DESIGN.md).

## Suggested status model

For larger learning projects:

```text
NEEDS_BASELINE
→ GUIDED
→ PRACTICING
→ TRANSFER_TEST
→ INDEPENDENT
```

Possible side state:

```text
BLOCKED_ON_PREREQUISITE
```

### NEEDS_BASELINE

Current ability has not been demonstrated.

### GUIDED

The learner still needs substantial cues, explanation, or worked examples.

### PRACTICING

The learner succeeds with light prompting and is beginning to self-correct.

### TRANSFER_TEST

The practiced form works; now reduce scaffolding and vary the problem.

### INDEPENDENT

The defined mastery proof passes without material teacher help.

### BLOCKED_ON_PREREQUISITE

A missing concept prevents meaningful practice of the current target.

Use these states only when they make a longer learning arc clearer. They are not required for a small lesson.

## When to stop

Do not manufacture more exercises simply because teaching can continue indefinitely.

Stop a learning arc when the defined proof passes at the level of independence required by the learner's real goal.

This adapts a MAPS negative operating rule: stop when acceptance criteria and required verification are complete rather than creating extra work after success. See [`AGENTS.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/AGENTS.md).

Mastery is always relative to the target. Someone can be independent at one level while still having much more to learn in the broader field.