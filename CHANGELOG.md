# Changelog

## [1.0.0] - 2026-03-23

### Added
- Initial release of Prompt Ops Playbook
- 9 modular sections covering commands, skills, MCP, subagents, troubleshooting, glossary, registry, prompts, and CodeX
- 136+ CodeX subagents catalog
- Knowledge cards from 9 source repositories
- 4 learning paths for different skill levels
- Cross-links between related concepts
- Agent architecture documentation

### Sections

#### 01-commands
- Slash commands for Claude Code (/usage, /chrome, /mcp, /stats, /clear, /compact, /context, /config, /plan, /copy)
- DX Plugin commands (/dx:clone, /dx:half-clone, /dx:handoff, /dx:gha, /dx:reddit-fetch, /dx:review-claudemd)
- Skills documentation (clone, gha, half-clone, handoff, reddit-fetch, review-claudemd)
- chub CLI commands (search, get, annotate, feedback)

#### 02-skills
- Skill concept and structure
- Workflow concept (7 core workflows)
- Subagent-driven development
- Test-Driven Development (RED-GREEN-REFACTOR)
- Brainstorming skill
- Writing plans skill
- Systematic debugging skill
- Git worktrees skill

#### 03-mcp
- Context7 platform overview
- ctx7 CLI commands
- MCP server integration
- MCP configuration for Cursor, Claude, Windsurf, VS Code
- resolve-library-id tool
- query-docs tool

#### 04-subagents
- Agent loop concept
- Tools and function calling
- Todo and planning system
- Subagents and delegation
- Skills system
- Context compression
- Task system
- Agent teams
- Agent harness
- Filesystem backend
- Context management

#### 09-codex
- CodeX ecosystem overview
- 136+ subagents catalog (10 categories)
- Subagent TOML specification template
- Workflow patterns
- Integration notes
- Troubleshooting guide

### Source Repositories
- awesome-codex-subagents
- claude-code-tips
- context7
- learn-claude-code
- superpowers
- deepagents
- page-agent
- context-hub
- supersearch

### Documentation
- README.md with quick start guide
- INDEX.md with navigation
- PLAYBOOK.md with Prompt Ops methodology
- AGENTS.md with agent architecture
- LICENSE (MIT)
- CONTRIBUTING.md with contribution guidelines
- CROSS_LINKS_REPORT.md with link analysis
- LEARNING_PATHS.md with 4 learning paths
- RELEASE_REPORT.md with release statistics

## [1.1.0] - 2026-03-23

### Added
- **Agency Agents** documentation (144+ specialized agents from msitarzewski/agency-agents)
  - 12 divisions: Engineering, Design, Paid Media, Sales, Marketing, Product, Project Management, Testing, Support, Spatial Computing, Specialized, Game Development
  - Multi-tool support: Claude Code, Cursor, Aider, Copilot, Gemini CLI, OpenCode, Windsurf, Qwen Code, OpenClaw
  - Real-world use cases and examples
- New Learning Path: **Agency Agents Mastery** (3-5 hours)
- Updated INDEX.md with 07-registry section
- Updated README.md with Agency Agents information
- Added agency-agents to source repositories list

### Updated
- README.md: Added 144+ Agency Agents to statistics
- INDEX.md: Added 07-registry/agency-agents.md link
- Statistics: 20 files, 10 repositories, 5 learning paths

## [1.1.1] - 2026-03-23

### Changed
- **README.md**: Master Prompt is now the FIRST and RECOMMENDED way to start
  - Added prominent warning block at the top
  - Moved Master Prompt to "Вариант 1" (was "Вариант 4")
  - Added clear instructions how to use
- **INDEX.md**: Enhanced "СТАРТУЙ ЗДЕСЬ" section
  - Added warning that Master Prompt should be used FIRST
  - Added step-by-step instructions
  - Added benefits list
- **MASTER_PROMPT.md**: Already exists and ready to use

### Why this change?
Users should start with Master Prompt to get the best experience:
- AI automatically suggests commands
- MCP servers are connected automatically
- Agency Agents are used from the knowledge base
- AI acts as an experienced Senior Developer

## [1.1.2] - 2026-03-23

### Added
- **Claude Code Commands Cheatsheet** (01-commands/claude-code-commands-cheatsheet.md)
  - 50+ команд Claude Code с описанием
  - Project Setup & Memory (/init, /memory, /add-dir)
  - Context & Session Lifecycle (/compact, /clear, /context)
  - Code Review & Quality (/diff, /simplify, /review)
  - CLI Flags (claude, --print, --continue, --effort)
  - System & Diagnostics (/config, /doctor, /permissions)
  - Model Controls (/model, /effort, /fast, /plan)
  - Monitoring (/cost, /export, /usage-report)
  - Inline Prefixes (@path, !command, #text)
  - Multi-Agent & Automation (/agents, /batch, /loop)
  - Keyboard Shortcuts (Shift+Tab, Ctrl+R, etc.)
- **Color Expert Skill** (02-skills/skill-color-expert.md)
  - Claude Code-скилл для работы с цветом
  - 113 справочных файлов
  - 286 000 слов о науке о цвете
  - От работ Гельмгольца (1856) до OKLCH
  - Установка: git clone https://github.com/meodai/skill.color-expert

### Updated
- **README.md**: Updated statistics (22 files), added Color Expert and commands cheatsheet
- **INDEX.md**: Added links to new files in 01-commands and 02-skills sections
- **Source repositories**: Added meodai/skill.color-expert

## Future Enhancements

### Planned for v1.2.0
- Fill 05-troubleshooting section with common issues
- Add 06-glossary with terminology
- Create 08-prompts with prompt templates
- Add more code examples
- Expand troubleshooting guides

### Planned for v1.3.0
- Integration with more MCP servers
- Additional subagent patterns
- Video tutorials
- Interactive examples
- Community contributions

---

**Total Files:** 83 Markdown files  
**Total Size:** ~644 KB  
**Knowledge Cards:** 76+ objects  
**CodeX Subagents:** 136+ catalogued
