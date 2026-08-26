# Rung Teaching

**Rung Teaching** is a teaching system built around a simple operating idea: the learner attempts the task, the teacher diagnoses where the reasoning breaks, gives only enough help to restore productive progress, then reduces that help until the learner can solve a meaningfully different version independently.

Rung distinguishes between two modes:

- **Output Mode:** the finished result is the product.
- **Teaching Mode:** the learner's increasing independence is the product.

Rung is deliberately not “Socratic questioning all the time.” Questions are the main diagnostic tool, but the teacher should use the **least help that still allows productive progress**. A novice may need a prerequisite explained or a worked example before a question becomes useful. As competence rises, that support should fade.

---

# If you want to use Rung now

Start with **[[Set Up and Use the Rung Teacher|Setup-and-Use]]**.

That page tells you:

- which prompt to use;
- how to configure an AI agent;
- what the learner needs to provide;
- exactly what the teacher should do on the first turn;
- how to run the loop;
- how to use the Assistance Ladder;
- what state to preserve across sessions;
- when to switch to Output Mode;
- how to handle common failure cases;
- how to know when the learner is actually independent.

If the AI can already read this repository, the short invocation is:

```text
Use the Rung Teaching System in this repository.
Read AGENTS.md and the relevant Rung wiki pages.
Teach me [SUBJECT/SKILL].
```

If it cannot reliably read the repository, use the complete portable prompt in:

https://github.com/BigCatMellow/Rung_Teaching/blob/main/prompts/RUNG_AGENT_INSTRUCTIONS.md

---

# The core loop

```text
DEFINE THE SKILL
      ↓
BASELINE
      ↓
ATTEMPT
      ↓
DIAGNOSE
      ↓
MINIMUM HELP
      ↓
REATTEMPT
      ↓
VERIFY
      ↓
TRANSFER
      ↓
RECORD THE LESSON
```

The goal is not merely for the learner to reach the right answer. The goal is for them to internalize the questions, tests, principles, and checking habits that produced it.

---

# Why “Rung”?

Learning is treated as a ladder rather than a switch. The teacher should know how much structure the learner currently needs and provide only enough to reach the next level of independent performance.

A typical progression is:

```text
Teacher carries the reasoning
        ↓
Teacher and learner share the reasoning
        ↓
Learner carries the reasoning
        ↓
Teacher audits the reasoning
        ↓
Learner works independently
```

This is related to the learning-science idea of **guidance fading**: novices often benefit from substantial structure, while excessive guidance becomes less useful as expertise develops. See [[Research Foundations]].

---

# Documentation path

## Use it

1. **[[Setup and Use|Setup-and-Use]]** — the default operational guide.
2. **[[AI Agent Instructions]]** — how to deploy Rung as standing AI instructions.

## Run the method

3. **[[Getting Started]]** — define target, mastery proof, baseline, and boundary.
4. **[[Teaching Loop]]** — live interaction cycle.
5. **[[Assistance Ladder]]** — decide how much help to give.
6. **[[Diagnosing Mistakes]]** — classify failures before correcting them.
7. **[[Mastery and Transfer]]** — determine whether learning actually transferred.

## Understand why it is designed this way

8. **[[MAPS Adaptations]]** — MAPS_Lean concepts translated into teaching.
9. **[[Research Foundations]]** — learning-science basis and limitations.
10. **[[Sources]]** — primary links and citations.

---

# Evidence policy

Rung separates three kinds of statements:

- **System rule** — a deliberate design choice in Rung.
- **MAPS-derived rule** — adapted from a specific MAPS_Lean project-control method.
- **Research-supported rule** — supported by learning-science research, with the source named.

These categories should not be blurred. A useful design rule is not automatically a scientific law, and a research finding does not automatically dictate one universal teaching procedure.

---

# The shortest usable version

If you remember only six things:

1. Define what the learner should eventually do **without help**.
2. See what they can actually do before teaching them.
3. Ask one diagnostic question at a time.
4. Give the least help needed for productive progress.
5. Make the learner explain, correct, and reapply the idea themselves.
6. Do not call it learned until it transfers to a fresh problem.

The repository README provides the compact system overview:

https://github.com/BigCatMellow/Rung_Teaching/blob/main/README.md
