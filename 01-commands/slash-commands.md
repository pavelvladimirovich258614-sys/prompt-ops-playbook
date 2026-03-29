# Slash-команды Claude Code

## Встроенные команды

### /usage
Показать статистику использования токенов и стоимость.

```
/usage
```

### /chrome
Открыть Chrome DevTools для отладки.

```
/chrome
```

### /mcp
Управление MCP серверами.

```
/mcp
/mcp add <server-name>
/mcp remove <server-name>
```

### /stats
Показать статистику сессии.

```
/stats
```

### /clear
Очистить контекст разговора.

```
/clear
```

### /compact
Сжать контекст, сохраняя ключевые моменты.

```
/compact
```

### /context
Показать текущий контекст.

```
/context
```

### /config
Настройки Claude Code.

```
/config
/config set <key> <value>
```

### /plan
Создать план выполнения задачи.

```
/plan <описание задачи>
```

### /copy
Копировать последний ответ в буфер обмена.

```
/copy
```

## DX Plugin команды

### /dx:clone
Клонировать разговор.

```
/dx:clone
```

### /dx:half-clone
Полуклонирование (сокращение контекста).

```
/dx:half-clone
```

### /dx:handoff
Создать документ передачи.

```
/dx:handoff
```

### /dx:gha
Анализ GitHub Actions failures.

```
/dx:gha
```

### /dx:reddit-fetch
Получить данные с Reddit.

```
/dx:reddit-fetch <subreddit>
```

### /dx:review-claudemd
Ревью CLAUDE.md из истории.

```
/dx:review-claudemd
```

## Источник
- https://github.com/ykdojo/claude-code-tips
