# AGENTS.md

This repository is a knowledge base and operational playbook for:
– commands;
– skills;
– MCP;
– subagents;
– diagnostics;
– prompt workflows.

## Mission
Work with this repository as a structured source of truth.
Do not treat it as random notes.
Use its files as operational guidance.

## Primary files
Always start from:
1. `PLAYBOOK.md`
2. `INDEX.md`

Then move to the relevant section:
- `01-commands/commands-catalog.md`
- `02-skills/skills-setup.md`
- `03-mcp/mcp-configs-patterns.md`
- `04-subagents/subagents-roles-bus.md`
- `05-troubleshooting/faq-diagnostics.md`
- `06-glossary/glossary.md`
- `07-registry/skills-and-mcp-registry.md`
- `08-prompts/`

## Rules
- Prefer repository guidance over guesses.
- Do not invent commands, configs or workflows that are not grounded in the repo.
- If context is missing, say which file is needed.
- For MCP or skill selection, check `07-registry/skills-and-mcp-registry.md` first.
- For troubleshooting, use `05-troubleshooting/faq-diagnostics.md`.
- For large tasks, consider subagent design from `04-subagents/subagents-roles-bus.md`.
- Keep answers practical and actionable.

## Default answer structure
A. Conclusion
B. Steps
C. Example
D. Errors and validation
E. Missing context

## When editing this repository
- Preserve the modular structure.
- Prefer adding new cards instead of long unstructured text.
- Use IDs consistently.
- Link related sections when adding new content.
- Keep docs reusable across ChatGPT, Cursor and Claude.

## If asked to choose a tool
First answer:
1. Is an external tool needed at all?
2. Which smallest sufficient option fits?
3. How to validate it with a minimal test case?
