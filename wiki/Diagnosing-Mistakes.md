# Diagnosing Mistakes

Rung treats **detection** and **correction** as separate steps.

A weak teaching response is:

```text
wrong answer
→ teacher supplies correct answer
```

Rung prefers:

```text
detect
→ classify
→ identify cause
→ choose intervention
→ learner repairs
→ verify
```

The same visible error can come from different causes. A learner who forgot a fact needs a different response from a learner who understands the facts but chooses a poor strategy.

## Error classes

### A. Slip

The learner knows the principle but executed it incorrectly.

Examples include arithmetic errors, typos, omitted steps they can immediately explain, and misread values.

**Teaching response:** point to the discrepancy and let the learner repair it. Do not reteach the entire concept unless evidence shows the concept itself is weak.

### B. Missing fact or prerequisite

The learner cannot reason because necessary information or a prerequisite concept is absent.

**Teaching response:** supply or teach the missing prerequisite, then return to the task. Do not repeatedly ask questions whose answers require knowledge the learner has never acquired.

### C. Misconception

The learner has an incorrect mental model, not merely a missing fact.

**Teaching response:** surface the model, test it against evidence or a counterexample, identify what it fails to explain, rebuild it, then apply the revised model to a new case.

### D. Strategy error

The learner knows relevant concepts but selects the wrong method.

**Teaching response:** ask which feature of the problem should determine method selection.

> What clue should tell you which tool belongs here?

The goal is method selection, not only method execution.

### E. Judgment error

The problem requires weighting competing considerations rather than applying a mechanical rule.

**Teaching response:** make the criteria explicit and compare consequences.

Useful questions include:

- What are the competing criteria?
- Which one matters most here, and why?
- What would your choice cost?
- What evidence would change the weighting?

### F. Monitoring error

The learner produces a weak or incorrect result **and believes it is strong**.

**Teaching response:** require an observable verification step such as a constraint check, prediction, counterexample, opposing interpretation, or diagnostic checklist.

A mature learner does not merely produce work. They also know how to distrust and test their own first answer.

### G. Transfer failure

The learner succeeds on the practiced form but fails when surface details change.

**Teaching response:** vary the context while preserving the underlying principle, then ask the learner to identify what remains invariant.

This is why Rung separates practice success from mastery. See [Mastery and Transfer](Mastery-and-Transfer).

### H. Repeated failure

The same underlying mistake returns after prior correction.

Do not simply repeat the old explanation.

Ask:

> What pattern connects this mistake to the earlier one?

Then create a durable countermeasure when the pattern is real.

Possible countermeasures include a diagnostic question, checklist item, standing principle, comparison example, short deliberate-practice drill, or mandatory self-check.

This is adapted from MAPS's repair rule: repeated failures should lead to a durable countermeasure rather than an endless sequence of one-off repairs. See [`REPAIR_AND_LEARNING.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/REPAIR_AND_LEARNING.md).

---

# The callback rule

When a mistake repeats, explicitly connect it to the previous occurrence.

```text
I made another mistake
        ↓
I recognize this class of mistake
        ↓
I know the test that catches it
        ↓
I catch it before the teacher does
```

The goal is not permanent teacher recognition. It is learner self-recognition.

---

# Mistake ledger

For a long learning project, keep a compact record of meaningful patterns.

| Situation | Error type | Repeated? | Countermeasure | Status |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | [yes/no] | [ ] | [candidate/active/resolved] |

Do not record every trivial slip. The ledger is for mistakes that reveal something stable or consequential about how the learner approaches problems.

---

# Mistake Regression Bank

A durable countermeasure is stronger when it can be tested later against the kind of failure that motivated it.

When a mistake is repeated, sticky, or consequential enough to matter beyond the current exercise, freeze the **failure shape** as a regression case.

Use:

```text
meaningful failure
→ diagnose cause
→ correct and verify
→ confirm recurring/sticky pattern
→ record regression case
→ later cold reappearance
→ did the learner recognize and prevent it independently?
```

A regression case should record only what is necessary:

```text
PATTERN:
TRIGGER / RECOGNITION CLUE:
LIKELY CAUSE:
COUNTERMEASURE OR SELF-CHECK:
FRESH TEST SHAPE:
STATUS: CANDIDATE | ACTIVE | RESOLVED | RETIRED
LAST COLD RESULT:
```

## Regression-test rules

1. **Test the pattern, not the memorized example.** Change the surface form.
2. **Do not announce which prior lesson applies.** Recognition is part of the test.
3. **Use normal tools and references.** Independence does not require artificial memorization.
4. **Do not count a teacher cue as an independent catch.** Record the assistance used.
5. **Do not overfit one incident.** A one-off slip usually does not deserve a regression case.
6. **Retire stale cases.** If the pattern no longer represents a meaningful weakness, remove it from active teaching state while preserving useful history when needed.

Example:

```text
PATTERN: chooses an index-based loop when the task only needs each item
TRIGGER: reaches for positions instead of asking whether position matters
COUNTERMEASURE: "Do I need the index, or only the value?"
FRESH TEST SHAPE: unfamiliar collection-processing problem with no need for indexes
STATUS: ACTIVE
```

Weeks later, the teacher can include a changed collection problem without naming the old lesson. If the learner chooses the simpler iteration or catches the unnecessary index themselves, that is stronger evidence than successfully repeating the original exercise.

This extends Rung's existing MAPS repair adaptation with MAPS_Lean's practice of preserving important real failures as future regression checks. The exact teaching form is a Rung design choice, not a validated educational protocol.

---

# When a mistake becomes a principle

Do not generalize from one incident too quickly.

Use:

```text
OBSERVATION
→ POSSIBLE PATTERN
→ TEST ON ANOTHER CASE
→ REPEATED EVIDENCE
→ STANDING PRINCIPLE
```

This also reflects MAPS's emergence discipline: notice freely, but promote deliberately. See [`EMERGENCE.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/EMERGENCE.md).