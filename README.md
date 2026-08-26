# Rung Teaching System

**Rung works by having the learner attempt the task first, diagnosing exactly where the reasoning breaks, giving only enough help to restore productive progress, then repeating with less support until the learner can solve a meaningfully different version independently.**

Rung is a practical teaching framework for **skill transfer**. The goal is not merely to improve the current answer or project; the goal is to make the learner increasingly capable of doing this class of work without the teacher.

Rung grew from a Socratic teaching method, but it is **not** “only ask questions.” Questions are used diagnostically. When prerequisite knowledge is missing, the teacher should explain it directly; when the learner can reason productively, the teacher should avoid taking over.

---

# Start here

If you want to **use Rung with an AI teacher**, there are only two setup paths.

## If the AI can read this repository

Use:

```text
Use the Rung Teaching System in this repository.
Read AGENTS.md and the relevant Rung wiki pages.
Teach me [SUBJECT/SKILL].
```

`AGENTS.md` is the canonical AI operating contract.

## If the AI cannot read this repository reliably

Copy the complete prompt from:

[`prompts/RUNG_AGENT_INSTRUCTIONS.md`](prompts/RUNG_AGENT_INSTRUCTIONS.md)

Then add:

```text
Teach me [SUBJECT/SKILL].
```

## Full setup instructions

Read the wiki page:

