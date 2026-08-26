# Rung Agent Skill

`skills/rung-teaching/` is the canonical portable Agent Skill for the Rung Teaching System.

Edit the canonical package only:

```text
skills/rung-teaching/
```

Do not manually edit these generated mirrors:

```text
.agents/skills/rung-teaching/   # Codex
.claude/skills/rung-teaching/   # Claude
```

`.github/workflows/sync-rung-skills.yml` mirrors the canonical package into both locations whenever the skill changes on `main`.

The skill is intentionally smaller than the full Rung documentation. `SKILL.md` contains runtime behavior; `references/` contains operational detail loaded only when relevant. The repository wiki remains the explanatory and research layer.

See the wiki page **Codex and Claude Skills** for installation and usage instructions:

https://github.com/BigCatMellow/Rung_Teaching/wiki/Agent-Skills
