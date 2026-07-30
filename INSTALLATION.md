# Installation

Build with LumynQ is distributed as both an OpenAI-compatible plugin bundle and a portable Agent Skill. Use the versioned ZIP from the [latest GitHub Release](https://github.com/quenaF/build-with-lumynq/releases/latest), not GitHub’s automatically generated source archive, when possible.

## Before installing

Review `skills/build-with-lumynq/SKILL.md` and its references. Skills are instructions an agent follows; install only versions you trust.

Keep the entire `build-with-lumynq` Skill folder together:

```text
build-with-lumynq/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── experience-map.md
    ├── integration-and-domain-packs.md
    └── review-rubric.md
```

## ChatGPT and Codex

The repository includes `.codex-plugin/plugin.json`, so the full release ZIP is the OpenAI plugin bundle.

### ChatGPT Work and Codex in ChatGPT

If your account or workspace supports installing local or private plugins:

1. Download `build-with-lumynq-v0.1.0.zip` from the GitHub Release.
2. Open **Plugins** in ChatGPT.
3. Choose the available option to add or install a plugin package.
4. Select the downloaded ZIP and review the requested contents.
5. Start a new chat and ask: `Use Build with LumynQ to review this experience.`

Plugin installation controls vary by plan and workspace policy. If local package installation is unavailable, use the repository Skill layout with a supported Codex client or ask a workspace administrator to make the plugin available.

### Codex local or repository Skill

For a personal Skill, copy the Skill folder to:

```text
$HOME/.agents/skills/build-with-lumynq/
```

For a Skill shared with everyone working in one repository, copy it to:

```text
your-project/.agents/skills/build-with-lumynq/
```

Then open the project in Codex and invoke `Build with LumynQ` by name or ask for a task that matches its description.

## Replit Agent

Replit project Skills live under `/.agents/skills`.

1. Download and extract the release.
2. Copy `skills/build-with-lumynq/` into your Replit project as:

```text
.agents/skills/build-with-lumynq/
```

3. Confirm `.agents/skills/build-with-lumynq/SKILL.md` exists.
4. Ask Replit Agent: `Use Build with LumynQ to review this project’s onboarding flow.`

You can also use Replit’s Skills interface when it supports importing a Skill folder. Installing this GitHub package manually does not imply that it has been reviewed or listed by Replit.

## Claude Code

Claude Code recognizes Agent Skills through `SKILL.md`.

For one project, copy the Skill folder to:

```text
your-project/.claude/skills/build-with-lumynq/
```

For your user account, copy it to:

```text
$HOME/.claude/skills/build-with-lumynq/
```

Start Claude Code in the project, then invoke:

```text
/build-with-lumynq
```

or ask Claude to use Build with LumynQ in natural language.

## Other compatible agents

For agents that implement the Agent Skills format:

1. Locate the product’s documented Skills directory.
2. Copy the complete `skills/build-with-lumynq/` folder into it.
3. Preserve `SKILL.md`, `agents/`, and `references/` at their relative paths.
4. Confirm the agent can discover the Skill’s `name` and `description` frontmatter.
5. Run a small read-only task before granting write access.

If an agent does not support Skills, attach `SKILL.md` and only the reference needed for the current task as project instructions. That fallback may not provide automatic triggering or progressive reference loading.

## Verify the installation

Use this bounded prompt:

```text
Use Build with LumynQ to review a fictional application confirmation that says only “We’ll be in touch.” Do not edit anything. Label evidence correctly, explain the human consequence, and provide one testable required change.
```

A conforming response should not invent live evidence, diagnose the user’s emotions, or solve the problem with warmer copy alone.

## Update or remove

To update, replace the installed folder with the folder from a newer versioned release and review the release notes first.

To remove, delete only the installed `build-with-lumynq` folder from the relevant Skills directory. Removing it does not change projects previously created with its guidance.

## Official references

- [OpenAI: Build Skills](https://developers.openai.com/codex/build-skills)
- [OpenAI: Skills and Plugins](https://developers.openai.com/codex/skills-and-plugins)
- [Replit: Agent Skills](https://docs.replit.com/features/agent/skills)
- [Anthropic: Extend Claude with Skills](https://docs.anthropic.com/en/docs/claude-code/skills)
