# Agent Loop

## Описание
Минимальный цикл агента — основа любого AI-агента.

## Концепция
```
┌─────────────┐
│   Start     │
└──────┬──────┘
       ▼
┌─────────────┐
│  Receive    │
│   Input     │
└──────┬──────┘
       ▼
┌─────────────┐     ┌─────────────┐
│   Think     │◄────┤   Memory    │
└──────┬──────┘     └─────────────┘
       ▼
┌─────────────┐
│   Act       │
│ (Tool Call) │
└──────┬──────┘
       ▼
┌─────────────┐
│   Observe   │
│   Result    │
└──────┬──────┘
       │
       └──────► (Loop back to Think)
```

## Реализация

```python
import anthropic

client = anthropic.Anthropic()

messages = []

def agent_loop(user_input):
    # Add user message
    messages.append({"role": "user", "content": user_input})
    
    # Get response from LLM
    response = client.messages.create(
        model="claude-3-5-sonnet-20241022",
        max_tokens=4096,
        tools=tools,  # Available tools
        messages=messages
    )
    
    # Check if tool call needed
    if response.stop_reason == "tool_use":
        for block in response.content:
            if block.type == "tool_use":
                # Execute tool
                result = execute_tool(block.name, block.input)
                
                # Add tool result to messages
                messages.append({
                    "role": "user",
                    "content": [
                        {
                            "type": "tool_result",
                            "tool_use_id": block.id,
                            "content": result
                        }
                    ]
                })
        
        # Continue loop
        return agent_loop("")
    
    # Return final response
    return response.content[0].text
```

## Компоненты

### 1. Input
Получение входных данных от пользователя.

### 2. Think
Анализ контекста и принятие решения.
- Понимание запроса
- Анализ доступных инструментов
- Планирование действий

### 3. Act
Выполнение действия (вызов инструмента).

### 4. Observe
Получение результата и обновление контекста.

### 5. Memory
Сохранение контекста между итерациями.

## Пример: Простой агент с инструментами

```python
tools = [
    {
        "name": "read_file",
        "description": "Read file contents",
        "input_schema": {
            "type": "object",
            "properties": {
                "path": {"type": "string"}
            },
            "required": ["path"]
        }
    },
    {
        "name": "write_file",
        "description": "Write to file",
        "input_schema": {
            "type": "object",
            "properties": {
                "path": {"type": "string"},
                "content": {"type": "string"}
            },
            "required": ["path", "content"]
        }
    }
]

def execute_tool(name, input):
    if name == "read_file":
        with open(input["path"], "r") as f:
            return f.read()
    elif name == "write_file":
        with open(input["path"], "w") as f:
            f.write(input["content"])
        return "File written successfully"
```

## Девиз
> "One loop & Bash is all you need"

## Источник
- https://github.com/shareAI-lab/learn-claude-code
