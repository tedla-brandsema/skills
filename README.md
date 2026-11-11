# Governor v3

Governor is a conventional, prompt-driven Agent Skill for autonomous engineering delivery within the invoking user's explicit authority.

- [Skill instructions](governor/SKILL.md)
- [Canonical Project Governor Prompt v3](governor/docs/project-governor-prompt-v3.md), preserved verbatim from the owner's source

Invoke `$governor` in Codex or `/governor` in Claude Code with the repository, requested outcome, scope and exclusions, delivery boundary, and exact Git authority. The prompt's **Immediate task and authority** section is a template; its placeholders grant no permissions. Missing Git authority means no branch creation or switching, commits, pushes, or main integration.

The skill uses the agent's available tools and the target repository's own checks. It requires no Governor executable, workflow engine, dashboard, observation database, or qualification framework.

## Local installations

The verified WSL installations are symlinks to this checkout's `governor/` directory:

- Codex: `/home/developer/.agents/skills/governor`
- Claude Code: `/home/developer/.claude/skills/governor`

Keep one Governor installation in each tool's discovery paths. Reuse these links when the checkout stays at `/home/developer/projects/misc/skillz`; do not add competing copies. Start a fresh conversation after replacement to avoid carrying the previous instructions in session context.

## Archived implementation

`main` starts a new history containing only this README, the skill, and the canonical prompt. The retired coded implementation and its accepted history remain on `archive/governor-coded-2026-11-11` at `dfb4afe0b4b82e9c9148783e81bcb99058caa56d`. Nothing from its runtime infrastructure is required by Governor v3.
