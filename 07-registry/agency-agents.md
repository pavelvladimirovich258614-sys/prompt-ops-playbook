# Agency Agents

> Полная AI-агентство у вас под рукой — от frontend-волшебников до Reddit-ниндзя, от инжекторов радости до проверяющих реальность. Каждый агент — специализированный эксперт с личностью, процессами и проверенными результатами.

**Источник:** https://github.com/msitarzewski/agency-agents

---

## Что это?

Agency Agents — это коллекция из **144+ специализированных AI-агентов**, организованных в **12 дивизий**. Каждый агент имеет:

- 🎭 **Уникальную личность** — характер, стиль коммуникации, подход
- 📋 **Чёткие результаты** — конкретные выходы, а не расплывчатые советы
- ✅ **Проверенные workflow** — пошаговые процессы, которые работают
- 📊 **Метрики успеха** — измеримые критерии качества

---

## Быстрый старт

### Вариант 1: С Claude Code (рекомендуется)

```bash
# Клонировать репозиторий
git clone https://github.com/msitarzewski/agency-agents.git
cd agency-agents

# Установить агентов
./scripts/install-claude.sh

# Или вручную
cp -r agency-agents/* ~/.claude/agents/
```

**Использование:**
```
Привет Claude, активируй режим Frontend Developer и помоги мне создать React компонент
```

### Вариант 2: С Cursor

```bash
# Установить для Cursor
./scripts/install-cursor.sh

# Агенты будут в .cursor/rules/
```

**Использование:**
```
@frontend-developer Перепиши этот компонент на TypeScript
```

### Вариант 3: С Aider

```bash
# Установить для Aider
./scripts/install-aider.sh

# Создаст CONVENTIONS.md в проекте
```

**Использование:**
```
Используй Frontend Developer для рефакторинга этого компонента
```

---

## Структура агента

Каждый агент — это markdown-файл с:

```markdown
---
name: "Frontend Developer"
description: "React/Vue/Angular, UI implementation, performance"
color: "🎨"
---

# Frontend Developer

## Identity & Memory
- Кто я: эксперт по frontend с 10+ годами опыта
- Мой стиль: практичный, ориентированный на результат
- Что я помню: ваши предпочтения, codebase, ошибки прошлого

## Core Mission
Создавать производительные, доступные и красивые пользовательские интерфейсы.

## Critical Rules
- ✅ Всегда проверяй доступность (a11y)
- ✅ Оптимизируй Core Web Vitals
- ✅ Пиши тесты для критичных путей
- ❌ Никогда не игнорируй мобильные устройства
- ❌ Никогда не оставляй console.log в production

## Technical Deliverables

### React Component Template
```tsx
interface Props {
  // ...
}

export const Component: React.FC<Props> = ({ ... }) => {
  // ...
};
```

## Workflow Process
1. Анализ требований
2. Проектирование интерфейса
3. Реализация
4. Тестирование
5. Оптимизация

## Success Metrics
- Lighthouse score > 90
- 100% типизация TypeScript
- Покрытие тестами > 80%
```

---

## Дивизии и агенты

### 💻 Engineering Division (19 агентов)

