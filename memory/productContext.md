# Product Context

## Project Scope
A cross-platform desktop chat and project management hub, supporting pluggable LLMs (OpenAI, Anthropic, Gemini, Grok, Groq), media generation (OpenAI, FAL), research tools, and full coding project management with Git integration.

## Core Components
- Electron Main Process (window management, secure API, system integration)
- React Renderer (UI, dark mode, modern UX)
- Secure API Key Management (Keytar/OS keychain)
- LLM/Media Service Layer (OpenAI, Anthropic, Gemini, Grok, Groq, FAL)
- Project Dashboard (create/open/manage coding projects)
- Git Service (NodeGit abstraction, never direct CLI)
- Project Management (tasks, Kanban, notes, deadlines)
- Research Tools (web search, notes, citation management)
- Media Generation (image/audio/video via OpenAI, FAL)
- Local Data (SQLite, encrypted)
- Optional Cloud Sync (future extension)
- Memory/Progress/Decision Logging (Windsurf .md files)

## Architecture
- Strict separation of main and renderer (secure IPC, contextIsolation)
- Modular, pluggable provider pattern for LLM/media APIs
- All sensitive data handled in main process, never exposed to renderer
- All API/service logic in dedicated modules, fully typed
- All state and configuration persisted locally (SQLite, encrypted)
- All Git operations abstracted and secured
- All workflows, rules, and compliance enforced via .md files and scripts

## Organizational Structure
- Feature modules: chat, project management, research, media, settings
- Service modules: LLM/media, git, storage, API key, sync
- UI modules: dashboard, sidebar, chat window, project/task views, research/media panels

## Compliance
- All features, code, and workflows adhere to Windsurf Master Global Rules and workspace overrides
- All memory and progress files updated at each milestone
- All technical decisions logged in ADRs and decisionLog.md
