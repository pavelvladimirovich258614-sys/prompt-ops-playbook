# Skills для Claude Code

## Установка Skills

```bash
# Клонировать репозиторий с skills
git clone https://github.com/ykdojo/claude-code-tips.git

# Скопировать skills в директорию Claude Code
mkdir -p ~/.claude/skills
cp -r claude-code-tips/skills/* ~/.claude/skills/
```

## Доступные Skills

### clone
Клонирование разговора для продолжения в новом контексте.

**Когда использовать:**
- Контекст стал слишком большим
- Хотите начать новую ветку обсуждения
- Нужно сохранить текущее состояние

```bash
# Использование
claude skill clone
```

### gha
Анализ failures в GitHub Actions.

**Когда использовать:**
- CI/CD пайплайн упал
- Нужно быстро найти причину ошибки
- Анализ логов GitHub Actions

```bash
# Использование
claude skill gha <run-id>
```

### half-clone
Полуклонирование — сокращение контекста без потери сути.

**Когда использовать:**
- Контекст заполнен на 50-70%
- Нужно освободить место
- Хотите сохранить ключевые решения

```bash
# Использование
claude skill half-clone
```

### handoff
Создание документа передачи для другого разработчика.

**Когда использовать:**
- Передача задачи коллеге
- Документирование прогресса
- Подготовка к code review

```bash
# Использование
claude skill handoff
```

### reddit-fetch
Получение данных с Reddit через Gemini CLI.

**Когда использовать:**
- Нужны свежие обсуждения
- Мониторинг мнений
- Исследование трендов

```bash
# Использование
claude skill reddit-fetch r/ClaudeAI
```

### review-claudemd
Ревью CLAUDE.md из истории разговоров.

**Когда использовать:**
- Анализ предыдущих сессий
- Поиск решений в истории
- Документирование паттернов

```bash
# Использование
claude skill review-claudemd
```

## Структура Skill

```
skills/
└── <skill-name>/
    ├── SKILL.md          # Основная документация
    ├── config.json       # Конфигурация (опционально)
    └── examples/         # Примеры (опционально)
```

## Источник
- https://github.com/ykdojo/claude-code-tips/tree/main/skills
