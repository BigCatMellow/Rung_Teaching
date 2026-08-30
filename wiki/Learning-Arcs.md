# Learning Arcs

A **learning arc** is Rung's long-horizon control layer for a goal that spans multiple dependent skills, sessions, or mastery checks.

It does **not** replace the normal Rung loop. The loop teaches the current skill. The learning arc keeps the larger path pointed at independent competence.

Use a learning arc when the learner is trying to become capable across a meaningful body of work, for example:

- learn Python well enough to build small programs independently;
- become better at scene construction across a writing project;
- learn to evaluate historical claims reliably;
- develop a durable debugging method across several kinds of failures.

Skip formal arc machinery for a small, local lesson.

---

## The two levels

```text
LEARNING ARC
  goal → capability map → current phase → trajectory checks → final proof
                              │
                              ▼
                         CURRENT SKILL
                              │
                              ▼
                          RUNG LOOP
  attempt → diagnose → minimum help → reattempt → verify → transfer
```

The distinction matters:

- **Skill steering:** Is this exercise attacking the learner's current bottleneck?
- **Arc steering:** Given what we have learned about the learner, is the larger roadmap still the right route to the final goal?

A good exercise can be the wrong next exercise. A good local lesson can also reveal that the original learning roadmap was based on a bad assumption.

---

# Learning Arc Bootstrap

For a durable learning goal, use:

```text
inspect reality
→ define independent DONE
→ map required capabilities backward
→ challenge the map once
→ choose the first useful skill
→ execute forward with Rung
→ adapt from evidence
```

This is adapted from MAPS_Lean's project-bootstrap discipline, translated into teaching. It is a Rung design rule, not a claim that educational research validates this exact sequence.

MAPS source: [`PROJECT_BOOTSTRAP.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/PROJECT_BOOTSTRAP.md)

## 1. Inspect reality

Use actual performance before constructing a detailed curriculum.

Inspect what is available:

- a cold attempt;
- the learner's existing work;
- prior mastery evidence;
- known prerequisite gaps;
- tools or references the learner will realistically use;
- constraints that materially change the goal.

Self-report can help orient the teacher, but it is not a substitute for demonstrated performance.

## 2. Define independent DONE

Write the destination as observable performance.

Weak:

> Learn Python.

Better:

> Given a small unfamiliar programming problem, independently decompose it, implement a working Python solution using normal references, debug important failures, explain the main design choices, and verify the result.

The final proof should resemble future reality rather than a familiar classroom exercise.

## 3. Map required capabilities backward

Ask what must be true immediately before the learner can pass the final proof, then what those capabilities depend on.

Example:

```text
independent small program
        ↑
program decomposition + debugging + organization
        ↑
functions + data structures + control flow
        ↑
basic expressions and data
```

This is a **provisional capability map**, not a rigid syllabus.

Keep distant portions broad. Detail the current phase and next useful skill only as far as current evidence supports.

## 4. Challenge the map once

Before treating the map as the plan, ask:

- Are we assuming a weakness the learner has not demonstrated?
- Are we teaching a prerequisite that may already be strong?
- Is an important prerequisite missing?
- Does the final proof actually represent the learner's real goal?
- Are we overplanning distant work that current evidence could change?
- Is the order based on dependency, or merely on a familiar textbook sequence?

For a consequential arc, deliberately test the weakest assumption with evidence, a cold task, or an alternative ordering.

## 5. Choose the first useful skill

The next skill should be the smallest meaningful bottleneck whose improvement moves the learner toward the final proof.

Then use the normal Rung Teaching Loop.

## 6. Adapt from evidence

The roadmap is allowed to change when learner evidence changes the picture.

Do not keep teaching the original sequence merely because it was written down first.

---

# Minimal arc state

For a multi-session arc, keep one canonical current view:

```text
ARC GOAL:
FINAL INDEPENDENT PROOF:
CURRENT PHASE:
CURRENT SKILL:
CURRENT STATUS:

CAPABILITY MAP / ROADMAP:
- [status] capability — evidence or next proof

VERIFIED STRENGTHS:
ACTIVE WEAKNESSES:
PREREQUISITE BLOCKERS:
MASTERY EVIDENCE:
ACTIVE REGRESSION CASES:
NEXT EXERCISE:
USEFUL BUT LATER:
```

Do not create a new mutable progress summary every session. Update the canonical current state; old sessions are evidence/history, not competing present truth.

The state may be informal in a conversation or durable in a handoff. The structure exists to preserve decision-relevant learning information, not to create paperwork.

---

# Learning Trajectory Check

Run a trajectory check at **natural arc boundaries**, not after every exercise.

Useful triggers:

- completion of a meaningful skill or phase;
- repeated prerequisite gaps changing several planned items;
- evidence that a supposedly weak capability is already strong;
- repeated success or failure that changes the likely bottleneck;
- a plateau despite locally successful exercises;
- most remaining roadmap items becoming conditional, irrelevant, or blocked;
- the learner's real goal materially changing.

Use:

```text
1. Re-check current evidence.
2. Name what changed.
3. Compare the roadmap with the final proof.
4. Choose a trajectory action.
5. Update the canonical arc state.
6. Continue with the next useful skill.
```

Possible actions:

- **CONTINUE** — roadmap still fits the evidence.
- **REPRIORITIZE** — same goal, different order.
- **INSERT PREREQUISITE** — a newly demonstrated dependency blocks useful practice.
- **CUT** — planned work is unnecessary for the defined goal.
- **RESEARCH** — factual or domain uncertainty prevents a sound teaching decision.
- **REDESIGN PRACTICE** — the target is right but current exercises are not exposing the skill.
- **TEST MASTERY** — evidence suggests the learner may already be independent.
- **STOP** — the final proof has passed or the arc is no longer relevant.

If the learner changes the objective itself, re-orient the arc and redefine the final proof rather than silently treating the old roadmap as authority.

This is adapted from MAPS_Lean's separation between task-level steering and roadmap-level trajectory checks.

MAPS source: [`ROADMAP_TRAJECTORY_CHECK.md`](https://github.com/BigCatMellow/MAPS_Lean/blob/main/playbook/ROADMAP_TRAJECTORY_CHECK.md)

---

# Relationship to mastery evidence

A roadmap status is only as trustworthy as the evidence behind it.

Do not mark a capability `INDEPENDENT` because:

- the learner says it feels easy;
- a guided exercise succeeded;
- the teacher supplied the decisive reasoning;
- a familiar example was repeated correctly.

Use the evidence record defined in [Mastery and Transfer](Mastery-and-Transfer). A consequential status should point to the fresh case that justified it.

---

# Relationship to regression cases

A repeated meaningful failure can become an active **mistake regression case**. The purpose is to see whether the learner later recognizes and prevents the pattern without the teacher announcing which lesson applies.

Regression cases are owned by [Diagnosing Mistakes](Diagnosing-Mistakes). The learning arc only carries the active cases that may affect future exercises or mastery claims.

---

# Anti-ceremony rules

A learning arc has failed as a control system if it creates more administration than learning.

- Do not formalize a one-off lesson.
- Do not require every field when it changes no teaching decision.
- Do not turn the capability map into a fixed curriculum that evidence cannot change.
- Do not create separate status trackers for each session.
- Do not preserve every mistake; preserve recurring or consequential patterns.
- Do not keep drilling work whose agreed mastery proof has already passed.

The smallest sufficient state is the correct state.