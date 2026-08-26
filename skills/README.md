# TeachMe Agent Skill

`skills/teachme/` is the canonical portable **TeachMe** Agent Skill. TeachMe is the user-facing skill; it uses the **Rung Teaching System** as its teaching method.

Edit the canonical package only:

```text
skills/teachme/
```

Do not manually edit these generated mirrors:

```text
.agents/skills/teachme/   # Codex
.claude/skills/teachme/   # Claude
```

`.github/workflows/sync-rung-skills.yml` mirrors the canonical package into both locations whenever the skill changes on `main`.

The naming distinction is intentional:

- **TeachMe** — the AI skill users invoke.
- **Rung** — the teaching methodology TeachMe follows.

The skill is intentionally smaller than the full Rung documentation. `SKILL.md` contains runtime behavior; `references/` contains operational detail loaded only when relevant. The repository wiki remains the explanatory and research layer.

See the wiki page **TeachMe Agent Skill** for installation and usage instructions:

https://github.com/BigCatMellow/Rung_Teaching/wiki/Agent-Skills
