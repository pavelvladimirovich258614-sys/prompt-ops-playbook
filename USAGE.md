# Как пользоваться этим репозиторием

> Подробное руководство с примерами промптов для разных задач

---

## Быстрый старт (2 минуты)

### 1. Откройте репозиторий
```
https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook
```

### 2. Найдите нужное в INDEX.md
Откройте файл `INDEX.md` — там вся навигация.

### 3. Перейдите в нужный раздел
- Нужны **команды** → `01-commands/`
- Нужны **навыки** → `02-skills/`
- Нужен **MCP** → `03-mcp/`
- Нужны **субагенты** → `04-subagents/`
- Нужен **CodeX** → `09-codex/`

---

## Сценарии использования

### Сценарий 1: Мне нужен skill для Claude Code

**Шаг 1:** Откройте файл `02-skills/concept-skill.md`

**Шаг 2:** Прочитайте структуру skill

**Шаг 3:** Скопируйте шаблон и адаптируйте

**Пример промпта для нейросети:**
```
Прочитай файл https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-skill.md

Создай skill для [ЗАДАЧА] по шаблону:
- Название: [название]
- Тип: Technique
- Описание: [что делает]
- Пошаговая инструкция: [шаги]
- Антипаттерны: [что нельзя делать]
```

**Готовый пример:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/skill-brainstorming.md

Создай skill "code-reviewer" для ревью кода на Python:
1. Проверяй типы
2. Ищи баги
3. Проверяй стиль PEP8
4. Оценивай сложность функций
```

---

### Сценарий 2: Мне нужна slash-команда для Claude Code

**Шаг 1:** Откройте файл `01-commands/slash-commands.md`

**Шаг 2:** Найдите нужную команду

**Шаг 3:** Используйте в Claude Code

**Пример промпта для нейросети:**
```
Прочитай файл https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/slash-commands.md

Объясни мне команды:
- /clear — когда использовать
- /compact — когда использовать
- /plan — как создавать планы
```

**Готовый пример:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/slash-commands.md

Как использовать /plan для разработки новой фичи?
Покажи пример сессии.
```

---

### Сценарий 3: Мне нужен CodeX субагент

**Шаг 1:** Откройте файл `09-codex/01-subagents-catalog.md`

**Шаг 2:** Найдите категорию агента

**Шаг 3:** Выберите подходящего

**Шаг 4:** Используйте шаблон из `09-codex/02-subagent-spec-template.md`

**Пример промпта для нейросети:**
```
Прочитай файл https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/01-subagents-catalog.md

Найди мне субагента для [ЗАДАЧА].
Нужен агент из категории [КАТЕГОРИЯ].
```

**Готовый пример:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/01-subagents-catalog.md

Мне нужен субагент для ревью Python кода.
Найди подходящего из категории 04-quality-security.
Покажи его спецификацию.
```

**Ещё пример (создание своего агента):**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/02-subagent-spec-template.md

Создай TOML спецификацию для субагента "api-tester":
- Тестирует REST API endpoints
- Проверяет статус коды
- Валидирует JSON ответы
- Генерирует отчёт
```

---

### Сценарий 4: Мне нужно настроить MCP

**Шаг 1:** Откройте файл `03-mcp/context7-platform.md`

**Шаг 2:** Прочитайте про MCP

**Шаг 3:** Скопируйте конфигурацию

**Пример промпта для нейросети:**
```
Прочитай файл https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/context7-platform.md

Как настроить Context7 MCP для Cursor?
Покажи пошагово:
1. Установку
2. Конфигурацию
3. Использование
```

**Готовый пример:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/ctx7-cli.md

Настрой Context7 для моего проекта:
- Использую React и TypeScript
- Нужна документация по hooks
- Работаю в VS Code
```

---

### Сценарий 5: Мне нужен workflow для команды

**Шаг 1:** Откройте файл `02-skills/concept-workflow.md`

**Шаг 2:** Выберите подходящий workflow

**Шаг 3:** Адаптируйте под свою команду

**Пример промпта для нейросети:**
```
Прочитай файл https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-workflow.md

Объясни workflow "Subagent-driven Development":
1. Когда применять
2. Какие шаги
3. Какие инструменты нужны
4. Примеры
```

**Готовый пример:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-workflow.md

Внедри workflow для моей команды:
- 3 разработчика
- Работаем над веб-приложением
- Нужно code review
- Используем Git

Покажи пошаговый план внедрения.
```

