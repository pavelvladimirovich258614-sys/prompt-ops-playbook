# Prompt Ops Playbook

> Модульная база знаний для AI-агентов: команды, навыки, MCP, субагенты и промпты.

[![GitHub](https://img.shields.io/badge/GitHub-Repo-blue)](https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## Что это?

Этот репозиторий — **энциклопедия** для работы с AI-агентами:
- **144+ Agency Agents** — специализированные агенты с личностями (Claude, Cursor, Aider)
- **136+ CodeX субагентов** — готовые специалисты для CodeX
- **Claude Code команды** — slash-команды и skills
- **MCP интеграции** — подключение внешних инструментов
- **Workflow шаблоны** — проверенные паттерны работы
- **Subagent паттерны** — делегирование и оркестрация

---

## Быстрый старт (30 секунд)

### Вариант 1: Найти нужное
1. Откройте **[INDEX.md](INDEX.md)** — там вся навигация
2. Найдите раздел по задаче
3. Перейдите по ссылке

### Вариант 2: Спросить нейросеть
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/INDEX.md

Мне нужно [ВАША ЗАДАЧА]. Какой раздел мне смотреть?
```

### Вариант 3: Пошаговое руководство
👉 **[USAGE.md](USAGE.md)** — подробные инструкции с примерами промптов

### Вариант 4: Мастер-промпт (рекомендуется!)
👉 **[MASTER_PROMPT.md](MASTER_PROMPT.md)** — активируй режим Senior AI Developer

**Как использовать:**
1. Открой [MASTER_PROMPT.md](MASTER_PROMPT.md)
2. Скопируй блок "MASTER PROMPT ACTIVATION"
3. Вставь в начало диалога с AI
4. AI сам будет предлагать команды, подключать MCP, использовать агентов

---

## Структура репозитория

```
📁 prompt-ops-playbook/
│
├── 📄 README.md          ← Вы здесь
├── 📄 MASTER_PROMPT.md   ← 🚀 СТАРТУЙ ЗДЕСЬ! Мастер-промпт
├── 📄 INDEX.md           ← Навигация по всем разделам
├── 📄 USAGE.md           ← Подробное руководство с примерами
├── 📄 PLAYBOOK.md        ← Prompt Ops методология
├── 📄 AGENTS.md          ← Архитектура агентов
├── 📄 CHANGELOG.md       ← История изменений
├── 📄 CONTRIBUTING.md    ← Как внести вклад
└── 📄 LICENSE            ← MIT License
│
├── 📁 01-commands/       ← CLI команды, slash-команды
├── 📁 02-skills/         ← Навыки, workflow, паттерны
├── 📁 03-mcp/            ← Model Context Protocol
├── 📁 04-subagents/      ← Субагенты, оркестрация
├── 📁 05-troubleshooting/← Решение проблем (TODO)
├── 📁 06-glossary/       ← Глоссарий терминов (TODO)
├── 📁 07-registry/       ← Реестр инструментов (Agency Agents — 144+ агентов!)
├── 📁 08-prompts/        ← Промпт-шаблоны (TODO)
└── 📁 09-codex/          ← CodeX субагенты (136+ агентов!)
```

---

## Примеры использования

### Пример 1: Нужен skill для Claude Code
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-skill.md

Создай skill для code review Python:
1. Проверяй типы
2. Ищи баги
3. Проверяй стиль PEP8
```

### Пример 2: Нужен CodeX субагент
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/01-subagents-catalog.md

Найди мне субагента для backend разработки на Python.
```

### Пример 3: Нужен Agency Agent (Claude/Cursor/Aider)
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/07-registry/agency-agents.md

Установи Agency Agents и активируй Frontend Developer для создания React компонента.
```

### Пример 4: Нужен workflow для команды
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-workflow.md

Внедри workflow "Subagent-driven Development" для моей команды.
```

### Пример 5: Нужен agent loop
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/agent-loop.md

Создай минимальный агент на Python с инструментами:
- read_file
- write_file
- execute (bash)
```

### Пример 6: Нужна команда агентов для проекта
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/07-registry/agency-agents.md

Собери команду агентов для разработки MVP:
- Frontend Developer (React)
- Backend Architect (Python/FastAPI)
- DevOps Automator (Docker/K8s)
- Code Reviewer (QA)
```

---

## Learning Paths (Пути обучения)

### Путь 1: Claude Code Basics ⏱️ 2-4 часа
**Для:** Новичков в Claude Code

**Что изучить:**
1. [Slash-команды](01-commands/slash-commands.md)
2. [Skills](01-commands/skills.md)
3. [Concept: Skill](02-skills/concept-skill.md)

**Промпт для нейросети:**
```
Прочитай последовательно:
1. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/slash-commands.md
2. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/skills.md
3. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-skill.md

Создай summary и покажи как применить.
```

### Путь 2: MCP Integration ⏱️ 3-5 часов
**Для:** Интеграторов MCP

**Что изучить:**
1. [Context7 Platform](03-mcp/context7-platform.md)
2. [ctx7 CLI](03-mcp/ctx7-cli.md)
3. [Agent Loop](04-subagents/agent-loop.md)

**Промпт для нейросети:**
```
Прочитай последовательно:
1. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/context7-platform.md
2. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/ctx7-cli.md

Настрой Context7 для моего проекта на React + TypeScript.
```

### Путь 3: Subagent Development ⏱️ 4-6 часов
**Для:** Разработчиков субагентов

**Что изучить:**
1. [Concept: Workflow](02-skills/concept-workflow.md)
2. [Subagents and Delegation](04-subagents/subagents-and-delegation.md)
3. [CodeX Catalog](09-codex/01-subagents-catalog.md)

**Промпт для нейросети:**
```
Прочитай последовательно:
1. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-workflow.md
2. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/subagents-and-delegation.md
3. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/01-subagents-catalog.md

Создай workflow для code review с 3 субагентами.
```

### Путь 4: Agency Agents Mastery ⏱️ 3-5 часов
**Для:** Тех, кто хочет использовать готовых агентов с личностями

**Что изучить:**
1. [Agency Agents Overview](07-registry/agency-agents.md)
2. Установка для вашего редактора (Claude/Cursor/Aider)
3. Выбор агентов под задачи

**Промпт для нейросети:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/07-registry/agency-agents.md

Установи Agency Agents для [Claude Code/Cursor/Aider] и покажи как использовать Frontend Developer.
```

### Путь 5: Full Stack ⏱️ 8-12 часов
**Для:** Тимлидов и архитекторов

**Что изучить:** Все разделы последовательно

**Промпт для нейросети:**
```
Прочитай все разделы:
https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook

Создай комплексное решение для моей команды:
- Настройка Claude Code
- Настройка MCP
- Workflow с субагентами
- Agency Agents интеграция
```

---

## Разделы подробно

### 01-commands — CLI и команды
**Когда использовать:** Нужна быстрая справка по командам

**Что внутри:**
- Slash-команды Claude Code (/usage, /chrome, /mcp, /stats, /clear, /compact, /context, /config, /plan, /copy)
- DX Plugin команды (/dx:clone, /dx:handoff, /dx:gha)
- Skills для Claude Code (clone, gha, handoff, reddit-fetch, review-claudemd)
- chub CLI (search, get, annotate, feedback)

**Пример промпта:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/slash-commands.md

Как использовать /plan для разработки новой фичи?
```

### 02-skills — Навыки и workflow
**Когда использовать:** Создаёте новый skill или workflow

**Что внутри:**
- Concept: Skill — что такое skill и как его создать
- Concept: Workflow — 7 core workflows
- Subagent-driven Development — делегирование субагентам
- TDD — RED-GREEN-REFACTOR цикл
- Brainstorming — Socratic design refinement
- Writing Plans — планирование реализации
- Systematic Debugging — 4-фазный debugging
- Git Worktrees — параллельные ветки

**Пример промпта:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-skill.md

Создай skill для [ВАША ЗАДАЧА].
```

### 03-mcp — Model Context Protocol
**Когда использовать:** Интеграция с MCP серверами

**Что внутри:**
- Context7 Platform — актуальная документация для LLM
- ctx7 CLI — команды library, docs, skills, setup
- MCP Server — интеграция с редакторами
- MCP Config — настройка для Cursor, Claude, Windsurf, VS Code
- Tools: resolve-library-id, query-docs

**Пример промпта:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/context7-platform.md

Настрой Context7 MCP для Cursor.
```

### 04-subagents — Субагенты
**Когда использовать:** Делегирование задач агентам

**Что внутри:**
- Agent Loop — минимальный цикл агента
- Tools and Function Calling — вызов функций
- Todo and Planning — система планирования
- Subagents and Delegation — делегирование
- Skills System — on-demand knowledge
- Context Compression — сжатие контекста
- Task System — фоновые задачи
- Agent Teams — команды агентов
- Agent Harness — ready-to-run агент
- Filesystem Backend — работа с файлами
- Context Management — авто-суммаризация

**Пример промпта:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/agent-loop.md

Создай агента на Python с инструментами read_file, write_file, execute.
```

### 07-registry — Реестр инструментов
**Когда использовать:** Выбираете инструменты для проекта

**Что внутри:**
- Agency Agents — **144+ специализированных AI-агента** с личностями
  - 12 дивизий (Engineering, Design, Sales, Marketing, и др.)
  - Поддержка Claude Code, Cursor, Aider, Copilot, Gemini CLI
  - Готовые workflow и метрики успеха

**Пример промпта:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/07-registry/agency-agents.md

Собери команду агентов для разработки MVP:
- Frontend Developer (React)
- Backend Architect (Python)
- DevOps Automator
```

### 09-codex — CodeX субагенты
**Когда использовать:** Работа с Codex

**Что внутри:**
- 00-overview — обзор CodeX экосистемы
- 01-subagents-catalog — **136+ субагентов** по 10 категориям
- 02-subagent-spec-template — шаблон TOML спецификации
- 03-workflows — паттерны workflow
- 04-integration-notes — заметки по интеграции
- 05-troubleshooting — типичные проблемы

**Пример промпта:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/01-subagents-catalog.md

Найди субагента для backend разработки на Python.
```

---

## Источники

- [awesome-codex-subagents](https://github.com/pavelvladimirovich258614-sys/awesome-codex-subagents)
- [claude-code-tips](https://github.com/ykdojo/claude-code-tips)
- [context7](https://github.com/upstash/context7)
- [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)
- [superpowers](https://github.com/obra/superpowers)
- [deepagents](https://github.com/langchain-ai/deepagents)
- [page-agent](https://github.com/alibaba/page-agent)
- [context-hub](https://github.com/andrewyng/context-hub)
- [supersearch](https://github.com/anish-palakurthi/supersearch)
- [agency-agents](https://github.com/msitarzewski/agency-agents)

---

## Статистика

- **20 файлов** документации
- **144+ Agency Agents** с личностями
- **136+ CodeX субагентов** в каталоге
- **10 репозиториев** разобрано
- **5 learning paths** для разных уровней

---

## Лицензия

MIT License — см. [LICENSE](LICENSE)

---

## Начните прямо сейчас

👉 **[INDEX.md](INDEX.md)** — полная навигация

👉 **[USAGE.md](USAGE.md)** — подробное руководство с примерами промптов

👉 **[09-codex/01-subagents-catalog.md](09-codex/01-subagents-catalog.md)** — 136+ готовых агентов
