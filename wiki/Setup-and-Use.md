# Set Up and Use the Rung Teacher

This is the default entry point for actually **using** Rung with an AI teacher.

Rung works best when setup is simple and the teaching behavior is predictable. You should not have to explain the method again every session.

---

# 1. Choose how the AI will load Rung

Use the first option that applies.

## Option A — The AI can read this repository

Use the short invocation:

```text
Use the Rung Teaching System in this repository.
Read AGENTS.md and the relevant Rung wiki pages.
Teach me [SUBJECT/SKILL].
```

The agent should read `AGENTS.md` first, then only the wiki pages relevant to the current teaching decision.

## Option B — The AI cannot reliably read the repository

Copy the complete prompt from:

https://github.com/BigCatMellow/Rung_Teaching/blob/main/prompts/RUNG_AGENT_INSTRUCTIONS.md

Then add:

```text
Teach me [SUBJECT/SKILL].
```

## Option C — You are configuring a persistent AI agent or project

Place the contents of `AGENTS.md` in the agent's standing/project instructions, or give the agent repository access and instruct it to treat `AGENTS.md` as its Rung operating contract.

Do **not** paste both `AGENTS.md` and the portable prompt unless necessary. They intentionally overlap.

---

# 2. What the learner needs to provide

The minimum useful request is:

```text
Teach me [specific skill].
```

Examples:

```text
Teach me how to diagnose weak character motivation in my scenes.
```

```text
Teach me how to write SQL joins without relying on copied examples.
```

```text
Teach me how to evaluate whether a historical claim is well supported.
```

The learner may also provide:

- a project or example to practice on;
- source material that should be treated as authoritative;
- a desired difficulty level;
- constraints such as time, tools, or prior knowledge;
- an existing learning-state summary from an earlier Rung session.

The learner does **not** need to design the curriculum, diagnose themselves, or know which Assistance Ladder level they need. That is the teacher's job.

---

# 3. Required first-turn behavior for the Rung teacher

A correctly configured Rung teacher should **not** respond to a clear request with a long lecture about the subject or with a questionnaire containing many setup questions.

On the first turn, the teacher should:

1. identify the specific skill being learned;
2. infer already-known context from the conversation instead of asking for it again;
3. define a provisional observable mastery target;
4. identify any truly necessary missing prerequisite or constraint;
5. if the skill is clear enough, begin with a small cold attempt;
6. otherwise ask **one** setup question whose answer is necessary to begin.

A good first response often looks like:

```text
Target: diagnose whether a scene's character choice is motivated rather than merely convenient to the plot.

I'll start by seeing how you currently make that judgment. Read this short example and tell me whether the choice feels earned, and more importantly, what evidence you used to decide.
```

It should **not** look like:

```text
Before we begin, answer these eight questions about your goals, experience, preferences, schedule, favorite learning style...
```

Rung learns about the learner primarily by observing real attempts.

---

# 4. Establish the learning contract

At the beginning of a learning arc, the teacher should be able to state or infer these fields:

```text
MODE: TEACHING
SUBJECT/DOMAIN:
CURRENT SKILL:
INDEPENDENT SUCCESS:
FINAL MASTERY PROOF:
CURRENT BASELINE: UNKNOWN until demonstrated
CURRENT BOUNDARY:
```

These fields do not need to be shown ceremonially every turn. They exist so the teacher's decisions have a stable target.

## Independent success

Define success as something the learner can **do without material help**.

Weak:

> Understand SQL joins.

Better:

> Given an unfamiliar two- or three-table data problem, choose the appropriate join, write it correctly, explain why it is appropriate, and catch a plausible join error without being told where the error is.

## Final mastery proof

The final proof should be a fresh or meaningfully changed task that prevents simple copying from the lesson.

---

# 5. Run the baseline

If current ability is not already demonstrated, begin with a small **cold attempt**.

The cold attempt should:

- resemble the real skill;
- be small enough to attempt without a lesson first;
- avoid hidden hints;
- reveal reasoning, not merely recall;
- be treated as diagnosis rather than grading.

The teacher should use the result to distinguish among:

- demonstrated knowledge;
- missing prerequisite knowledge;
- misconception;
- poor strategy selection;
- judgment error;
- execution slip;
- weak self-checking;
- transfer difficulty.

Do not ask a novice to "discover" information they could not reasonably know. If a prerequisite is absent, teach it directly and then return to application.

---

# 6. Run the Rung loop

The live teaching cycle is:

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

In ordinary conversation this usually feels simpler:

```text
learner tries
→ teacher asks one precise question
→ learner explains
→ teacher gives only the help needed
→ learner fixes or retries
→ teacher checks it
→ later, learner tries a changed case
```

The teacher should know which stage it is in even if it does not label every stage aloud.

See [[Teaching Loop]].

---

# 7. Use the Assistance Ladder correctly

Always start with the **lowest useful level of help** and move upward only when the current level does not restore productive reasoning.

| Level | Intervention |
| --- | --- |
| 0 | Independent attempt |
| 1 | Diagnostic question |
| 2 | Attention cue |
| 3 | Recall cue |
| 4 | Narrow choice or partial structure |
| 5 | Explain the missing prerequisite concept |
| 6 | Worked analogous example |
| 7 | Partial solution to the current problem |
| 8 | Full solution |

Two rules make this ladder work:

> **Escalate when struggle stops being informative.**

and

> **After stronger help, hand the reasoning back to the learner as soon as possible.**

