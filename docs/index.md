---
title: "Quick Start"
description: "Welcome to your new documentation site."
---

# Quick Start Your Docs 🚀

This is the home page of your new **docmd** project. You're currently viewing `docs/index.md` — edit it, and your site updates.

## Run the dev server

```bash
npx @docmd/core dev
```

Open `http://localhost:3000` — the page auto-reloads as you edit.

## Build for production

```bash
npx @docmd/core build
```

Output goes to `site/`. Deploy that folder anywhere that serves static files.

## Project structure

```text
.
├── docs/                  # Your markdown content
│   └── index.md           # You are here
├── assets/                # Custom CSS, JS, and images
├── docmd.config.json      # Site configuration
└── package.json           # Node dependencies + scripts
```

## Features

### 1. Smart containers

```markdown
::: callout tip "Did you know?"
You can nest containers, add titles, and use icons.
:::

::: card "Flexible" icon:layout-grid
Organise content with cards.

[View the docs →](https://docs.docmd.io){.docmd-button}
:::
```

Renders as a styled callout and a card with a button.

### 2. Tabs and code

````markdown
::: tabs
== tab "JavaScript" icon:braces
```javascript
console.log('Hello World');
```

== tab "Python" icon:code
```python
print('Hello World')
```
:::
````

### 3. Built-in plugins

docmd ships with these plugins enabled by default — no install needed:

- **AI Assistant** — interactive documentation chat (100% free with BYOK or docmd Cloud)
- **Search** — full-text + semantic search (optional)
- **Sitemap** + **SEO** meta tags
- **LLMs context** — `llms.txt` and `llms.json` for AI agents
- **OKF** — Open Knowledge Format bundle at `site/okf/`
- **Mermaid** diagrams
- **Git** last-modified timestamps
- **Math** (KaTeX) — enable with `docmd add math`

See the [full plugin list](https://docs.docmd.io/plugins/usage/).

## Next steps

- **[Install docmd](https://docs.docmd.io/getting-started/installation/)**
- **[Configure your site](https://docs.docmd.io/configuration/overview/)**
- **[Browse templates](https://docs.docmd.io/theming/templates/)**
- **[Deploy to production](https://docs.docmd.io/deployment/)**
- **[GitHub repo](https://github.com/docmd-io/docmd/)**

Happy documenting! 🎉