Строим будущее, один коммит за раз.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🎨 **Frontend Developer** | React/Vue/Angular, UI, performance | Современные веб-приложения, pixel-perfect UI |
| 🏗️ **Backend Architect** | API design, БД, scalability | Серверные системы, микросервисы |
| 📱 **Mobile App Builder** | iOS/Android, React Native, Flutter | Мобильные приложения |
| 🤖 **AI Engineer** | ML models, deployment, AI integration | ML-фичи, data pipelines |
| 🚀 **DevOps Automator** | CI/CD, infrastructure, cloud | Автоматизация деплоя |
| ⚡ **Rapid Prototyper** | Fast POC, MVPs | Быстрые прототипы, хакатоны |
| 💎 **Senior Developer** | Laravel/Livewire, advanced patterns | Сложная реализация |
| 🔒 **Security Engineer** | Threat modeling, secure code review | Безопасность приложений |
| ⚡ **Autonomous Optimization Architect** | LLM routing, cost optimization | Оптимизация затрат на AI |
| 🔩 **Embedded Firmware Engineer** | Bare-metal, RTOS, ESP32/STM32 | Embedded системы |
| 🚨 **Incident Response Commander** | Incident management, post-mortems | Production инциденты |
| ⛓️ **Solidity Smart Contract Engineer** | EVM contracts, gas optimization | Smart contracts, DeFi |
| 📚 **Technical Writer** | Developer docs, API reference | Техническая документация |
| 🎯 **Threat Detection Engineer** | SIEM rules, threat hunting | Обнаружение угроз |
| 💬 **WeChat Mini Program Developer** | WeChat ecosystem, Mini Programs | WeChat Mini Programs |
| 👁️ **Code Reviewer** | Code review, security, maintainability | PR reviews, code quality |
| 🗄️ **Database Optimizer** | Schema design, query optimization | PostgreSQL/MySQL tuning |
| 🌿 **Git Workflow Master** | Branching strategies, conventional commits | Git workflow design |
| 🏛️ **Software Architect** | System design, DDD, patterns | Архитектурные решения |

### 🎨 Design Division (8 агентов)

Делаем красиво, удобно и приятно.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🎯 **UI Designer** | Visual design, component libraries | Создание интерфейсов |
| 🔍 **UX Researcher** | User testing, behavior analysis | Исследование пользователей |
| 🏛️ **UX Architect** | Technical architecture, CSS systems | Архитектура UX |
| 🎭 **Brand Guardian** | Brand identity, consistency | Бренд-стратегия |
| 📖 **Visual Storyteller** | Visual narratives, multimedia | Визуальные истории |
| ✨ **Whimsy Injector** | Personality, delight, playful interactions | Добавление радости в UI |
| 📷 **Image Prompt Engineer** | AI image generation prompts | Генерация изображений |
| 🌈 **Inclusive Visuals Specialist** | Representation, bias mitigation | Инклюзивный дизайн |

### 💰 Paid Media Division (7 агентов)

Превращаем рекламный бюджет в измеримые результаты.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 💰 **PPC Campaign Strategist** | Google/Microsoft/Amazon Ads | Настройка рекламных кампаний |
| 🔍 **Search Query Analyst** | Search term analysis, negative keywords | Анализ поисковых запросов |
| 📋 **Paid Media Auditor** | 200+ point account audits | Аудит рекламных аккаунтов |
| 📡 **Tracking & Measurement Specialist** | GTM, GA4, conversion tracking | Настройка отслеживания |
| ✍️ **Ad Creative Strategist** | RSA copy, Meta creative | Создание рекламных креативов |
| 📺 **Programmatic & Display Buyer** | GDN, DSPs, ABM display | Программатик и дисплей |
| 📱 **Paid Social Strategist** | Meta, LinkedIn, TikTok | Социальные сети |

### 💼 Sales Division (8 агентов)

Превращаем pipeline в выручку.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🎯 **Outbound Strategist** | Signal-based prospecting | Исходящий sales |
| 🔍 **Discovery Coach** | SPIN, Gap Selling, Sandler | Подготовка к discovery calls |
| ♟️ **Deal Strategist** | MEDDPICC, competitive positioning | Стратегия сделок |
| 🛠️ **Sales Engineer** | Technical demos, POC scoping | Pre-sales |
| 🏹 **Proposal Strategist** | RFP response, win themes | Написание предложений |
| 📊 **Pipeline Analyst** | Forecasting, pipeline health | Анализ pipeline |
| 🗺️ **Account Strategist** | Land-and-expand, QBRs | Работа с аккаунтами |
| 🏋️ **Sales Coach** | Rep development, call coaching | Коучинг sales reps |

### 📢 Marketing Division (20+ агентов)

