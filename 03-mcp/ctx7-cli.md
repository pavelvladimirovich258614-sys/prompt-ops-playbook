# ctx7 CLI

## Установка

```bash
# One-command setup
npx ctx7 setup

# Или глобальная установка
npm install -g ctx7
```

## Команды

### ctx7 library
Поиск и получение информации о библиотеке.

```bash
# Поиск библиотеки
ctx7 library react

# Запрос с вопросом
ctx7 library react "How to use useEffect"

# Конкретная версия
ctx7 library react@18.2.0 "Hooks API"
```

### ctx7 docs
Получение документации по пути.

```bash
# Получить документацию
ctx7 docs /facebook/react "useEffect"

# С примерами кода
ctx7 docs /facebook/react "useEffect" --examples

# Только типы
ctx7 docs /facebook/react "useEffect" --types
```

### ctx7 setup
Настройка Context7 для проекта.

```bash
# Интерактивная настройка
ctx7 setup

# Быстрая настройка
ctx7 setup --quick

# С конкретными библиотеками
ctx7 setup --libs react,express,lodash
```

### ctx7 skills
Управление skills.

```bash
# Список доступных skills
ctx7 skills

# Установить skill
ctx7 skills install context7-cli

# Обновить skills
ctx7 skills update
```

## Опции

| Опция | Описание |
|-------|----------|
| `--lang` | Язык (js, ts, py, go) |
| `--version` | Версия библиотеки |
| `--full` | Полная документация |
| `--json` | JSON формат вывода |
| `--output` | Сохранить в файл |

## Примеры

```bash
# React hooks на TypeScript
ctx7 docs /facebook/react "useEffect" --lang ts

# Express middleware
ctx7 docs /expressjs/express "middleware" --examples

# Python requests
ctx7 docs /psf/requests "session" --lang py

# Сохранить в файл
ctx7 docs /facebook/react "hooks" --output react-hooks.md
```

## Конфигурация

Файл: `~/.context7/config.json`

```json
{
  "defaultLanguage": "ts",
  "cacheEnabled": true,
  "cacheTTL": 3600,
  "outputFormat": "markdown"
}
```

## Источник
- https://github.com/upstash/context7/tree/main/packages/cli
