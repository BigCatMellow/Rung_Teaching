# TeachMe Agent Skill for Codex and Claude

**TeachMe** is the portable Agent Skill for the **Rung Teaching System**.

The naming distinction is intentional:

- **TeachMe** is the capability the user invokes.
- **Rung** is the teaching method TeachMe follows.

This lets Rung remain the name of the framework while giving the installed skill a simple user-facing command.

The skill does **not** replace `AGENTS.md`, the README, or this wiki. Those pieces serve different purposes:

| Component | Role |
| --- | --- |
| `README.md` | Human quickstart, complete example, and system overview |
| Wiki | Detailed method, examples, research, explanations, and sources |
| `AGENTS.md` | Persistent Rung operating contract when working inside this repository |
| `skills/teachme/` | Canonical portable TeachMe Agent Skill |
| `.agents/skills/teachme/` | Codex-compatible mirror |
| `.claude/skills/teachme/` | Claude-compatible mirror |
| `prompts/RUNG_AGENT_INSTRUCTIONS.md` | Fallback when Skills/repository instructions are unavailable |

---

# What using TeachMe looks like

The user only needs to name what they want to learn.

For writing:

```text
/teachme Teach me how to improve my story.
[attach or link story]
```

TeachMe reads the supplied work before choosing the learning target.

If the goal is already specific enough, it starts with a **Direct Diagnostic**.

If the goal is broad and subjective, TeachMe can use **Interview Mode**:

```text
/teachme Teach me how to improve my story. Interview me first.
```

Interview Mode asks one consequential question at a time. Each next question is chosen from the learner's previous answer until a concrete skill or bottleneck is identified; then the interview stops and the normal Rung loop begins.

Example shape:

```text
story supplied
→ “What do you want the reader to feel here?”
→ learner answers
→ next question follows from that answer
→ specific writing weakness becomes visible
→ define the skill
→ learner attempts
→ diagnose
→ minimum help
→ reattempt
→ transfer
```

See **[[Example: Story Improvement|Example-Story-Session]]** for the complete conversation.

---

# Canonical skill

The only skill package that should be edited directly is:

```text
skills/teachme/
├── SKILL.md
└── references/
    ├── setup-and-use.md
    ├── teaching-loop.md
    ├── assistance-ladder.md
    ├── diagnosing-mistakes.md
    ├── mastery-and-transfer.md
    └── session-state.md
```

`SKILL.md` contains the stable runtime behavior. The reference files provide progressive detail only when the current teaching decision needs it.

This keeps TeachMe compact enough for discovery while preserving the detailed Rung behavior required for reliable teaching.

---

# Codex

The repository exposes TeachMe to Codex at:

```text
.agents/skills/teachme/
```

The complete directory is a generated mirror of the canonical package.

To invoke it explicitly:

```text
Use the teachme skill to teach me how to diagnose weak SQL joins.
```

Or:

```text
Teach me how to improve my story using TeachMe.
```

The skill description is written so learning/coaching requests can also be recognized as appropriate triggers when skill discovery is available.

---

# Claude

The repository exposes TeachMe to Claude at:

```text
.claude/skills/teachme/
```

The complete directory is also a generated mirror of the canonical package.

Invoke it explicitly with:

```text
/teachme Teach me how to evaluate the evidence behind a historical claim.
```

or:

```text
/teachme Teach me how to improve my story. Interview me first.
```

Or ask Claude normally to teach or coach you when automatic skill selection is available.

---

# Installing TeachMe in another project

You do not need to copy the entire Rung_Teaching repository.

## For Codex

Copy the canonical package into the target project as:

```text
.agents/skills/teachme/
```

## For Claude

Copy the canonical package into the target project as:

```text
.claude/skills/teachme/
```

If a project uses both systems, install the same canonical package in both locations.

The package is self-contained for normal runtime behavior. The main Rung wiki remains useful when a human or agent needs deeper explanation, examples, the learning-science basis, MAPS adaptations, or source citations.

---

# Automatic synchronization

Do **not** manually maintain the Codex and Claude mirrors.

The GitHub Action:

```text
.github/workflows/sync-rung-skills.yml
```

copies:

```text
skills/teachme/
```

into both:

```text
.agents/skills/teachme/
.claude/skills/teachme/
```

whenever the canonical package changes on `main`.

The workflow also removes the former generated `rung-teaching` mirror paths. This keeps one runtime source of truth instead of parallel skill names that can drift apart.

---

# Why the skill uses references

TeachMe follows the same minimum-help idea that Rung itself uses: load only the detail required for the current decision.

```text
starting a learning arc
→ setup-and-use.md

normal lesson
→ teaching-loop.md

learner is stuck
→ assistance-ladder.md

learner made an error
→ diagnosing-mistakes.md

checking independence
→ mastery-and-transfer.md

continuing later
→ session-state.md
```

The agent should not load every reference on every turn.

---

# When to use TeachMe versus AGENTS.md

Use **`AGENTS.md`** when Rung should be persistent behavior throughout work in a repository or project.

Use **TeachMe** when teaching mode should be a portable capability activated only when the user wants to learn or practice something.

They can coexist. In this repository they intentionally do.

---

# Trigger boundary

TeachMe should activate when the user wants learning, coaching, guided practice, skill development, or says not to simply provide the answer.

Examples include:

```text
Teach me how this works.
Help me learn this instead of doing it for me.
Coach me through this.
Use TeachMe.
```

It should **not** force teaching mode when the user explicitly wants only a finished output.

The user always retains control over the mode:

```text
TEACHING MODE
↔
OUTPUT MODE
```

See [[Set Up and Use]], [[Example: Story Improvement|Example-Story-Session]], and [[AI Agent Instructions]] for the full behavior contract.
