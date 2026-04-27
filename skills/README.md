# Skills

Skills are self-contained prompt definitions that teach the AI agent how to perform a specific research activity. They are plain Markdown files, so they work with **any** AI tool — GitHub Copilot Chat, Claude, OpenAI ChatGPT/Codex, or any other LLM.

---

## How a Skill Is Structured

```
skills/
└── <skill-name>/
    ├── README.md           # Human-readable guide: when and how to invoke the skill
    ├── skill.md            # Prompt definition loaded by the AI agent
    └── output-template.md  # Markdown template the agent fills in and saves to docs/
```

### `skill.md`

Defines the agent's behaviour for this skill:
- **Role** – the persona the agent should adopt
- **Goal** – what the skill produces
- **Process** – the step-by-step questions / conversation flow
- **Output instructions** – how to write the finished document

### `output-template.md`

A Markdown template with placeholder sections. The agent fills this in with information gathered during the conversation and writes the result to `docs/`.

---

## Available Skills

| Skill | Directory |
|-------|-----------|
| Stakeholder Analysis | [stakeholder-analysis/](stakeholder-analysis/) |

---

## Authoring a New Skill

1. Copy an existing skill directory as a starting point.
2. Update `skill.md` with the new role, goal, process, and output instructions.
3. Update `output-template.md` to match the desired document structure.
4. Update `README.md` with invocation instructions.
5. Register the skill in [the top-level README](../README.md).
6. Register the skill in `.github/copilot-instructions.md` so GitHub Copilot Chat can discover it.
