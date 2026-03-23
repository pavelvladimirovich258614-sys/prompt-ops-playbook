# chub CLI — Context Hub

## Установка

```bash
npm install -g @aisuite/chub
```

## Команды

### chub search
Поиск документов и навыков.

```bash
# Поиск по запросу
chub search "stripe"

# Список всех доступных пакетов
chub search

# Фильтрация по тегам
chub search "openai" --tags api,python

# Ограничение результатов
chub search "react" --limit 10

# JSON формат
chub search "vue" --json
```

### chub get
Получить документы/навыки по ID.

```bash
# Получить документацию
chub get stripe/api

# Указать язык
chub get openai/chat --lang py
chub get openai/chat --lang js

# Полная версия со всеми reference-файлами
chub get anthropic/claude --full

# Конкретный файл
chub get langchain/core --file agents.md

# Сохранить в файл
chub get react/hooks --output react-hooks.md

# JSON формат
chub get vue/composition --json
```

### chub annotate
Добавить локальную заметку к документу.

```bash
# Добавить заметку
chub annotate stripe/api "Использовать v2 для новых проектов"

# Очистить заметки
chub annotate stripe/api --clear

# Показать все заметки
chub annotate stripe/api --list
```

### chub feedback
Проголосовать за документ.

```bash
# Положительный отзыв
chub feedback stripe/api up

# Отрицательный отзыв
chub feedback stripe/api down

# С комментарием
chub feedback stripe/api up --label "helpful" "Отличные примеры кода"

# С меткой
chub feedback openai/chat down --label "outdated" "Устаревшая версия API"
```

## Конфигурация

Файл конфигурации: `~/.chub/config.yaml`

```yaml
# Источники контента
sources:
  - official    # Официальная документация
  - maintainer  # От мейнтейнеров
  - community   # Комьюнити

# Язык по умолчанию
language: en

# Формат вывода
format: markdown  # markdown | json
```

## Интеграция с Claude Code

```bash
# Установить skill
mkdir -p ~/.claude/skills
cp cli/skills/get-api-docs/SKILL.md ~/.claude/skills/get-api-docs.md
```

## Интеграция с Cursor

```bash
# Скопировать skill в проект
mkdir -p .cursor/rules
cp cli/skills/get-api-docs/SKILL.md .cursor/rules/get-api-docs.md
```

## Источник
- https://github.com/andrewyng/context-hub
