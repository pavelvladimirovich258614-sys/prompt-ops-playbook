# Context7 Platform

Context7 — платформа для получения актуальной документации по библиотекам для LLM и AI-редакторов кода.

## Возможности

- **9000+ библиотек** — от React до редких Python пакетов
- **Актуальная документация** — всегда свежая, из первоисточника
- **Версионирование** — документация для конкретной версии
- **Мультиязычность** — Python, JavaScript, TypeScript, Go

## Режимы работы

### MCP Mode
Интеграция с AI-редакторами через Model Context Protocol.

**Поддерживаемые редакторы:**
- Cursor
- Claude Desktop
- Windsurf
- VS Code (Cline, Roo Code)

### CLI Mode
Командная строка для прямого доступа.

```bash
npx ctx7 setup
ctx7 library react "How to use hooks"
ctx7 docs /facebook/react "useEffect cleanup"
```

### Skills Mode
On-demand загрузка знаний в агента.

## MCP Tools

### resolve-library-id
Конвертирует имя библиотеки в Context7 ID.

**Input:**
```json
{
  "libraryName": "react"
}
```

**Output:**
```json
{
  "libraryId": "/facebook/react",
  "version": "18.2.0"
}
```

### query-docs
Получает документацию по library ID.

**Input:**
```json
{
  "libraryId": "/facebook/react",
  "query": "useEffect cleanup function"
}
```

**Output:**
```json
{
  "documentation": "...",
  "codeExamples": [...],
  "references": [...]
}
```

## Установка MCP Server

### Cursor
```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

### Claude Desktop
```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

### Windsurf
```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

## NPM Packages

| Пакет | Назначение |
|-------|------------|
| `ctx7` | CLI |
| `@upstash/context7-mcp` | MCP Server |
| `@upstash/context7-sdk` | TypeScript SDK |
| `@upstash/context7-tools-ai-sdk` | Vercel AI SDK Tools |

## Источник
- https://github.com/upstash/context7
- https://context7.com