Растим аудиторию, одно аутентичное взаимодействие за раз.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🚀 **Growth Hacker** | Rapid user acquisition, viral loops | Взрывной рост |
| 📝 **Content Creator** | Multi-platform content | Контент-стратегия |
| 🐦 **Twitter Engager** | Real-time engagement | Twitter стратегия |
| 📱 **TikTok Strategist** | Viral content, algorithm | TikTok рост |
| 📸 **Instagram Curator** | Visual storytelling | Instagram стратегия |
| 🤝 **Reddit Community Builder** | Authentic engagement | Reddit маркетинг |
| 📱 **App Store Optimizer** | ASO, conversion optimization | ASO |
| 🌐 **Social Media Strategist** | Cross-platform strategy | Общая SMM стратегия |
| 📕 **Xiaohongshu Specialist** | Lifestyle content | Xiaohongshu |
| 💬 **WeChat Official Account Manager** | Subscriber engagement | WeChat OA |
| 🧠 **Zhihu Strategist** | Thought leadership | Zhihu |
| 🇨🇳 **Baidu SEO Specialist** | Baidu optimization | SEO для Китая |
| 🎬 **Bilibili Content Strategist** | B站 algorithm | Bilibili |
| 🎠 **Carousel Growth Engine** | TikTok/Instagram carousels | Карусели |
| 💼 **LinkedIn Content Creator** | Personal branding | LinkedIn |
| 🛒 **China E-Commerce Operator** | Taobao, Tmall, Pinduoduo | E-commerce в Китае |
| 🎥 **Kuaishou Strategist** | Kuaishou, 老铁 community | Kuaishou |
| 🔍 **SEO Specialist** | Technical SEO, content strategy | SEO |
| 📘 **Book Co-Author** | Thought-leadership books | Написание книг |
| 🌏 **Cross-Border E-Commerce Specialist** | Amazon, Shopee, Lazada | Cross-border |
| 🎵 **Douyin Strategist** | Douyin platform | Douyin |
| 🎙️ **Livestream Commerce Coach** | Host training, live room | Livestream commerce |
| 🎧 **Podcast Strategist** | Podcast content strategy | Подкасты |
| 🔒 **Private Domain Operator** | WeCom, private traffic | Private domain |
| 🎬 **Short-Video Editing Coach** | Post-production | Редактирование видео |
| 🔥 **Weibo Strategist** | Sina Weibo | Weibo |
| 🔮 **AI Citation Strategist** | AEO/GEO, AI recommendation | Видимость в AI |

### 📊 Product Division (4 агента)

Строим правильную вещь в правильное время.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🎯 **Sprint Prioritizer** | Agile planning, feature prioritization | Планирование спринтов |
| 🔍 **Trend Researcher** | Market intelligence | Исследование рынка |
| 💬 **Feedback Synthesizer** | User feedback analysis | Анализ feedback |
| 🧠 **Behavioral Nudge Engine** | Behavioral psychology | Поведенческая психология |
| 🧭 **Product Manager** | Full lifecycle product ownership | Product management |

### 🎬 Project Management Division (6 агентов)

Держим поезда вовремя (и в бюджете).

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🎬 **Studio Producer** | High-level orchestration | Управление портфелем |
| 🐑 **Project Shepherd** | Cross-functional coordination | Координация проектов |
| ⚙️ **Studio Operations** | Day-to-day efficiency | Операционная эффективность |
| 🧪 **Experiment Tracker** | A/B tests, hypothesis validation | Эксперименты |
| 👔 **Senior Project Manager** | Realistic scoping | Планирование проектов |
| 📋 **Jira Workflow Steward** | Git workflow, branch strategy | Jira workflow |

### 🧪 Testing Division (7 агентов)

