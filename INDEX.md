# Prompt Ops Playbook — Index

## 🚀 СТАРТУЙ ЗДЕСЬ (ПЕРВЫМ ДЕЛОМ!)

> ⚠️ **ВАЖНО:** Перед началом работы активируй мастер-промпт!

### 👉 [MASTER_PROMPT.md](MASTER_PROMPT.md) ← НАЖМИ И СКОПИРУЙ

**Что делает мастер-промпт:**
- ✅ AI сам предлагает команды (не нужно думать что спросить)
- ✅ Подключает MCP автоматически (Context7, GitHub и др.)
- ✅ Использует агентов из базы знаний (144+ Agency Agents)
- ✅ Ведёт разработку как опытный Senior Developer
- ✅ Даёт конкретные инструкции что делать дальше

**Как использовать:**
1. Открой [MASTER_PROMPT.md](MASTER_PROMPT.md)
2. Скопируй блок "MASTER PROMPT ACTIVATION"
3. Вставь в начало диалога с AI
4. Опиши свою задачу
5. AI сам всё сделает!

---

## Быстрая навигация

### 01-commands — CLI и команды
- [Claude Code Commands Cheatsheet](01-commands/claude-code-commands-cheatsheet.md) — **50+ команд**: /init, /compact, /diff, /review, CLI flags, hotkeys
- [Slash-команды Claude Code](01-commands/slash-commands.md) — /usage, /chrome, /mcp, /stats, /clear, /compact, /context, /config, /plan, /copy
- [chub CLI](01-commands/chub-cli.md) — Context Hub команды: search, get, annotate, feedback
- [Skills](01-commands/skills.md) — 6 skills для Claude Code: clone, gha, handoff, reddit-fetch, review-claudemd, half-clone

### 02-skills — Навыки и workflow
- [Skill](02-skills/concept-skill.md) — Что такое skill
- [Workflow](02-skills/concept-workflow.md) — Mandatory agentic workflows
- [Subagent-driven Development](02-skills/concept-subagent-driven-development.md) — Делегирование субагентам
- [TDD](02-skills/concept-tdd.md) — RED-GREEN-REFACTOR
- [Brainstorming](02-skills/skill-brainstorming.md) — Socratic design refinement
- [Writing Plans](02-skills/skill-writing-plans.md) — Планирование реализации
- [Systematic Debugging](02-skills/skill-systematic-debugging.md) — 4-фазный debugging
- [Git Worktrees](02-skills/skill-git-worktrees.md) — Параллельные ветки
- [Color Expert](02-skills/skill-color-expert.md) — **Скилл по науке о цвете**: 113 файлов, 286K слов, от Гельмгольца до OKLCH

### 03-mcp — Model Context Protocol
- [Context7 Platform](03-mcp/context7-platform.md) — Актуальная документация для LLM
- [ctx7 CLI](03-mcp/ctx7-cli.md) — Команды: library, docs, skills, setup
- [MCP Server](03-mcp/mcp-server.md) — Интеграция с редакторами
- [MCP Config](03-mcp/mcp-config.md) — Конфигурация для Claude/Cursor/Windsurf
- [Resolve Library ID](03-mcp/tool-resolve-library-id.md) — Tool для поиска Library ID
- [Query Docs](03-mcp/tool-query-docs.md) — Tool для получения документации

### 04-subagents — Субагенты
- [Agent Loop](04-subagents/agent-loop.md) — Минимальный цикл агента
- [Tools and Function Calling](04-subagents/tools-and-function-calling.md) — Вызов функций
- [Todo and Planning](04-subagents/todo-and-planning.md) — Система планирования
- [Subagents and Delegation](04-subagents/subagents-and-delegation.md) — Делегирование
- [Skills System](04-subagents/skills-system.md) — On-demand knowledge
- [Context Compression](04-subagents/context-compression.md) — Сжатие контекста
- [Task System](04-subagents/task-system.md) — Фоновые задачи
- [Agent Teams](04-subagents/agent-teams.md) — Команды агентов
- [Agent Harness](04-subagents/agent-harness.md) — Ready-to-run агент
- [Filesystem Backend](04-subagents/filesystem-backend.md) — Работа с файлами
- [Context Management](04-subagents/context-management.md) — Авто-суммаризация

### 09-codex — CodeX субагенты
- [Overview](09-codex/00-overview.md) — Обзор CodeX экосистемы
- [Subagents Catalog](09-codex/01-subagents-catalog.md) — 136+ субагентов по категориям
- [Subagent Spec Template](09-codex/02-subagent-spec-template.md) — Шаблон TOML спецификации
- [Workflows](09-codex/03-workflows.md) — Паттерны workflow
- [Integration Notes](09-codex/04-integration-notes.md) — Интеграция с Codex
- [Troubleshooting](09-codex/05-troubleshooting.md) — Типичные проблемы

## Learning Paths

### Claude Code Basics
1. [Slash-команды](01-commands/slash-commands.md)
2. [Skills](01-commands/skills.md)
3. [Troubleshooting](05-troubleshooting/)

### MCP Integration
1. [Context7 Platform](03-mcp/context7-platform.md)
2. [MCP Server](03-mcp/mcp-server.md)
3. [Subagents](04-subagents/)

### Subagent Development
1. [Skills](02-skills/)
2. [Subagents](04-subagents/)
3. [CodeX Catalog](09-codex/01-subagents-catalog.md)

### 07-registry — Реестр инструментов
- [Agency Agents](07-registry/agency-agents.md) — 144+ специализированных AI-агента от msitarzewski

## Реестр инструментов

| Инструмент | Назначение | Раздел |
|------------|------------|--------|
| Claude Code | AI ассистент для кодирования | 01-commands |
| Context7 | Актуальная документация | 03-mcp |
| chub | CLI для документации | 01-commands |
| Deep Agents | Agent harness | 04-subagents |
| Page Agent | In-page GUI agent | 04-subagents |
| Superpowers | Skills framework | 02-skills |
| Supersearch | BM25 поиск | 06-glossary |
| Agency Agents | 144+ AI агентов с личностями | 07-registry |

## Теги

- #cli — CLI команды
- #skills — Навыки и workflow
- #mcp — Model Context Protocol
- #subagents — Субагенты
- #codex — CodeX
- #troubleshooting — Решение проблем
