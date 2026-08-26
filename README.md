# Rung Teaching System

**Rung works by having the learner attempt the task first, diagnosing exactly where the reasoning breaks, giving only enough help to restore productive progress, then repeating with less support until the learner can solve a meaningfully different version independently.**

Rung is the teaching method. **TeachMe** is the portable AI skill that runs it in Codex and Claude.

The goal is not merely to improve the current answer, story, program, design, or project. The goal is to make the learner increasingly capable of doing that class of work without the teacher.

Rung grew from a Socratic teaching method, but it is **not** “only ask questions.” Questions are used diagnostically. When prerequisite knowledge is missing, the teacher explains it directly; when the learner can reason productively, the teacher avoids taking over.

---

# Start here

## If TeachMe is installed

The minimum request is simply:

```text
/teachme Teach me [what you want to learn].
```

Examples:

```text
/teachme Teach me how to improve my story.
```

```text
/teachme Teach me how to write SQL joins without copying examples.
```

```text
/teachme Teach me how to evaluate whether a historical claim is well supported.
```

You can attach or link the thing you want to work from:

```text
/teachme Teach me how to improve my story.
[attach or link the story]
```

TeachMe should read the supplied work before deciding what to teach.

## If the AI can read this repository but does not use Skills

Use:

```text
Use the Rung Teaching System in this repository.
Read AGENTS.md and the relevant Rung wiki pages.
Teach me [SUBJECT/SKILL].
```

## If the AI cannot read this repository reliably

Copy the complete prompt from:

[`prompts/RUNG_AGENT_INSTRUCTIONS.md`](prompts/RUNG_AGENT_INSTRUCTIONS.md)

Then add:

```text
Teach me [SUBJECT/SKILL].
```