Ломаем вещи, чтобы пользователи не сломали.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 📸 **Evidence Collector** | Screenshot-based QA | UI тестирование |
| 🔍 **Reality Checker** | Evidence-based certification | Проверка готовности |
| 📊 **Test Results Analyzer** | Test evaluation | Анализ результатов |
| ⚡ **Performance Benchmarker** | Performance testing | Performance тестирование |
| 🔌 **API Tester** | API validation | API тестирование |
| 🛠️ **Tool Evaluator** | Technology assessment | Оценка инструментов |
| 🔄 **Workflow Optimizer** | Process analysis | Оптимизация процессов |
| ♿ **Accessibility Auditor** | WCAG auditing | Accessibility testing |

### 🛟 Support Division (6 агентов)

Опора операции.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 💬 **Support Responder** | Customer service | Поддержка клиентов |
| 📊 **Analytics Reporter** | Data analysis, dashboards | Аналитика |
| 💰 **Finance Tracker** | Financial planning | Финансы |
| 🏗️ **Infrastructure Maintainer** | System reliability | Инфраструктура |
| ⚖️ **Legal Compliance Checker** | Compliance, regulations | Комплаенс |
| 📑 **Executive Summary Generator** | C-suite communication | Executive отчёты |

### 🥽 Spatial Computing Division (6 агентов)

Строим иммерсивное будущее.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🏗️ **XR Interface Architect** | Spatial interaction design | AR/VR/XR дизайн |
| 💻 **macOS Spatial/Metal Engineer** | Swift, Metal, 3D | Vision Pro native apps |
| 🌐 **XR Immersive Developer** | WebXR, browser-based AR/VR | WebXR приложения |
| 🎮 **XR Cockpit Interaction Specialist** | Cockpit-based controls | Cockpit системы |
| 🍎 **visionOS Spatial Engineer** | Apple Vision Pro development | Vision Pro apps |
| 🔌 **Terminal Integration Specialist** | Terminal integration | CLI инструменты |

### 🎯 Specialized Division (30+ агентов)

Уникальные специалисты, которые не вписываются в рамки.

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🎭 **Agents Orchestrator** | Multi-agent coordination | Оркестрация агентов |
| 🔍 **LSP/Index Engineer** | Language Server Protocol | LSP реализация |
| 📥 **Sales Data Extraction Agent** | Excel monitoring | Извлечение данных |
| 📈 **Data Consolidation Agent** | Sales data aggregation | Консолидация данных |
| 📬 **Report Distribution Agent** | Automated report delivery | Рассылка отчётов |
| 🔐 **Agentic Identity & Trust Architect** | Agent identity | Identity системы |
| 🔗 **Identity Graph Operator** | Shared identity resolution | Identity resolution |
| 💸 **Accounts Payable Agent** | Payment processing | Платежи |
| 🛡️ **Blockchain Security Auditor** | Smart contract audits | Аудит контрактов |
| 📋 **Compliance Auditor** | SOC 2, ISO 27001 | Комплаенс аудит |
| 🌍 **Cultural Intelligence Strategist** | Global UX | Культурный интеллект |
| 🗣️ **Developer Advocate** | Community building | Developer advocacy |
| 🔬 **Model QA Specialist** | ML audits | QA для ML |
| 🗃️ **ZK Steward** | Knowledge management | Knowledge management |
| 🔌 **MCP Builder** | Model Context Protocol | MCP серверы |
| 📄 **Document Generator** | PDF, PPTX, DOCX generation | Генерация документов |
| ⚙️ **Automation Governance Architect** | Automation governance | Governance автоматизации |
| 📚 **Corporate Training Designer** | Enterprise training | Корпоративное обучение |
| 🏛️ **Government Digital Presales Consultant** | China ToG presales | Государственные закупки |
| ⚕️ **Healthcare Marketing Compliance** | Healthcare compliance | Healthcare compliance |
| 🎯 **Recruitment Specialist** | Talent acquisition | Рекрутинг |
| 🎓 **Study Abroad Advisor** | International education | Образование за рубежом |
| 🔗 **Supply Chain Strategist** | Supply chain management | Supply chain |
| 🗺️ **Workflow Architect** | Workflow discovery | Workflow архитектура |
| ☁️ **Salesforce Architect** | Multi-cloud Salesforce | Salesforce |
| 🇫🇷 **French Consulting Market Navigator** | ESN/SI ecosystem | Французский рынок |
| 🇰🇷 **Korean Business Navigator** | Korean business culture | Корейский бизнес |

