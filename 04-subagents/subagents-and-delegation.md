# Subagents and Delegation

## Описание
Делегирование задач субагентам с изолированными контекстами.

## Концепция

### Independent Context Windows
Каждый субагент работает в своём изолированном контексте:
- Нет cross-contamination
- Чистый slate для каждой задачи
- Параллельное выполнение

### Explicit Delegation
Явное делегирование — пользователь указывает:
- Каких агентов создать
- Как разделить работу
- Какой формат результата

## Пример делегирования

```
Пользователь: "Review this PR"
→ Агент создаёт subagent-reviewer
→ Reviewer анализирует код
→ Возвращает результат
```

## Структура субагента

```python
subagent = {
    "name": "code-reviewer",
    "description": "Reviews code for correctness and style",
    "model": "claude-3-5-sonnet-20241022",
    "instructions": "Review the provided code...",
    "tools": ["read_file", "grep"]
}
```

## Паттерны делегирования

### 1. Parallel Review
Несколько ревьюеров работают параллельно.

```python
reviewers = [
    create_subagent("security-reviewer"),
    create_subagent("performance-reviewer"),
    create_subagent("style-reviewer")
]

results = await asyncio.gather(
    *[r.review(code) for r in reviewers]
)
```

### 2. Pipeline
Последовательная обработка.

```python
# Step 1: Analyze
analysis = await subagent_analyzer.analyze(code)

# Step 2: Fix
fixes = await subagent_fixer.fix(analysis)

# Step 3: Verify
result = await subagent_verifier.verify(fixes)
```

### 3. Map-Reduce
Разделение задачи и агрегация результатов.

```python
# Map: Process chunks in parallel
chunks = split_file(large_file)
results = await asyncio.gather(
    *[subagent.process(chunk) for chunk in chunks]
)

# Reduce: Combine results
final = await subagent_summarizer.summarize(results)
```

## Инструмент task

```python
# Deep Agents
task = {
    "description": "Review this function",
    "prompt": "Analyze the following code for bugs...",
    "context": {
        "file": "path/to/file.py",
        "function": "process_data"
    }
}

result = await agent.task(task)
```

## Best Practices

### ✅ Делать
- Давать чёткие инструкции
- Предоставлять контекст
- Определять формат результата
- Использовать для изолированных задач

### ❌ Не делать
- Создавать слишком много субагентов
- Делегировать слишком мелкие задачи
- Терять track of созданных агентов

## Антипаттерны

### Over-delegation
```python
# ❌ Плохо: слишком много мелких задач
for line in code:
    await subagent.review_line(line)  # Неэффективно

# ✅ Хорошо: одна задача на файл
await subagent.review_file(file)
```

### Under-specification
```python
# ❌ Плохо: нечёткие инструкции
await subagent.task("Review this")

# ✅ Хорошо: конкретные требования
await subagent.task("""
Review this code for:
1. Security vulnerabilities
2. Performance issues
3. Style violations

Return findings as JSON with severity levels.
""")
```

## Источники
- https://github.com/shareAI-lab/learn-claude-code
- https://github.com/langchain-ai/deepagents
