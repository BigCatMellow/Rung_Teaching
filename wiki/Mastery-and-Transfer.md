# Mastery and Transfer

The most important verification rule in Rung is:

> **Assisted success is not mastery.**

A learner can reach the correct answer while relying on prompts, hints, examples, or the teacher's framing. That proves the interaction produced an answer. It does not yet prove the learner can reproduce the reasoning independently.

## Why the practiced example is not enough

Instruction changes the environment around the problem. The learner may know which concept is being tested, which diagnostic question the teacher expects, what kind of answer was just corrected, or which worked example the task resembles.

Those cues can disappear in real use. Final verification should therefore use a fresh case with substantially less scaffolding.

---

# The mastery tests

Use the dimensions that fit the skill.

## 1. Recognition

Can the learner identify when the principle applies without being told which lesson is relevant?

## 2. Execution

Can the learner perform the skill without step-by-step prompting, using the normal tools or references they would have in real life?

## 3. Explanation

Can the learner explain why the method applies, why it works, which evidence matters, and why a plausible alternative is weaker?

## 4. Error detection

Can the learner catch an important mistake in their own work or diagnose a plausible wrong approach?

## 5. Transfer

Can the learner apply the principle when the surface form changes enough that copying the practiced procedure is insufficient?

Possible variations include a different context, reordered information, distracting details, a competing plausible method, or incomplete information.

## 6. Delayed retrieval

When durable memory matters, can the learner still retrieve and use the relevant principle or diagnostic after time has passed without rereading the prior lesson first?

Retrieval-practice research supports the broader value of retrieving information for later retention in many settings. See [Research Foundations](Research-Foundations).

---

# Cold-start mastery simulation

For consequential or complex skills, give the learner:

1. only information they would realistically possess;
2. a fresh problem;
3. no explicit label telling them which lesson applies;
4. a plausible trap when useful;
5. normal tools and references.

Observe:

```text
recognition
→ method selection
→ execution
→ self-check
→ explanation
```

Do not make transfer so different that it silently tests an unrelated prerequisite rather than the intended skill.

---

# Mastery Evidence Record

For a meaningful skill in a longer learning arc, preserve the evidence behind the status rather than only the status label.

Use the smallest useful record:

```text
SKILL:
STATUS: NEEDS_BASELINE | GUIDED | PRACTICING | TRANSFER_TEST | INDEPENDENT
CASE / TASK:
ASSISTANCE USED: highest material Assistance Ladder level

RECOGNITION: PASS | FAIL | NOT TESTED
EXECUTION: PASS | FAIL | NOT TESTED
EXPLANATION: PASS | FAIL | NOT TESTED
ERROR DETECTION: PASS | FAIL | NOT TESTED
TRANSFER: PASS | FAIL | NOT TESTED
DELAYED RETRIEVAL: PASS | FAIL | NOT TESTED

VERDICT:
LIMITATIONS / NEXT PROOF:
```

Not every small lesson needs a formal record. Use it when future teaching decisions will rely on a mastery claim.

## Evidence rules

- A guided success is **practice evidence**, not independent mastery evidence.
- Record material assistance. If the teacher supplied the decisive reasoning, the case cannot prove independence.
- A correct answer for the wrong reason does not pass the relevant reasoning criterion.
- A failed dimension narrows the next teaching target; it does not automatically reset the whole skill.
- A status such as `INDEPENDENT` should point to the fresh case that justified it.
- `NOT TESTED` is preferable to pretending evidence exists.
- Later contradictory evidence can reopen a previously passed skill.

This adapts MAPS_Lean's rule that consequential status claims should be backed by inspectable evidence rather than unsupported summaries. It is a Rung system design choice, not a claim that this exact record format is validated by learning research.

---

# Suggested status model

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

Use states only when they make a longer learning arc clearer. They are not required for a small lesson.

---

# After a failed mastery test

Do not reset the learner to the beginning automatically.

Diagnose whether the failure is primarily recognition, execution, explanation, monitoring, transfer, forgotten prerequisite, or a badly designed test. Return to the lowest Assistance Ladder rung that addresses the observed weakness, then use a different case for the next mastery test.

---

# When to stop

Stop a learning arc when the defined proof passes at the level of independence required by the learner's real goal.

Do not manufacture more exercises simply because teaching can continue indefinitely.

Mastery is relative to the target. Someone can be independent at one level while still having much more to learn in the broader field.