### 🎮 Game Development Division (9+ агентов)

Строим миры, системы и опыт.

#### Cross-Engine Agents

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🎯 **Game Designer** | Systems design, GDD | Дизайн игр |
| 🗺️ **Level Designer** | Layout theory, pacing | Level design |
| 🎨 **Technical Artist** | Shaders, VFX | Technical art |
| 🔊 **Game Audio Engineer** | FMOD/Wwise, spatial audio | Game audio |
| 📖 **Narrative Designer** | Story systems, branching dialogue | Нарратив |

#### Unity

| Агент | Специализация | Когда использовать |
|-------|---------------|-------------------|
| 🏗️ **Unity Architect** | ScriptableObjects, DOTS/ECS | Unity архитектура |
| ✨ **Unity Shader Graph Artist** | Shader Graph, HLSL | Unity shaders |
| 🌐 **Unity Multiplayer Engineer** | Netcode for GameObjects | Unity multiplayer |
| 🛠️ **Unity Editor Tool Developer** | EditorWindows, AssetPostprocessors | Unity Editor tools |

---

## Реальные сценарии использования

### Сценарий 1: Создание стартап MVP

**Ваша команда:**
1. 🎨 **Frontend Developer** — строит React приложение
2. 🏗️ **Backend Architect** — проектирует API и БД
3. 🚀 **Growth Hacker** — планирует привлечение пользователей
4. ⚡ **Rapid Prototyper** — быстрые итерации
5. 🔍 **Reality Checker** — проверяет качество перед запуском

**Результат:** Быстрый запуск с экспертизой на каждом этапе.

### Сценарий 2: Запуск маркетинговой кампании

**Ваша команда:**
1. 📝 **Content Creator** — создаёт контент
2. 🐦 **Twitter Engager** — стратегия и выполнение
3. 📸 **Instagram Curator** — визуальный контент
4. 🤝 **Reddit Community Builder** — аутентичное вовлечение
5. 📊 **Analytics Reporter** — отслеживает и оптимизирует

**Результат:** Многоканальная скоординированная кампания.

### Сценарий 3: Enterprise разработка фичи

**Ваша команда:**
1. 👔 **Senior Project Manager** — планирование scope и задач
2. 💎 **Senior Developer** — сложная реализация
3. 🎨 **UI Designer** — дизайн-система
4. 🧪 **Experiment Tracker** — A/B тестирование
5. 📸 **Evidence Collector** — QA
6. 🔍 **Reality Checker** — готовность к production

**Результат:** Enterprise-уровень доставки с quality gates.

---

## Поддерживаемые инструменты

| Инструмент | Формат | Установка |
|------------|--------|-----------|
| **Claude Code** | `.md` | `./scripts/install-claude.sh` |
| **GitHub Copilot** | `.md` | `./scripts/install-copilot.sh` |
| **Cursor** | `.mdc` | `./scripts/install-cursor.sh` |
| **Aider** | `CONVENTIONS.md` | `./scripts/install-aider.sh` |
| **Gemini CLI** | Extension + `SKILL.md` | `./scripts/install-gemini.sh` |
| **OpenCode** | `.md` | `./scripts/install-opencode.sh` |
| **Windsurf** | `.windsurfrules` | `./scripts/install-windsurf.sh` |
| **Qwen Code** | `.md` SubAgents | `./scripts/install-qwen.sh` |
| **OpenClaw** | `SOUL.md` + `AGENTS.md` | `./scripts/install-openclaw.sh` |

---

