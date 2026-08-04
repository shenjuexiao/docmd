---
title: "Agent Skills"
description: "Teach AI coding agents to work with docmd projects"
---

# Agent Skills

docmd ships a **modular skill set** for AI coding agents (Claude Code, Cursor, Windsurf, Copilot, etc.). The skills teach your agent the `docmd` CLI, configuration, plugin system, and the `docmd mcp` server — so it can build, configure, validate, and deploy sites for you.

## What gets installed

The [`docmd-skills`](https://www.npmjs.com/package/docmd-skills) npm package contains three skill modules:

| Skill | When your agent loads it |
|---|---|
| **`docmd-skills`** | A docmd **site operator**. Knows the `npx @docmd/core` CLI, `docmd.config.json`, plugins, themes, deployment, and the `docmd mcp` server. |
| **`docmd-dev`** | A docmd **framework contributor**. Knows the monorepo layout, how to author plugins and templates, the JS / Rust engine loaders, and the public Node API (`EngineLoader`, `createActionDispatcher`, `TemplateSlot`). |
| **`docmd-writer`** | A **multi-language documentation writer**. Drafts and reviews prose in any language, with SEO awareness and docmd's markdown conventions (containers, frontmatter, file-title rule). |

## Install

Pick the directory your agent reads skills from and run **one** command:

### Claude Code

```bash
npx docmd-skills ~/.claude/skills
```

### Cursor

```bash
npx docmd-skills ~/.cursor/skills
```

### Project-local (any agent)

```bash
npx docmd-skills ./.skills
```

After install, the `docmd-skills`, `docmd-dev`, and `docmd-writer` modules are available to your agent.

Run `npx docmd-skills --help` for the full list of commands.

## How it works at runtime

Once installed, your agent automatically loads the right skill based on the files in scope:

- When you ask "add a plugin to my docmd site" → `docmd-skills` loads
- When you ask "add a new template" inside the cloned `docmd-io/docmd` monorepo → `docmd-dev` loads
- When you ask "write the intro for my new docs" → `docmd-writer` loads

## Update or remove

The CLI is idempotent — running it again updates the skills to latest:

```bash
npx docmd-skills <dir>          # updates all three
npx docmd-skills remove <dir>   # deletes all three
```
