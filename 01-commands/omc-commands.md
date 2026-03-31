# 🚀 Oh-My-ClaudeCode (OMC) — Полное руководство по командам

> Multi-agent orchestration для Claude Code. 32 агента, 8 режимов, zero learning curve.
> Репозиторий: https://github.com/Yeachan-Heo/oh-my-claudecode

---

## Установка

### Шаг 1 — npm (CLI)
```bash
npm i -g oh-my-claude-sisyphus@latest
Шаг 2 — Plugin (внутри Claude Code)
Copy/plugin marketplace add https://github.com/Yeachan-Heo/oh-my-claudecode
/plugin install oh-my-claudecode
/reload-plugins
Шаг 3 — tmux (обязательно для Team/Wait)
Платформа	Установка
Windows (native)	winget install psmux
Windows (WSL2)	sudo apt install tmux
macOS	brew install tmux
Ubuntu/Debian	sudo apt install tmux
Шаг 4 — Первый запуск
Copy/setup
или

Copy/omc-setup
Режимы оркестрации
1. autopilot: [задача] — Автономное выполнение
Что делает: Claude сам планирует, пишет код, создаёт файлы, тестирует. Без вопросов.

Когда применять:

Задача чётко сформулирована
Понятен конечный результат
Не нужен контроль на каждом шаге
Когда НЕ применять:

Задача размытая ("сделай лучше", "почини всё")
Нужен контроль на каждом этапе
Критичный production-код без ревью
Примеры:

Copyautopilot: создай REST API эндпоинт POST /api/users с валидацией email и password, сохранением в PostgreSQL и возвратом JWT токена

autopilot: добавь middleware для rate limiting — максимум 100 запросов в минуту на IP, Redis для хранения счётчиков

autopilot: напиши unit-тесты для модуля auth — покрой login, register, refresh-token, минимум 80% coverage

autopilot: создай Dockerfile для проекта — multi-stage build, node:20-alpine, production-оптимизация
Pipeline внутри: expand → plan → execute → verify

2. ralph: [задача] — Упёртый режим (verify-fix loop)
Что делает: Выполняет задачу, проверяет результат, находит ошибки, исправляет — и так в цикле, пока всё не заработает. Не остановится на полпути.

Когда применять:

Задача сложная, с первого раза не получится
Нужна 100% завершённость
Рефакторинг, миграции, исправление цепочки багов
Задачи типа "сделай пока не будет 0 ошибок"
Когда НЕ применять:

Простая задача на 5 минут (overkill)
Экспериментальный код (ralph потратит много токенов)
Примеры:

Copyralph: исправь все ошибки TypeScript в проекте — запускай tsc --noEmit и чини пока не будет 0 ошибок

ralph: мигрируй все API-эндпоинты с Express на Fastify, каждый должен проходить существующие тесты

ralph: переведи весь проект с JavaScript на TypeScript, добавь типы ко всем функциям, пока npm run typecheck не пройдёт чисто

ralph: почини все failing тесты в CI — запускай pytest, чини, запускай снова, пока не будет 100% pass
Pipeline внутри: execute → verify → fix → verify → fix → ... → done

Важно: Ralph включает в себя ultrawork (параллельное выполнение), поэтому отдельно ulw вызывать не нужно.

3. /deep-interview "идея" — Сократовский опрос
Что делает: Задаёт серию вопросов по методу Сократа, чтобы превратить размытую идею в чёткое техническое задание. Выявляет скрытые допущения, измеряет ясность по взвешенным параметрам.

Когда применять:

Есть идея, но не уверен в деталях
Начинаешь новую фичу или проект
Хочешь убедиться, что ничего не забыл
Перед передачей задачи команде
Когда НЕ применять:

Задача уже полностью расписана
Нужно быстро починить баг (не время для интервью)
Примеры:

Copy/deep-interview "хочу добавить систему оплаты в проект"

/deep-interview "нужна система уведомлений — email, push, telegram"

/deep-interview "хочу переписать фронтенд на Next.js"

/deep-interview "нужен бот для автоматической модерации контента"
Что спросит:

Какие платёжные системы? (Stripe, PayPal, ЮKassa?)
Разовая оплата или подписка?
Пробный период?
Webhook-и для обработки событий?
Какие валюты?
Как обрабатывать ошибки оплаты?
Результат: Структурированный документ требований, готовый для autopilot: или /team.

4. /team N:executor "задача" — Мульти-агентный режим
Что делает: Запускает N агентов-воркеров параллельно. Каждый работает над своей частью задачи. Проходит через staged pipeline: plan → PRD → exec → verify → fix.

Когда применять:

Большая задача, которую можно разбить на части
Нужна скорость (параллельная работа)
Разные аспекты задачи требуют разных специалистов
Комплексные фичи с frontend + backend + тесты
Когда НЕ применять:

Маленькая задача (overhead на координацию > пользы)
Задачи с жёсткой последовательностью (каждый шаг зависит от предыдущего)
Синтаксис:

Copy/team N:executor "задача"
Где N — количество воркеров (1-5 рекомендуется).

Примеры:

Copy/team 3:executor "добавь авторизацию: агент 1 — модель User и миграции, агент 2 — middleware auth и JWT, агент 3 — роуты login/register/logout с валидацией"

/team 2:executor "агент 1 — напиши backend API для чата на WebSocket, агент 2 — напиши frontend React компонент чата"

/team 4:executor "рефакторинг модуля billing: агент 1 — модели, агент 2 — сервисы, агент 3 — API роуты, агент 4 — тесты"
С Codex/Gemini (через tmux CLI):

Copyomc team 2:codex "проведи security review модуля авторизации"
omc team 2:gemini "редизайн UI компонентов для accessibility"
omc team 1:claude "реализуй payment flow"
omc team status task-name
omc team shutdown task-name
Pipeline внутри: team-plan → team-prd → team-exec → team-verify → team-fix (loop)

Требование: Включить в ~/.claude/settings.json:

Copy{
  "env": {
    "CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS": "1"
  }
}
5. ulw [задача] — Maximum Parallelism (Ultrawork)
Что делает: Максимальная параллелизация без Team-координации. Быстрый burst-режим для массовых исправлений.

Когда применять:

Много однотипных задач (исправить 20 файлов)
Скорость важнее координации
Не нужен общий план
Примеры:

Copyulw исправь все ESLint ошибки во всех файлах src/

ulw добавь JSDoc комментарии ко всем экспортируемым функциям

ulw обнови все import-ы с relative на alias @/
6. ralplan [тема] — Iterative Planning Consensus
Что делает: Итеративное планирование с несколькими раундами обсуждения — создаёт консенсус по архитектуре/подходу перед написанием кода.

Когда применять:

Сложная архитектурная задача
Нужно взвесить несколько подходов
Перед большим рефакторингом
Примеры:

Copyralplan миграция с монолита на микросервисы

ralplan выбор между GraphQL и REST для нового API

ralplan архитектура системы real-time уведомлений
7. ultrathink [тема] — Deep Reasoning
Что делает: Режим глубокого размышления. Claude тратит больше токенов на рассуждения, проверяет свои выводы.

Когда применять:

Сложная алгоритмическая задача
Архитектурные решения с trade-offs
Debug сложного бага
Примеры:

Copyultrathink как оптимизировать запрос к БД, который занимает 15 секунд

ultrathink архитектура event-driven системы для 100K concurrent users

ultrathink почему возникает race condition в модуле синхронизации
8. deepsearch [запрос] — Codebase Search
Что делает: Поиск по кодовой базе с контекстным пониманием.

Примеры:

Copydeepsearch где обрабатываются webhook-и от Stripe

deepsearch найди все middleware для авторизации

deepsearch как работает кэширование в проекте
Утилиты
/ccg [задача] — Tri-Model Advisor
Отправляет задачу в Codex + Gemini, Claude синтезирует ответы.

Copy/ccg проведи ревью этого PR — архитектура (Codex) и UI компоненты (Gemini)
omc ask [провайдер] "вопрос" — Совет от внешнего AI
Copyomc ask codex "проверь этот migration plan на риски"
omc ask gemini "предложи UI/UX улучшения"
omc ask claude "напиши implementation steps"
omc wait — Rate Limit Wait
Copyomc wait          # Проверить статус
omc wait --start  # Включить авто-резюм
omc wait --stop   # Выключить
stopomc / cancelomc — Остановка
Останавливает все активные OMC режимы.

/omc-doctor — Диагностика
Проверяет состояние OMC, чистит кэш, показывает ошибки.

Skills (Навыки)
OMC автоматически извлекает и переиспользует паттерны:

Создание навыка
Copy/skill add
Структура файла навыка
Copy# .omc/skills/fix-proxy-crash.md
---
name: Fix Proxy Crash
description: aiohttp proxy crashes on ClientDisconnectedError
triggers: ["proxy", "aiohttp", "disconnected"]
source: extracted
---
Wrap handler at server.py:42 in try/except ClientDisconnectedError...
Управление навыками
Команда	Действие
/skill list	Показать все навыки
/skill add	Добавить навык
/skill remove	Удалить навык
/skill edit	Редактировать
/skill search	Поиск
/learner	Автоизвлечение паттернов
Scope навыков
Уровень	Путь	Для кого
Project	.omc/skills/	Команда (version-controlled)
User	~/.omc/skills/	Все твои проекты
Project-навыки имеют приоритет над User-навыками.

Уведомления (Telegram/Discord/Slack)
Telegram
Copyomc config-stop-callback telegram --enable --token <BOT_TOKEN> --chat <CHAT_ID> --tag-list "@username"
Discord
Copyomc config-stop-callback discord --enable --webhook <WEBHOOK_URL> --tag-list "@here,123456789"
Slack
Copyomc config-stop-callback slack --enable --webhook <WEBHOOK_URL> --tag-list "<!here>,<@U1234567890>"
Шпаргалка — Что когда использовать
Ситуация	Команда	Токены
Знаю точно что делать — пусть сделает	autopilot:	Средние
Сложная задача, нужно упорство	ralph:	Высокие
Идея без деталей — нужно уточнить	/deep-interview	Низкие
Большая задача, можно распараллелить	/team N:executor	Высокие
Много однотипных правок	ulw	Средние
Нужно спланировать архитектуру	ralplan	Средние
Глубокий анализ проблемы	ultrathink	Высокие
Поиск по кодовой базе	deepsearch	Низкие
Совет от Codex/Gemini	omc ask / /ccg	Низкие
Остановить всё	stopomc	—
Требования
Claude Code CLI v2.x+ (Claude Max/Pro или Anthropic API key)
tmux (psmux на Windows, tmux на Linux/macOS)
Опционально: Codex CLI (npm i -g @openai/codex), Gemini CLI (npm i -g @google/gemini-cli)
Ссылки
Репозиторий: https://github.com/Yeachan-Heo/oh-my-claudecode
npm пакет: https://www.npmjs.com/package/oh-my-claude-sisyphus
Документация: https://yeachan-heo.github.io/oh-my-claudecode-website
Discord: https://discord.gg/PUwSMR9XNk
Источник: oh-my-claudecode v4.9.3, адаптировано для prompt-ops-playbook