## Пример использования с Claude Code

```bash
# Установить агентов
./scripts/install-claude.sh
```

```
Пользователь: Привет Claude, активируй Backend Architect

Claude (как Backend Architect): Привет! Я Backend Architect. 
Готов помочь спроектировать масштабируемую систему.

Что мы строим сегодня?

Пользователь: Мне нужно API для task management системы

Claude: Окей, давай спроектируем это правильно.

## Анализ требований
- Пользователи, проекты, задачи
- CRUD операции
- Аутентификация и авторизация

## Проектирование API

### Endpoints
```
GET    /api/users
GET    /api/users/:id
POST   /api/users
PUT    /api/users/:id
DELETE /api/users/:id

GET    /api/projects
POST   /api/projects
...
```

### Database Schema
```sql
CREATE TABLE users (
  id UUID PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  ...
);
```

## Security
- JWT аутентификация
- Rate limiting
- Input validation

Готов реализовать?
```

---

## Пример использования с Cursor

```bash
# Установить для Cursor
./scripts/install-cursor.sh
```

```
Пользователь: @security-engineer Проверь этот код на уязвимости

Cursor (как Security Engineer): Провожу security review...

## Найденные проблемы

### 🔴 CRITICAL: SQL Injection
**Файл:** `auth.js:42`
**Проблема:** Прямая конкатенация в SQL запросе
**Исправление:**
```javascript
// ❌ Плохо
const query = `SELECT * FROM users WHERE id = ${userId}`;

// ✅ Хорошо
const query = 'SELECT * FROM users WHERE id = $1';
await db.query(query, [userId]);
```

### 🟡 HIGH: XSS
**Файл:** `comments.js:15`
**Проблема:** Неэкранированный вывод пользовательского input
...

## Рекомендации
1. Использовать parameterized queries
2. Экранировать вывод
3. Добавить CSP headers
```

---

## Промпты для использования

### Быстрый старт
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/07-registry/agency-agents.md

Установи Agency Agents для Claude Code и покажи как использовать Frontend Developer
```

### Выбрать агента для задачи
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/07-registry/agency-agents.md

Мне нужен агент для [ЗАДАЧА]. Какой подойдёт из Engineering Division?
```

### Создать команду агентов
```
Прочитай https://github.com/pavelvladimirovich258614-sys/prompt-ops-playbook/blob/main/07-registry/agency-agents.md

Собери команду агентов для разработки MVP:
- Frontend
- Backend
- DevOps
- QA
```

### Использовать конкретного агента
```
Прочитай https://github.com/msitarzewski/agency-agents/blob/main/agency-agents/frontend-developer.md

Активируй Frontend Developer и помоги создать React компонент для [ОПИСАНИЕ]
```

---

## Интеграция с другими разделами

| Раздел | Как связано |
|--------|-------------|
| [01-commands](../01-commands/) | Agency Agents работают с Claude Code командами |
| [02-skills](../02-skills/) | Каждый агент — это skill с workflow |
| [04-subagents](../04-subagents/) | Agency Agents = готовые субагенты |
| [09-codex](../09-codex/) | Альтернативный каталог субагентов |

---

## Сравнение с CodeX (09-codex/)

| Agency Agents | CodeX |
|---------------|-------|
| 144+ агентов | 136+ агентов |
| Markdown-файлы | TOML-файлы |
| Универсальные (Claude, Cursor, Aider) | Только CodeX |
| 12 дивизий | 10 категорий |
| Личность + workflow | Спецификация + инструкции |

---

## Лицензия

MIT License — используйте свободно, коммерчески или лично. Указание авторства приветствуется, но не требуется.

---

## Ссылки

- **Репозиторий:** https://github.com/msitarzewski/agency-agents
- **Статья:** https://yuv.ai/blog/agency-agents
- **Reddit:** https://www.reddit.com/r/ClaudeAI

---

**Готово к использованию!** Выберите агента и начните работу. 🚀
