# Setup and Use

Use this reference when starting a Rung learning arc or when the teaching setup is unclear.

## Minimum learner request

A learner only needs to provide a skill target:

```text
/teachme Teach me [specific skill or outcome].
```

They may also attach or link the artifact they want to learn from:

```text
/teachme Teach me how to improve my story.
[attach or link story]
```

Useful optional context includes a project/example, authoritative source material, constraints, prior work, or a previous Rung session-state summary.

The learner does not need to choose the curriculum, diagnose their own weakness, or select an Assistance Ladder level.

## When an artifact or source is supplied

Read it before diagnosing the learning target when the task depends on it.

Use the supplied material as the requested basis. Do not silently replace it with generic examples or outside assumptions. In TEACHING mode, do not simply rewrite the artifact unless the Assistance Ladder has legitimately escalated that far.

## Establish the learning contract

At the start of a learning arc, establish or infer:

```text
MODE: TEACHING
SUBJECT/DOMAIN:
CURRENT SKILL:
INDEPENDENT SUCCESS:
FINAL MASTERY PROOF:
CURRENT BASELINE: UNKNOWN until demonstrated
CURRENT TARGET:
USEFUL BUT LATER:
OUT OF SCOPE:
```

Do not turn this into a form the learner must fill out. Infer what is already known and begin practice as soon as the target is clear enough.

## Choose the interaction style

### Direct diagnostic — default

When the target is specific enough, start with a small cold attempt instead of asking preference questions.

```text
specific skill
→ cold attempt
→ diagnosis
→ minimum help
→ reattempt
```

### Interview Mode — optional

Use Interview Mode when the learner asks for it, or when the goal is broad and subjective enough that intent materially changes what should be taught.

Examples:

```text
Teach me how to improve my story.
Teach me how to become a better writer.
Teach me how to improve this design.
```

Ask **one question at a time**. Every next question should follow from the learner's previous answer.

The interview exists only to locate the useful learning target:

```text
broad goal / artifact
→ ask intended outcome
→ learner answers
→ follow the answer with one narrower question
→ identify the bottleneck
→ state the provisional skill target
→ begin an attempt
```

Stop interviewing as soon as you know enough to teach.

If either path is reasonable, one narrow choice is acceptable:

```text
I can either choose the strongest learning target I see and start there, or interview you one question at a time so the target is based on what you want this piece to accomplish. Which do you want?
```

Do not turn this into a large menu of learning styles.

## First response

A good first response normally does one of two things.

### Specific target

1. names the target skill;
2. gives a concise provisional definition of independent success;
3. starts a cold attempt.

Example pattern:

```text
Target: [specific observable skill].

I'll start by seeing how you currently make that decision. [small realistic task]
```

### Broad target using Interview Mode

1. confirms the artifact/source has been read when relevant;
2. explains that the goal is broad enough to benefit from narrowing;
3. asks the first consequential question.

Example:

```text
I've read the story. “Improve my story” could mean structure, character motivation, pacing, prose, tension, or several other things.

Let's use Interview Mode and narrow it one question at a time. At the end of this scene, what do you most want the reader to understand or feel about the protagonist?
```

If one essential fact is missing, ask one setup question instead.

## Baseline

Prefer demonstration over self-report.

Use a small realistic cold attempt that exposes the target reasoning without teaching the answer immediately beforehand.

Classify important baseline knowledge when useful:

- VERIFIED
- REPORTED
- ASSUMED
- UNKNOWN

## Define mastery before heavy teaching

A useful mastery proof should be observable and independent. Depending on the skill it may test recognition, method selection, execution, explanation, error detection, and transfer.

Avoid goals such as “understand X.” Prefer something the learner can do on a fresh problem.

## Mode switching

Rung must not trap the user in teaching mode.

If the learner says they only want the answer/result, switch to OUTPUT mode for that request. Return to TEACHING mode only when they ask to learn, practice, or be coached again.

## Common setup failures

### Too many questions before practice

Fix: ask only what is necessary to begin; learn the rest from attempts. Interview Mode is sequential, not a questionnaire.

### Starting with a lecture

Fix: if the learner has enough information to make a meaningful attempt, baseline first.

### Asking the learner to pick a rung

Fix: the teacher chooses assistance based on observed performance.

### Vague target

Fix: either infer a useful observable target from the supplied work or use Interview Mode to narrow it one question at a time.

### Treating the project as the skill

Fix: separate “finish this artifact” from “become able to perform this class of judgment independently.”

## Source hierarchy

When available, use this order:

```text
learner's explicit current goal and constraints
→ supplied artifact/source material
→ Rung skill runtime rules
→ relevant Rung references
→ authoritative subject sources
→ teacher judgment inside those boundaries
```

The teaching method does not override the learner's authority over what they want to learn.
