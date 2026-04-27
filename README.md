# User Research AI Assistant

This repository is an AI-driven workspace for conducting structured user research and stakeholder analysis. Users interact with an AI agent (GitHub Copilot Chat, Claude, OpenAI Codex, or any other LLM) directly from the chat window. The agent uses **skills** — self-contained prompt definitions — to guide conversations and produce research documents that are saved in the `docs/` directory.

---

## How It Works

1. **Open the chat window** in your preferred AI tool (GitHub Copilot Chat, Claude, ChatGPT, etc.).
2. **Invoke a skill** by describing what you want to do (e.g. *"Run a stakeholder analysis for our mobile banking project"*).
3. **The agent asks you questions** based on the skill's prompt definition.
4. **A finished document** is written into the `docs/` directory when the conversation is complete.

Because skills are defined as plain Markdown files, they are tool-agnostic and work with any AI system that can read the repository.

---

## Repository Structure

```
user-research/
├── README.md                          # This file
├── docs/                              # Output: generated research documents
│   └── README.md
└── skills/                            # Skill definitions (tool-agnostic)
    ├── README.md
    └── stakeholder-analysis/          # Stakeholder Analysis skill
        ├── README.md                  # How to invoke and use the skill
        ├── skill.md                   # Prompt definition (loaded by the AI agent)
        └── output-template.md         # Document template the agent fills in
```

---

## Available Skills

| Skill | Description | Output |
|-------|-------------|--------|
| [Stakeholder Analysis](skills/stakeholder-analysis/README.md) | Identifies stakeholders, maps their interests and influence, and produces a stakeholder register | `docs/stakeholder-analysis-<project>.md` |

---

## Adding New Skills

1. Create a new subdirectory under `skills/`.
2. Add `skill.md` (prompt definition), `output-template.md` (document template), and `README.md` (usage guide).
3. Register the skill in the table above.

See [skills/README.md](skills/README.md) for the full skill authoring guide.

---

## GitHub Copilot Chat Quick Start

Open Copilot Chat in VS Code and type:

```
Run the stakeholder analysis skill for my project.
```

Copilot will read `.github/copilot-instructions.md` and the relevant skill files, then guide you through the analysis interactively.
