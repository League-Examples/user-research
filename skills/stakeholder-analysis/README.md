# Stakeholder Analysis Skill

The **Stakeholder Analysis** skill guides the AI agent through an interactive conversation to identify everyone who has an interest in — or influence over — a project, then produces a structured stakeholder register in `docs/`.

---

## When to Use This Skill

Use this skill at the **start of any project** before writing requirements, designing personas, or planning workshops. It answers:

- Who are the people and organisations affected by this project?
- How much influence does each stakeholder have?
- What does each stakeholder want or need?
- Where are the conflicts or alignment gaps?

---

## How to Invoke the Skill

### GitHub Copilot Chat (VS Code)

```
Run the stakeholder analysis skill for [your project name].
```

### Claude

Paste the contents of `skill.md` as a system prompt, then type:

```
Let's begin. The project is: [your project name].
```

### OpenAI ChatGPT / Codex

Paste the contents of `skill.md` into the system prompt (or the first user message), then type:

```
Start the stakeholder analysis for: [your project name].
```

### Any Other LLM

1. Open `skill.md` and copy its full text.
2. Paste it as the opening instruction to the model.
3. Follow the agent's questions to complete the analysis.

---

## Output

When the session is complete the agent writes (or asks you to save):

```
docs/stakeholder-analysis-<project-slug>.md
```

The document structure follows [output-template.md](output-template.md).

---

## Example Session Excerpt

```
Agent: What is the name of the project?
You:   Mobile Banking App Redesign

Agent: Who are the primary users of the system — the people who will interact
       with it directly?
You:   Retail banking customers aged 18–65, and bank staff (tellers, advisors)

Agent: Who sponsors or owns the project inside the organisation?
You:   The Digital Transformation Director and the Retail Banking VP
...
```