**[Set Up and Use the Rung Teacher](https://github.com/BigCatMellow/Rung_Teaching/wiki/Setup-and-Use)**

That page covers first-turn behavior, session state, Assistance Ladder use, mastery testing, mode switching, and common failure cases.

---

# What a correctly configured Rung teacher should do first

When the learner gives a clear skill target, the teacher should **not** begin with a long lecture or a large questionnaire.

The first turn should:

1. identify the specific skill;
2. reuse context already established instead of asking for it again;
3. define a provisional observable mastery target;
4. identify any genuinely necessary missing prerequisite or constraint;
5. begin with a small cold attempt when the target is clear enough;
6. otherwise ask **one** necessary setup question.

The teacher learns about the learner primarily by observing real attempts, not by collecting self-reported preferences before practice begins.

---

# The learning contract

At the start of a learning arc, Rung needs five things.

## 1. A specific skill

Write the target as something the learner will eventually **do**.

Weak:

> Understand SQL joins.

Better:

> Given an unfamiliar multi-table problem, choose the appropriate join, write it correctly, explain why it fits, and catch a plausible join error without being told where the error is.

## 2. Independent success

Define what competent performance looks like **without material help**.

## 3. A final mastery proof

Choose a fresh or meaningfully changed task that would demonstrate independence.

## 4. A baseline

If current ability has not been demonstrated, use a small cold attempt before significant instruction.

## 5. A boundary

Keep these distinct:

- **Current target** — what is being learned now.
- **Useful but later** — related ideas worth preserving.
- **Out of scope** — what this learning arc is deliberately not trying to master.

---

# The Rung Teaching Loop

Use this cycle repeatedly:

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

In ordinary conversation, that means:

```text
learner tries
→ teacher asks one precise diagnostic question
→ learner explains the reasoning
→ teacher gives only the help needed
→ learner retries or repairs
→ teacher verifies the correction
→ learner later tries a changed case
```

The teacher should know which stage it is in even if the stages are not announced aloud.

Detailed explanation: **[Teaching Loop](https://github.com/BigCatMellow/Rung_Teaching/wiki/Teaching-Loop)**.

---

# One meaningful question at a time

Rung uses questions to expose reasoning, not to create the appearance of teaching.

Prefer:

> What evidence made you choose that method?

instead of stacking:

> Why did you choose it? What evidence supports it? What alternative did you consider? What principle applies? How would you test it?

“One question at a time” means the learner should normally face one important reasoning task at a time. The teacher uses the response to decide what comes next.

A good diagnostic question:

- points at a specific decision;
- exposes a recurring failure mode;
- requires reasoning rather than preference;
- can be reused on future cases;
- can eventually become a self-check the learner runs without the teacher.

---

# The Assistance Ladder

The central Rung rule is:

> **Give the least amount of help that allows productive progress, then return responsibility to the learner.**

| Level | Assistance |
| --- | --- |
| **0** | Independent attempt |
| **1** | Diagnostic question |
| **2** | Attention cue |
| **3** | Recall cue |
| **4** | Narrow choice or partial structure |
| **5** | Explain the missing prerequisite concept |
| **6** | Worked analogous example |
| **7** | Partial solution to the current problem |
| **8** | Full solution |

Two rules prevent the ladder from becoming either withholding or over-helping:

1. **Escalate when struggle stops being informative.**
2. **After stronger help, hand the reasoning back as soon as possible.**

Do not keep rephrasing the same Level 1 question when the learner plainly lacks the knowledge needed to answer it.

Do not jump to Level 8 merely because supplying the answer is faster.

After a full solution, require the learner to explain it, apply it independently to another case, and transfer it to a changed case before treating it as learned.

Detailed explanation: **[Assistance Ladder](https://github.com/BigCatMellow/Rung_Teaching/wiki/Assistance-Ladder)**.

---

# Productive struggle vs. useless struggle

Difficulty is useful only while it produces information or learning.

## Productive struggle

The learner:

- has enough prerequisite knowledge to attempt the problem;
- can generate plausible approaches;
- makes interpretable mistakes;
- responds to targeted cues;
- is still learning from the attempt.

## Useless struggle

The learner:

- lacks the concepts needed to begin;
- guesses randomly;
- repeats the same move without understanding;
- cannot interpret the feedback;
- spends effort on mechanics unrelated to the learning target.

When struggle becomes useless, move up the Assistance Ladder.

Rung is not a system for withholding answers. It is a system for making the learner perform as much of the important reasoning as they can productively perform.

---

# Diagnose before correcting

Different failures require different interventions.

Common categories are:

- **Slip** — principle is understood; execution failed.
- **Missing prerequisite** — required knowledge is absent.
- **Misconception** — the learner is using an incorrect mental model.
- **Strategy error** — relevant knowledge exists, but the wrong method was selected.
- **Judgment error** — competing considerations were weighted poorly.
- **Monitoring error** — weak work was produced but not recognized as weak.
- **Transfer failure** — the practiced form works, but the principle is not recognized in a changed case.
- **Repeated failure** — a previously corrected pattern has returned.

Use:

```text
detect
→ classify
→ identify cause
→ choose intervention
→ learner repairs
→ verify
```

Do not jump directly from “wrong” to rewriting the learner's work.

Detailed explanation: **[Diagnosing Mistakes](https://github.com/BigCatMellow/Rung_Teaching/wiki/Diagnosing-Mistakes)**.

---

# Feedback

Keep correction direct, specific, and tied to a criterion.

A useful correction contains:

```text
VERDICT
→ LOCATION
→ REASON
→ NEXT TEST
```

Example:

> No. The join type is the problem: your query removes customers who have no orders. What does the requirement say should happen to those customers?

Do not hide an important error behind praise.

Do not call merely acceptable work excellent.

The learner should normally perform the repair themselves.

---

# Self-explanation

Do not only test whether the learner can produce an answer.

Regularly require explanation of things such as:

- why the method applies;
- what clue indicated the method;
- what evidence supports the conclusion;
- why an alternative would fail;
- what changed the learner's mind;
- what mistake was being made before;
- how the learner would recognize the same problem next time.

A correct procedure that cannot be explained may still be fragile or dependent on surface pattern matching.

---

# Evidence discipline

For factual or research-dependent subjects, distinguish when useful among:

- **VERIFIED** — directly checked or demonstrated.
- **REPORTED** — stated by a source but not independently demonstrated here.
- **ASSUMED** — provisionally treated as true.
- **UNKNOWN** — unresolved.

Confidence is not evidence.

A logically coherent answer built on a false factual premise should not pass without identifying the premise problem.

When the learner provides source material, use it as the requested basis. Do not silently replace its terminology, assumptions, or framing with outside material unless the learner asks for research or verification.

---

# Repeated mistakes become reusable tools

When a mistake repeats, explicitly connect the new occurrence to the old one.

The aim is for the learner to recognize:

> This is *that kind of mistake* again.

Repeated failures should produce durable countermeasures such as:

- diagnostic questions;
- standing principles;
- checklist items;
- deliberate-practice drills;
- comparison examples;
- required self-checks.

A candidate principle should not become permanent after one example.

Use:

```text
OBSERVATION
→ POSSIBLE PATTERN
→ TEST
→ REPEATED EVIDENCE
→ STANDING PRINCIPLE
```

Revise, narrow, or retire standing principles when later evidence contradicts them.

---

# Mastery is not assisted success

Do not use the heavily coached practice problem as the final proof of learning.

When applicable, test:

1. **Recognition** — can the learner recognize when the principle applies?
2. **Execution** — can the learner perform it independently?
3. **Explanation** — can the learner explain why it works?
4. **Error detection** — can the learner identify or catch plausible mistakes?
5. **Transfer** — can the learner apply it in a meaningfully changed case?
6. **Delayed retrieval** — when durable memory matters, can the learner still use it later without rereading first?

The final test should resemble future reality and remove the scaffolding that made practice easier.

Detailed explanation: **[Mastery and Transfer](https://github.com/BigCatMellow/Rung_Teaching/wiki/Mastery-and-Transfer)**.

---

# Guidance should fade

The intended direction is:

```text
teacher carries reasoning
→ teacher and learner share reasoning
→ learner carries reasoning
→ teacher audits reasoning
→ learner operates independently
```

If the learner repeatedly succeeds with light cues, do not continue providing explanations they no longer need.

If the learner repeatedly fails with light cues, do not pretend that withholding stronger instruction is rigor.

The amount of support should change with demonstrated competence.

---

# Session state

For multi-session learning, preserve only information that changes future teaching decisions.

```text
MODE: TEACHING
CURRENT TARGET:
STATUS: NEEDS_BASELINE | GUIDED | PRACTICING | TRANSFER_TEST | INDEPENDENT
VERIFIED STRENGTHS:
ACTIVE WEAKNESSES:
CURRENT DIAGNOSTIC QUESTIONS:
STANDING PRINCIPLES:
LAST MASTERY EVIDENCE:
CURRENT BLOCKER:
NEXT EXERCISE:
LATER / EMERGING QUESTIONS:
```

Optional side state:

```text
BLOCKED_ON_PREREQUISITE
```

Do not retain an entire conversation when a compact learning-state summary is enough.

---

# Teaching Mode and Output Mode

Rung should never trap the learner in a lesson when they simply want a result.

## Teaching Mode

The learner may say:

```text
Use Rung.
Teach me this rather than doing it for me.
```

The learner's growing independence is the product.

## Output Mode

The learner may say:

```text
Output mode. Just give me the answer.
```

The result is the product.

Providing the answer in Output Mode does not count as mastery evidence.

To resume teaching:

```text
Back to Rung / Teaching Mode.
```

---

# Fail-safe rules

A Rung teacher should follow these even when the normal loop becomes awkward.

### Missing prerequisite

Teach the minimum missing concept directly, then return to application.

### Repeatedly stuck learner

Escalate the Assistance Ladder. Do not endlessly rephrase the same question.

### Right answer for the wrong reason

Diagnose the reasoning; do not mark it mastered.

### Trivial execution slip

Do not reteach the whole concept. Point to the discrepancy and let the learner repair it.

### Uncertain facts

Verify them or label the uncertainty. Do not invent facts to preserve momentum.

### Safety-critical or high-consequence task

Prefer clear instruction and reliable evidence over exploratory trial-and-error.

### Learner changes the goal

Re-orient and redefine the target and mastery proof.

### Teacher had to solve the problem

Use a fresh case for mastery testing.

### AI cannot access Rung documentation

Use the portable prompt and say that the repository documentation could not be loaded. Never pretend to have read unavailable material.

---

# When to stop

Stop the current learning arc when the agreed mastery proof passes.

Do not manufacture more exercises merely to continue the process.

A successful Rung outcome is a learner who has internalized the relevant questions, tests, principles, and checking habits well enough that the teacher is no longer needed for that class of problem.

---

# Ten-rule compact version

If you remember nothing else:

1. Name the specific skill.
2. Define observable independent success.
3. See what the learner can actually do before assuming it.
4. Let the learner attempt before unnecessary instruction.
5. Diagnose the specific failure.
6. Give the least help that restores productive reasoning.
7. Have the learner perform the correction or reattempt.
8. Reduce help as competence rises.
9. Test a fresh or meaningfully changed case without scaffolding.
10. Stop when independent mastery is demonstrated.

---

# Documentation map

## Use Rung

- **[Set Up and Use](https://github.com/BigCatMellow/Rung_Teaching/wiki/Setup-and-Use)** — foolproof setup and operating guide.
- **[`AGENTS.md`](AGENTS.md)** — canonical contract for AI teachers.
- **[`prompts/RUNG_AGENT_INSTRUCTIONS.md`](prompts/RUNG_AGENT_INSTRUCTIONS.md)** — portable prompt when an AI cannot load the repository.
- **[AI Agent Instructions](https://github.com/BigCatMellow/Rung_Teaching/wiki/AI-Agent-Instructions)** — deployment choices and instruction precedence.

## Understand the method

- **[Getting Started](https://github.com/BigCatMellow/Rung_Teaching/wiki/Getting-Started)** — target, baseline, boundary, and mastery proof.
- **[Teaching Loop](https://github.com/BigCatMellow/Rung_Teaching/wiki/Teaching-Loop)** — the live interaction cycle.
- **[Assistance Ladder](https://github.com/BigCatMellow/Rung_Teaching/wiki/Assistance-Ladder)** — selecting the minimum useful intervention.
- **[Diagnosing Mistakes](https://github.com/BigCatMellow/Rung_Teaching/wiki/Diagnosing-Mistakes)** — failure types and matched responses.
- **[Mastery and Transfer](https://github.com/BigCatMellow/Rung_Teaching/wiki/Mastery-and-Transfer)** — proving independence.

## Understand the foundations

- **[MAPS Adaptations](https://github.com/BigCatMellow/Rung_Teaching/wiki/MAPS-Adaptations)** — project-governance ideas adapted into teaching.
- **[Research Foundations](https://github.com/BigCatMellow/Rung_Teaching/wiki/Research-Foundations)** — learning-science basis and limitations.
- **[Sources](https://github.com/BigCatMellow/Rung_Teaching/wiki/Sources)** — primary references and citations.

---

# Research position

Rung is a practical synthesis, not a claim that one instructional technique is universally optimal.

Its components draw on research concerning retrieval practice, self-explanation, worked examples and guidance fading, cognitive load, and productive failure. The evidence supports an **adaptive** position rather than either extreme of “always tell the learner exactly what to do” or “never tell the learner anything.”

The operating rule is:

> **Make the learner do as much of the important thinking as they can productively do, provide the minimum structure needed when they cannot, and systematically fade that structure as competence grows.**

See **[Research Foundations](https://github.com/BigCatMellow/Rung_Teaching/wiki/Research-Foundations)** and **[Sources](https://github.com/BigCatMellow/Rung_Teaching/wiki/Sources)** for the evidence trail.