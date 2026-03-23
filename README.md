# Prompt Ops Playbook

> Модульная база знаний для агентов: команды, навыки, MCP, субагенты и промпты.

## Быстрый старт

```bash
# Клонировать репозиторий
git clone https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook.git

# Найти нужную информацию
cd prompt-ops-playbook
 cat INDEX.md
```

## Структура репозитория

| Раздел | Содержание | Когда использовать |
|--------|------------|-------------------|
| [01-commands](01-commands/) | CLI команды, slash-команды | Нужна быстрая справка по командам |
| [02-skills](02-skills/) | Навыки, workflow, паттерны | Создаёте новый skill или workflow |
| [03-mcp](03-mcp/) | Model Context Protocol | Интеграция с MCP серверами |
| [04-subagents](04-subagents/) | Субагенты, оркестрация | Делегирование задач агентам |
| [05-troubleshooting](05-troubleshooting/) | Решение проблем | Что-то пошло не так |
| [06-glossary](06-glossary/) | Термины и определения | Нужно уточнить термин |
| [07-registry](07-registry/) | Реестр инструментов | Выбираете инструмент |
| [08-prompts](08-prompts/) | Промпт-шаблоны | Пишете промпт |
| [09-codex](09-codex/) | CodeX субагенты | Работа с Codex |

## Learning Paths

### Путь 1: Claude Code Basics (2-4 часа)
```
01-commands → 02-skills → 05-troubleshooting
```

### Путь 2: MCP Integration (3-5 часов)
```
03-mcp → 04-subagents
```

### Путь 3: Subagent Development (4-6 часов)
```
02-skills → 04-subagents → 09-codex
```

### Путь 4: Full Stack (8-12 часов)
```
01-commands → 02-skills → 03-mcp → 04-subagents
```

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

## Лицензия

MIT License — см. [LICENSE](LICENSE)