---

### Сценарий 6: Мне нужен agent loop для своего проекта

**Шаг 1:** Откройте файл `04-subagents/agent-loop.md`

**Шаг 2:** Изучите структуру

**Шаг 3:** Реализуйте на своём языке

**Пример промпта для нейросети:**
```
Прочитай файл https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/agent-loop.md

Создай agent loop на Python:
1. Получает input от пользователя
2. Думает (LLM API)
3. Вызывает инструменты
4. Возвращает результат

Используй OpenAI API.
```

**Готовый пример:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/agent-loop.md

Напиши минимальный агент на Python с:
- Инструментом read_file
- Инструментом write_file
- Инструментом execute (bash)

Покажи полный код.
```

---

### Сценарий 7: Мне нужно делегирование субагентам

**Шаг 1:** Откройте файл `04-subagents/subagents-and-delegation.md`

**Шаг 2:** Изучите паттерны

**Шаг 3:** Примените в проекте

**Пример промпта для нейросети:**
```
Прочитай файл https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/subagents-and-delegation.md

Объясни паттерн "Parallel Review":
1. Как создать несколько субагентов
2. Как запустить параллельно
3. Как агрегировать результаты
```

**Готовый пример:**
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/subagents-and-delegation.md

Создай систему code review с 3 субагентами:
1. security-reviewer — проверяет безопасность
2. style-reviewer — проверяет стиль
3. logic-reviewer — проверяет логику

Покажи как запустить их параллельно.
```

---

## Примеры промптов для разных задач

### Для Claude Code
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/skills.md

Установи skill clone и покажи как им пользоваться.
```

### Для Cursor
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/context7-platform.md

Настрой Context7 MCP для моего проекта на React.
```

### Для CodeX
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/01-subagents-catalog.md

Найди мне субагента для backend разработки на Python.
```

### Для собственного агента
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/agent-loop.md

Создай мне агента с инструментами:
- Поиск по коду
- Чтение файлов
- Запуск тестов
```

---

## Learning Paths (Пути обучения)

### Путь 1: Claude Code Basics (2-4 часа)
```
01-commands/slash-commands.md → 01-commands/skills.md → 02-skills/concept-skill.md
```

**Промпт:**
```
Прочитай последовательно:
1. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/slash-commands.md
2. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/01-commands/skills.md
3. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-skill.md

Создай summary и покажи как применить.
```

### Путь 2: MCP Integration (3-5 часов)
```
03-mcp/context7-platform.md → 03-mcp/ctx7-cli.md → 04-subagents/agent-loop.md
```

**Промпт:**
```
Прочитай последовательно:
1. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/context7-platform.md
2. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/03-mcp/ctx7-cli.md

Настрой Context7 для моего проекта и покажи как использовать.
```

### Путь 3: Subagent Development (4-6 часов)
```
02-skills/concept-workflow.md → 04-subagents/subagents-and-delegation.md → 09-codex/01-subagents-catalog.md
```

**Промпт:**
```
Прочитай последовательно:
1. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/02-skills/concept-workflow.md
2. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/04-subagents/subagents-and-delegation.md
3. https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/09-codex/01-subagents-catalog.md

Создай workflow для моей команды с использованием субагентов.
```

### Путь 4: Full Stack (8-12 часов)
```
01-commands → 02-skills → 03-mcp → 04-subagents → 09-codex
```

**Промпт:**
```
Прочитай все разделы репозитория:
https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook

Создай комплексное решение для моей команды разработчиков:
- Настройка Claude Code
- Настройка MCP
- Workflow с субагентами
- CodeX интеграция
```

---

## Частые вопросы (FAQ)

### Q: Как быстро найти нужное?
**A:** Откройте `INDEX.md` — там вся навигация по разделам.

### Q: Где взять готовый skill?
**A:** В `02-skills/` — там concept-skill.md и примеры.

### Q: Как создать свой субагент?
**A:** В `09-codex/02-subagent-spec-template.md` — шаблон TOML.

### Q: Как настроить MCP?
**A:** В `03-mcp/context7-platform.md` — инструкции для разных редакторов.

### Q: Где список всех CodeX агентов?
**A:** В `09-codex/01-subagents-catalog.md` — 136+ агентов.

---

## Контакты и поддержка

Если что-то непонятно:
1. Откройте issue в репозитории
2. Опишите проблему
3. Добавьте пример промпта

---

**Начните с:** https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/INDEX.md
