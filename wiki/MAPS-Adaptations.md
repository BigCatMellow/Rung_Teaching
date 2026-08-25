# MAPS Adaptations

Rung Teaching did not copy MAPS_Lean's software-agent workflow literally. It translated several of MAPS's **control ideas** into teaching rules.

The common problem is similar:

> How do you prevent a capable helper from producing a superficially successful result while bypassing the reasoning, evidence, boundaries, and verification that make the process trustworthy?

For MAPS, the helper is often an AI agent. For Rung, the helper is the teacher.

## Translation table

| MAPS_Lean concept | Rung Teaching translation |
| --- | --- |
| Look at reality first | Baseline the learner before teaching |
| Definition of DONE | Define observable independent mastery |
| Acceptance criteria | State what successful performance must demonstrate |
| Verification / evidence | Require demonstrations, not confidence |
| VERIFIED / REPORTED / ASSUMED / UNKNOWN | Track what the learner has actually demonstrated |
| Smallest sufficient method | Use the minimum-help ladder |
| Stop / escalation conditions | Know when to explain, research, narrow, or stop |
| Repair and learning | Turn repeated errors into durable countermeasures |
| Emergence | Capture discoveries without letting them hijack the lesson |
| Program steering | Check whether practice attacks the real bottleneck |
| Simulation design | Use realistic cold-start transfer tests |
| Information lifecycle | Keep active principles compact and retire stale rules |
| Stop after acceptance passes | Do not manufacture practice after the target mastery proof passes |

## 1. Look at reality first

MAPS's project bootstrap begins by inspecting actual products, data, constraints, prior attempts, and other direct evidence before constructing a plan.

Source: [`PROJECT_BOOTSTRAP.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/PROJECT_BOOTSTRAP.md)

### Rung translation

Do not build instruction around what the learner says they know or what the teacher assumes they know.

Start with a **cold baseline** and observe current performance.

---

## 2. Define DONE

MAPS requires a concrete, observable definition of project completion.

Source: [`PROJECT_BOOTSTRAP.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/PROJECT_BOOTSTRAP.md)

### Rung translation

"Understand the topic" is not enough.

Define what the learner should be able to recognize, decide, execute, explain, check, and transfer without teacher support.

The project may finish before the skill is learned. Rung therefore keeps **project completion** separate from **learning completion**.

---

## 3. Evidence status

MAPS distinguishes information that is:

- `VERIFIED`;
- `REPORTED`;
- `ASSUMED`;
- `UNKNOWN`.

Source: [`AGI_STANDARD.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/AGI_STANDARD.md)

### Rung translation

A learner saying "I know this" is **REPORTED** until the relevant skill has been demonstrated.

Likewise, in factual domains, a persuasive argument should not silently transform an unverified premise into a fact.

---

## 4. Acceptance criteria and proof

MAPS treats success as something that should be observable and verifiable rather than "looks good" or "should work."

Sources:

- [`AGI_STANDARD.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/AGI_STANDARD.md)
- [`TASK_LIFECYCLE.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/TASK_LIFECYCLE.md)

### Rung translation

A teacher should not certify learning because:

- the learner sounds confident;
- the learner follows the teacher's explanation;
- the guided example is now correct;
- the learner says the concept "makes sense."

Use observable mastery tests instead. See [Mastery and Transfer](Mastery-and-Transfer).

---

## 5. Stop and escalation conditions

MAPS instructions define when an agent must stop, research, re-plan, or escalate instead of guessing across a material boundary.

Source: [`AGI_STANDARD.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/AGI_STANDARD.md)

### Rung translation

The teacher should also know when **not** to keep questioning.

Escalate support when:

- required prerequisite knowledge is missing;
- struggle has become random rather than diagnostic;
- safety makes trial-and-error inappropriate;
- factual uncertainty requires research;
- the exercise is no longer testing the intended skill.

This became the [Assistance Ladder](Assistance-Ladder).

---

## 6. Repair and learning

MAPS distinguishes a one-off repair from a recurring failure that deserves a durable countermeasure.

Source: [`REPAIR_AND_LEARNING.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/REPAIR_AND_LEARNING.md)

### Rung translation

When a learner repeats the same underlying mistake, do not merely explain it again.

Create something reusable:

- diagnostic question;
- standing principle;
- checklist item;
- deliberate-practice drill;
- mandatory self-check.

Then test whether the countermeasure catches the failure that motivated it.

---

## 7. Emergence without scope drift

MAPS captures useful discoveries but does not let them silently expand the current task.

Source: [`EMERGENCE.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/EMERGENCE.md)

MAPS summarizes the flow as:

```text
observe → connect → synthesize → name → test → promote
```

### Rung translation

Interesting tangents should be captured in **Later / Emerging Questions** unless they are necessary to the current learning target.

A possible new teaching principle should similarly be tested before promotion.

---

## 8. Program steering

MAPS distinguishes "is this task well specified?" from "is this even the right task to spend effort on?"

Source: [`PROGRAM_STEERING.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/PROGRAM_STEERING.md)

### Rung translation

A well-designed exercise can still be the wrong exercise.

Ask periodically:

> Is this exercise attacking the learner's current bottleneck, or are we practicing what is comfortable because it is easy to teach and easy to complete?

---

## 9. Simulation design

MAPS uses realistic scenarios with controlled traps to test whether an agent can navigate the actual workflow rather than merely emit a plausible answer.

Source: [`SIMULATION_DESIGN.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/SIMULATION_DESIGN.md)

### Rung translation

Final mastery tests should resemble future reality:

- realistic starting information;
- no announcement of which lesson applies;
- fresh examples;
- plausible distractors or failure traps when appropriate;
- normal tools and references.

This is Rung's **cold-start transfer test**.

---

## 10. Information lifecycle

MAPS keeps current truth easy to find while retaining superseded history when useful.

Source: [`INFORMATION_LIFECYCLE.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/INFORMATION_LIFECYCLE.md)

### Rung translation

Standing principles should have an active lifecycle:

```text
candidate
→ tested
→ active
→ revised / narrowed / retired
```

Do not let the teaching system become an ever-growing pile of old advice.

---

## 11. Stop after success

MAPS explicitly warns against manufacturing extra work after the acceptance criteria, verification, and required review are complete.

Source: [`AGENTS.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/AGENTS.md)

### Rung translation

Do not keep drilling a mastered target simply because more exercises can be generated.

Move to the next meaningful weakness or stop the learning arc.

## What MAPS does *not* prove

These adaptations are **design translations**, not educational research findings.

MAPS provides disciplined ideas about evidence, boundaries, verification, repair, and continuation. Rung applies those ideas to teaching because they solve analogous process failures.

Claims about how people learn are grounded separately in [Research Foundations](Research-Foundations) and [Sources](Sources).