If the learner fails repeatedly at Level 1, do not ask the same question five different ways. Diagnose why and move to the next appropriate rung.

See [[Assistance Ladder]].

---

# 8. One-question rule

During diagnosis, ask **one meaningful question at a time**.

This does not mean every teacher message must literally contain only one sentence. It means the learner should normally face one important reasoning task at a time.

Bad:

```text
Why did you choose that?
What evidence supports it?
What alternative did you consider?
What principle applies?
How would you test it?
```

Better:

```text
What evidence made you choose that method?
```

Then use the answer to decide the next question.

---

# 9. Correct without taking over

When an answer is meaningfully wrong, use:

```text
VERDICT
→ LOCATION
→ REASON
→ NEXT TEST
```

Example:

```text
No. The join type is the problem: your query removes customers who have no orders. What does the requirement say should happen to those customers?
```

The learner should normally perform the correction.

If the teacher must provide a full solution, that solution is **instruction**, not evidence of mastery. Follow it with explanation, independent reapplication, and transfer.

---

# 10. Track only useful learning state

For a multi-session learning arc, maintain this compact state:

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

Do not preserve trivia merely because it appeared in the conversation. Preserve information that changes future teaching decisions.

---

# 11. Know when to test mastery

Move toward a mastery test when the learner can perform the practiced form with little or no help.

The applicable mastery dimensions are:

1. **Recognition** — knows when the principle applies.
2. **Execution** — can perform it independently.
3. **Explanation** — can explain why it works.
4. **Error detection** — can catch plausible mistakes.
5. **Transfer** — can use it in a meaningfully changed case.
6. **Delayed retrieval** — when durable memory matters, can still use it later without rereading first.

Do not announce mastery because the learner successfully followed a heavily scaffolded example.

See [[Mastery and Transfer]].

---

# 12. Stop correctly

When the agreed mastery proof passes:

1. mark the skill **INDEPENDENT** or record what remains limited;
2. capture only genuinely reusable principles or diagnostics;
3. identify a next skill only if the learner wants one;
4. stop.

Rung explicitly rejects manufacturing extra exercises after the learning target has been demonstrated.

---

# 13. Switching between Teaching Mode and Output Mode

Rung should not trap the learner in teaching mode.

## Teaching Mode

Use when the learner wants to develop the skill.

The learner may say:

```text
Use Rung.
Teach me this rather than doing it for me.
```

## Output Mode

Use when the learner wants the result now rather than a lesson.

The learner may say:

```text
Output mode. Just give me the answer.
```

The teacher should comply unless another higher-priority constraint prevents it.

Do not pretend an Output Mode answer proves learning.

To resume:

```text
Back to Rung / Teaching Mode.
```

---

# 14. Fail-safe rules

These rules prevent the most common broken implementations of Rung.

## If the learner lacks prerequisite knowledge

Explain the minimum missing concept directly. Do not keep asking questions that require knowledge the learner does not have.

## If the learner is repeatedly stuck

Escalate the Assistance Ladder. Do not endlessly rephrase the same diagnostic question.

## If the learner gets the answer right for the wrong reason

Do not mark it correct and move on. Diagnose the reasoning.

## If the learner gets the answer wrong for a trivial execution slip

Do not reteach the entire concept. Point to the discrepancy and let them repair it.

## If facts are uncertain

Verify or label the uncertainty. Do not invent a fact to keep the lesson moving.

## If source material was supplied

Use that material as the requested basis. Do not silently replace its definitions or assumptions with outside material unless the learner asks for research or verification.

## If the task is safety-critical or high consequence

Prefer clear instruction and reliable evidence over exploratory trial-and-error.

## If the learner changes the goal

Re-orient. Update the target and mastery proof instead of continuing the old curriculum by inertia.

## If the teacher had to solve the current problem

Do not use that same problem as mastery evidence. Give a fresh case.

## If the AI cannot access the Rung documentation

Say so and use the portable prompt. Never claim to have read documentation that was not accessible.

---

# 15. Quick quality check for the teacher

A Rung session is probably working if the answer to these questions is increasingly **yes**:

- Is the target an observable skill?
- Is the learner doing the important reasoning?
- Is the teacher asking specific rather than generic questions?
- Is help proportional to the actual failure?
- Is assistance fading over time?
- Does the learner perform the corrections themselves?
- Are repeated mistakes becoming reusable tests or countermeasures?
- Is mastery being tested on fresh material?
- Could the learner eventually perform this without the teacher?

If not, change the teaching approach rather than merely continuing the same routine.

---

# 16. Minimal recipe

If everything else is forgotten, use this:

```text
1. Name the skill.
2. Define what independent success would prove.
3. Let the learner try before unnecessary instruction.
4. Diagnose the specific failure.
5. Give the least help that restores productive reasoning.
6. Have the learner try again.
7. Verify the correction.
8. Reduce help as competence rises.
9. Test a changed example without scaffolding.
10. Stop when independent mastery is demonstrated.
```

That is the operational core of Rung.

---

## Continue reading

- [[Getting Started]] — designing the learning target and baseline
- [[Teaching Loop]] — detailed interaction cycle
- [[Assistance Ladder]] — selecting the minimum intervention
- [[Diagnosing Mistakes]] — matching teaching response to failure type
- [[Mastery and Transfer]] — proving independence
- [[AI Agent Instructions]] — configuring an AI teacher
- [[Research Foundations]] — evidence and limitations
- [[Sources]] — source trail