Full setup instructions: **[Set Up and Use the Rung Teacher](https://github.com/BigCatMellow/Rung_Teaching/wiki/Setup-and-Use)**.

---

# Example: using TeachMe to improve a story

This example shows the intended interaction from beginning to end.

The learner does **not** need to know the Rung terminology, choose an Assistance Ladder level, or diagnose their own weakness. They only need to say what they want to learn and provide the relevant work.

## 1. Invoke TeachMe

**Learner**

```text
/teachme Teach me how to improve my story.
[story attached]
```

“Improve my story” is broad. The problem might be prose, pacing, character motivation, structure, tension, scene construction, dialogue, or something else.

TeachMe has two reasonable ways to begin:

- **Direct diagnostic** — TeachMe chooses the strongest learning target it can see in the work and starts there.
- **Interview Mode** — TeachMe asks one question at a time to understand what the learner wants the work to accomplish, then identifies the skill to practice.

For a subjective goal like this, TeachMe may ask:

**TeachMe**

> I’ve read the story. “Improve my story” could lead in several useful directions. I can either choose the strongest learning target I see and start there, or interview you one question at a time so the target is based on what you want the story to accomplish. Which do you want?

**Learner**

> Interview me first.

## 2. Interview Mode narrows the goal

Interview Mode is not a questionnaire. Each question should follow from the previous answer.

**TeachMe**

> At the end of this scene, what do you most want the reader to understand or feel about Mara?

**Learner**

> I want them to feel that she desperately wants to leave, but she is afraid that leaving means abandoning her brother.

The next question should use that answer rather than switching to an unrelated checklist item.

**TeachMe**

> Where in the current scene do you think the reader can most clearly see both halves of that conflict?

**Learner**

> Probably when she picks up the car keys and then puts them back.

**TeachMe**

> What in that moment tells the reader that her hesitation is specifically about her brother rather than just general fear or indecision?

**Learner**

> Actually, nothing. I know that is why she is doing it, but I don’t think the reader does.

At this point the interview has done its job. TeachMe has found a concrete learning target.

## 3. TeachMe names the skill

**TeachMe**

> That gives us the first skill to work on: **making a character’s internal conflict legible through concrete scene details instead of relying on information that exists only in the writer’s head.**
>
> I’m not going to rewrite the scene for you. Let’s use the keys moment as the first attempt.

The broad goal “improve my story” has become an observable skill.

## 4. The learner attempts the repair

**TeachMe**

> Without adding an explanatory paragraph, what could Mara notice, touch, avoid, or react to that would connect putting the keys down specifically to her brother?

**Learner**

> Maybe his school bag is sitting next to the door, and when she reaches for the keys she sees it.

**TeachMe**

> That can work. Why is the school bag stronger than simply having her think, “I can’t leave him”?

**Learner**

> Because the bag makes the brother physically present in the scene without explaining what she feels.

TeachMe is now testing whether the learner understands the principle, not merely whether they can accept a suggestion.

## 5. The learner writes the change

**TeachMe**

> Write only that beat—two to four sentences. Keep the same basic action: she reaches for the keys and decides not to take them.

**Learner**

> Mara hooked one finger through the key ring. Her brother’s backpack leaned against the door beneath his raincoat, one strap still twisted from where he had dropped it. She held the keys for another second, then set them back in the bowl.

## 6. TeachMe diagnoses instead of taking over

TeachMe might respond:

> The connection is clearer now, but I want to test whether you can diagnose your own version: which detail is doing the actual emotional work, and which detail might just be decoration?

The learner answers. TeachMe uses that answer to choose the next question or the next Assistance Ladder rung.

If the learner is stuck because they do not understand a prerequisite concept—such as concrete detail, subtext, or point of view—TeachMe explains the minimum missing concept and hands the work back.

## 7. The same principle is tested again

After the learner can handle the original scene, TeachMe should not declare mastery simply because the coached revision improved.

It should use a fresh or changed case:

> Here is a different situation: a character wants to accept a job overseas but feels responsible for an aging parent. Without using internal narration that directly states the conflict, sketch one small action or environmental detail that could make both pressures visible.

If the learner can recognize and apply the principle without being led to the answer, the evidence for transfer is stronger.

## What happened underneath the conversation

```text
“Teach me how to improve my story”
        ↓
read the supplied story
        ↓
INTERVIEW MODE
one question → answer → next question
        ↓
identify the actual bottleneck
        ↓
name an observable skill
        ↓
learner attempts
        ↓
diagnose the reasoning
        ↓
give minimum useful help
        ↓
learner revises
        ↓
verify understanding
        ↓
try a changed example
        ↓
fade the teacher out
```

That is Rung in practice.

---

# Direct Diagnostic vs. Interview Mode

TeachMe supports two starting styles. They are not different teaching systems; both feed into the same Rung loop.

## Direct Diagnostic — default

Use when the requested skill is already clear.

```text
/teachme Teach me how to choose between INNER JOIN and LEFT JOIN.
```

TeachMe should normally start with a small problem and see how the learner currently makes that decision.

## Interview Mode — optional

Use when the learner asks for it or when the goal is broad and intent materially changes what should be taught.

```text
/teachme Teach me how to improve my story. Interview me first.
```

Interview Mode follows:

```text
one consequential question
→ learner answer
→ next question chosen from that answer
→ enough information to identify the target
→ stop interviewing
→ begin teaching
```

It should **not** become a ten-question intake form.

---

# What a correctly configured Rung teacher should do first

When the learner gives a clear skill target, the teacher should **not** begin with a long lecture or a large questionnaire.

The first turn should:

1. identify the specific skill;
2. reuse context already established instead of asking for it again;
3. read supplied artifacts or source material when the task depends on them;
4. define a provisional observable mastery target;
5. identify any genuinely necessary missing prerequisite or constraint;
6. begin with a small cold attempt when the target is clear enough;
7. otherwise ask **one** necessary setup question or begin Interview Mode when appropriate.

The teacher learns about the learner primarily by observing real attempts, not by collecting self-reported preferences before practice begins.

---

# The learning contract

At the start of a learning arc, Rung needs five things.

## 1. A specific skill

Write the target as something the learner will eventually **do**.

Weak:

> Understand character motivation.

Better:

> Given an unfamiliar scene, identify whether a character choice is adequately motivated, explain what evidence makes it feel earned or unearned, and revise a weak beat without being told what detail to add.

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

In ordinary conversation:

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

> What in that moment tells the reader the hesitation is about her brother?

instead of stacking:

> Why did she hesitate? What detail shows it? What emotion is she feeling? What should you add? How would you rewrite it?

“One question at a time” means the learner should normally face one important reasoning task at a time. The response determines what comes next.

A good diagnostic question:

- points at a specific decision;
- exposes a recurring failure mode;
- requires reasoning rather than preference;
- can be reused on future cases;
- can eventually become a self-check the learner runs without the teacher.

---

# The Assistance Ladder

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

After a full solution, require explanation, independent reapplication, and transfer before treating the skill as learned.

Detailed explanation: **[Assistance Ladder](https://github.com/BigCatMellow/Rung_Teaching/wiki/Assistance-Ladder)**.

---

# Productive struggle vs. useless struggle

Difficulty is useful only while it produces information or learning.

**Productive struggle** means the learner has enough prerequisite knowledge to form plausible approaches, makes interpretable mistakes, responds to targeted cues, and is still learning from the attempt.

**Useless struggle** means the learner lacks necessary concepts, guesses randomly, repeats the same move without understanding, cannot use the feedback, or is spending effort on mechanics unrelated to the skill.

When struggle becomes useless, move up the Assistance Ladder.

Rung is not a system for withholding answers. It is a system for making the learner perform as much of the important reasoning as they can productively perform.

---

# Diagnose before correcting

Common failure categories are:

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

```text
VERDICT
→ LOCATION
→ REASON
→ NEXT TEST
```

Do not hide an important error behind praise. Do not call merely acceptable work excellent. The learner should normally perform the repair themselves.

---

# Evidence discipline

For factual or research-dependent subjects, distinguish when useful among:

- **VERIFIED** — directly checked or demonstrated.
- **REPORTED** — stated by a source but not independently demonstrated here.
- **ASSUMED** — provisionally treated as true.
- **UNKNOWN** — unresolved.

Confidence is not evidence.

When the learner supplies a story, document, dataset, codebase, source, or other material, use that material as the requested basis. Do not silently replace its terminology, assumptions, organization, or content with generic outside material unless the learner asks for research or verification.

---

# Repeated mistakes become reusable tools

Repeated failures should produce durable countermeasures such as diagnostic questions, standing principles, checklist items, deliberate-practice drills, comparison examples, or required self-checks.

```text
OBSERVATION
→ POSSIBLE PATTERN
→ TEST
→ REPEATED EVIDENCE
→ STANDING PRINCIPLE
```

A one-time observation should not automatically become permanent doctrine.

---

# Mastery is not assisted success

When applicable, test:

1. **Recognition** — can the learner recognize when the principle applies?
2. **Execution** — can they perform it independently?
3. **Explanation** — can they explain why it works?
4. **Error detection** — can they identify or catch plausible mistakes?
5. **Transfer** — can they apply it in a meaningfully changed case?
6. **Delayed retrieval** — when durable memory matters, can they still use it later without rereading first?

Do not use the heavily coached practice problem as the final proof of learning.

Detailed explanation: **[Mastery and Transfer](https://github.com/BigCatMellow/Rung_Teaching/wiki/Mastery-and-Transfer)**.

---

# Guidance should fade

```text
teacher carries reasoning
→ teacher and learner share reasoning
→ learner carries reasoning
→ teacher audits reasoning
→ learner operates independently
```

If the learner succeeds with lighter cues, stop giving explanations they no longer need. If the learner repeatedly fails with light cues, escalate rather than pretending that withholding help is rigor.

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

---

# Teaching Mode and Output Mode

Rung should never trap the learner in a lesson when they simply want a result.

## Teaching Mode

```text
/teachme Teach me this rather than doing it for me.
```

The learner's growing independence is the product.

## Output Mode

```text
Output mode. Just give me the answer.
```

The result is the product. Providing it does not count as mastery evidence.

To resume:

```text
Back to TeachMe / Teaching Mode.
```

---

# Fail-safe rules

### Missing prerequisite
Teach the minimum missing concept directly, then return to application.

### Repeatedly stuck learner
Escalate the Assistance Ladder. Do not endlessly rephrase the same question.

### Right answer for the wrong reason
Diagnose the reasoning; do not mark it mastered.

### Trivial execution slip
Point to the discrepancy and let the learner repair it rather than reteaching the entire concept.

### Uncertain facts
Verify them or label the uncertainty. Do not invent facts to preserve momentum.

### Supplied source material
Use the supplied material as the requested basis. Do not silently substitute generic content.

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

# TeachMe Agent Skill

Canonical skill source:

```text
skills/teachme/
```

Codex mirror:

```text
.agents/skills/teachme/
```

Claude mirror:

```text
.claude/skills/teachme/
```

Edit only the canonical package. The GitHub workflow mirrors it to both agent locations.

See **[TeachMe Agent Skill](https://github.com/BigCatMellow/Rung_Teaching/wiki/Agent-Skills)**.

---

# Documentation map

## Use Rung / TeachMe

- **[Set Up and Use](https://github.com/BigCatMellow/Rung_Teaching/wiki/Setup-and-Use)** — setup and operating guide.
- **[Example: Story Improvement](https://github.com/BigCatMellow/Rung_Teaching/wiki/Example-Story-Session)** — complete conversational example.
- **[TeachMe Agent Skill](https://github.com/BigCatMellow/Rung_Teaching/wiki/Agent-Skills)** — Codex and Claude installation/use.
- **[`AGENTS.md`](AGENTS.md)** — canonical contract for repository-aware AI teachers.
- **[`prompts/RUNG_AGENT_INSTRUCTIONS.md`](prompts/RUNG_AGENT_INSTRUCTIONS.md)** — portable fallback prompt.
- **[AI Agent Instructions](https://github.com/BigCatMellow/Rung_Teaching/wiki/AI-Agent-Instructions)** — deployment choices and instruction precedence.

## Understand the method

- **[Getting Started](https://github.com/BigCatMellow/Rung_Teaching/wiki/Getting-Started)**
- **[Teaching Loop](https://github.com/BigCatMellow/Rung_Teaching/wiki/Teaching-Loop)**
- **[Assistance Ladder](https://github.com/BigCatMellow/Rung_Teaching/wiki/Assistance-Ladder)**
- **[Diagnosing Mistakes](https://github.com/BigCatMellow/Rung_Teaching/wiki/Diagnosing-Mistakes)**
- **[Mastery and Transfer](https://github.com/BigCatMellow/Rung_Teaching/wiki/Mastery-and-Transfer)**

## Understand the foundations

- **[MAPS Adaptations](https://github.com/BigCatMellow/Rung_Teaching/wiki/MAPS-Adaptations)**
- **[Research Foundations](https://github.com/BigCatMellow/Rung_Teaching/wiki/Research-Foundations)**
- **[Sources](https://github.com/BigCatMellow/Rung_Teaching/wiki/Sources)**

---

# Research position

Rung is a practical synthesis, not a claim that one instructional technique is universally optimal.

Its components draw on research concerning retrieval practice, self-explanation, worked examples and guidance fading, cognitive load, and productive failure. The evidence supports an **adaptive** position rather than either extreme of “always tell the learner exactly what to do” or “never tell the learner anything.”

The operating rule is:

> **Make the learner do as much of the important thinking as they can productively do, provide the minimum structure needed when they cannot, and systematically fade that structure as competence grows.**

See **[Research Foundations](https://github.com/BigCatMellow/Rung_Teaching/wiki/Research-Foundations)** and **[Sources](https://github.com/BigCatMellow/Rung_Teaching/wiki/Sources)** for the evidence trail.
