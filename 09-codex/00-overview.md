# CodeX Overview

## Что такое CodeX

CodeX — это AI-ассистент для программирования от OpenAI. Поддерживает субагентов для специализированных задач.

## Архитектура

```
┌─────────────────────────────────────┐
│           User Prompt               │
└─────────────┬───────────────────────┘
              ▼
┌─────────────────────────────────────┐
│         CodeX (Main)                │
│  - Planning                         │
│  - Orchestration                    │
│  - Integration                      │
└─────────────┬───────────────────────┘
              ▼
┌─────────────────────────────────────┐
│        Subagents (Specialized)      │
│  - code-reviewer                    │
│  - security-auditor                 │
│  - performance-engineer             │
│  - ...                              │
└─────────────────────────────────────┘
```

## Формат субагента

### TOML Specification

```toml
name = "backend-developer"
description = "Expert in server-side development"
model = "gpt-5.4"
model_reasoning_effort = "high"
sandbox_mode = "workspace-write"

[developer_instructions]
prompt = """
You are a backend development expert.

## Scope
- API design and implementation
- Database operations
- Business logic

## Tools
- read_file
- write_file
- execute

## Output Format
Return code changes as unified diff.
"""

[mcp_servers]
required = ["github", "postgres"]
```

## Model Routing

| Model | Назначение |
|-------|------------|
| `gpt-5.4` | Deep reasoning (архитектура, security) |
| `gpt-5.3-codex-spark` | Fast scanning, synthesis |

## Sandbox Modes

| Mode | Доступ | Назначение |
|------|--------|------------|
| `read-only` | Чтение | Reviewers, auditors |
| `workspace-write` | Чтение/запись | Developers, engineers |

## Хранение агентов

### Global
```bash
~/.codex/agents/
```
Доступны во всех проектах.

### Project-specific
```bash
.codex/agents/
```
Доступны только в текущем проекте. Имеют приоритет над global.

## Установка субагента

```bash
# Global
mkdir -p ~/.codex/agents
cp backend-developer.toml ~/.codex/agents/

# Project-specific
mkdir -p .codex/agents
cp backend-developer.toml .codex/agents/
```

## Использование

```
Пользователь: "@backend-developer Create REST API for users"
→ CodeX создаёт субагента
→ Субагент выполняет задачу
→ Результат возвращается в основной поток
```

## Конфигурация

Файл: `.codex/config.toml`

```toml
[agents]
default_model = "gpt-5.4"
auto_spawn = false  # Не создавать автоматически

[agents.preferences]
prefer_project_agents = true
```

## Источники
- https://github.com/pavelvladimirovich258614-sys/awesome-codex-subagents
- OpenAI Codex Documentation
