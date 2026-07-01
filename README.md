# ai-feedback-integration

Codex skill that adds a governed post-run feedback and improvement loop to other AI skills, with wrappers for Codex, Claude Cowork, and Copilot Cowork.

This repository publishes `ai-feedback-integration` as a portable agent skill. The source skill may come from Codex, GitHub Copilot/Copilot Cowork, Claude Cowork, or another agent-skill environment. A root `SKILL.md` is provided for tools that install from the repository root, and wrapper paths are included for Codex, GitHub Copilot/Copilot Cowork, Claude Cowork, and generic agent-skill environments.

## Install for Codex

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/breaknout/ai-feedback-integration.git "${CODEX_HOME:-$HOME/.codex}/skills/ai-feedback-integration"
```

Then ask Codex:

```text
Use $ai-feedback-integration ...
```

## Install for GitHub Copilot / Copilot Cowork

This repository includes conventional skill paths:

```text
.github/skills/ai-feedback-integration/
.agents/skills/ai-feedback-integration/
skills/ai-feedback-integration/
```

If using GitHub's skill installer:

```bash
gh extension install github/gh-copilot
gh skill install breaknout/ai-feedback-integration ai-feedback-integration
```

For a project-local install, copy `.github/skills/ai-feedback-integration/` into the target repository.

## Install for Claude Cowork / Claude-Style Agents

Use:

```text
.claude/skills/ai-feedback-integration/
```

Copy that folder into the Claude Cowork project or user skill location used by your environment.

## Generic Agent Skill

Use:

```text
.agents/skills/ai-feedback-integration/
```

## Contents

- `SKILL.md` - root Codex-compatible skill instructions
- `agents/openai.yaml` - Codex UI metadata when present
- `scripts/` - bundled executable helpers when present
- `.github/skills/ai-feedback-integration/` - GitHub Copilot/Copilot Cowork skill path
- `.claude/skills/ai-feedback-integration/` - Claude Cowork/Claude-style skill path
- `.agents/skills/ai-feedback-integration/` - generic agent skill path

## License

MIT License unless replaced by the publisher.
