# Rung as a Codex and Claude Skill

Rung is packaged as an **Agent Skill** so it can be used as a portable teaching mode instead of requiring the entire Rung repository to govern every agent interaction.

The skill does **not** replace `AGENTS.md`, the README, or this wiki. Those pieces serve different purposes:

| Component | Role |
| --- | --- |
| `README.md` | Human quickstart and system overview |
| Wiki | Detailed method, research, explanations, and sources |
| `AGENTS.md` | Persistent Rung operating contract when working inside this repository |
| `skills/rung-teaching/` | Canonical portable Agent Skill |
| `.agents/skills/rung-teaching/` | Codex-compatible mirror |
| `.claude/skills/rung-teaching/` | Claude-compatible mirror |
| `prompts/RUNG_AGENT_INSTRUCTIONS.md` | Fallback when Skills/repository instructions are unavailable |

---

# Canonical skill

The only skill package that should be edited directly is:

```text
skills/rung-teaching/
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

This keeps the skill compact enough for discovery while preserving the detailed Rung behavior required for reliable teaching.

---

# Codex

The repository exposes the skill to Codex at:

```text
.agents/skills/rung-teaching/
```

The complete directory is a generated mirror of the canonical package.

To use Rung explicitly, ask Codex to use the `rung-teaching` skill while teaching a subject or skill, for example:

```text
Use the rung-teaching skill to teach me how to diagnose weak SQL joins.
```

The skill description is also written so teaching/coaching requests can be recognized as appropriate triggers when skill discovery is available.

---

# Claude

The repository exposes the skill to Claude at:

```text
.claude/skills/rung-teaching/
```

The complete directory is also a generated mirror of the canonical package.

Use it explicitly with the Rung skill when needed, for example:

```text
/rung-teaching Teach me how to evaluate the evidence behind a historical claim.
```

Or ask Claude normally to teach/coach you when automatic skill selection is available.

---

# Installing Rung in another project

You do not need to copy the entire Rung_Teaching repository.

## For Codex

Copy the canonical package into the target project as:

```text
.agents/skills/rung-teaching/
```

## For Claude

Copy the canonical package into the target project as:

```text
.claude/skills/rung-teaching/
```

If a project uses both systems, install the same canonical package in both locations.

The package is self-contained for normal runtime behavior. The main Rung wiki remains useful when a human or agent needs deeper explanation, the learning-science basis, MAPS adaptations, or source citations.

---

# Automatic synchronization

Do **not** manually maintain the Codex and Claude mirrors.

The GitHub Action:

```text
.github/workflows/sync-rung-skills.yml
```

copies:

```text
skills/rung-teaching/
```

into both:

```text
.agents/skills/rung-teaching/
.claude/skills/rung-teaching/
```

whenever the canonical package changes on `main`.

This means there is one runtime source of truth rather than three versions that can drift apart.

---

# Why the skill uses references

The skill follows the same minimum-help idea that Rung itself uses: load only the detail required for the current decision.

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

# When to use the skill versus AGENTS.md

Use **`AGENTS.md`** when Rung should be persistent behavior throughout work in a repository or project.

Use the **Rung skill** when teaching mode should be a portable capability that can be activated only when the user wants to learn or practice something.

They can coexist. In this repository they intentionally do.

---

# Trigger boundary

Rung should activate when the user wants learning, coaching, guided practice, skill development, or says not to simply provide the answer.

It should **not** force teaching mode when the user explicitly wants only a finished output.

The user always retains control over the mode:

```text
TEACHING MODE
↔
OUTPUT MODE
```

See [[Set Up and Use]] and [[AI Agent Instructions]] for the full behavior contract.
