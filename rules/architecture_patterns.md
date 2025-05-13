# Architecture Patterns

## General Principles
- Modular, layered architecture: clear separation between UI (renderer), backend logic (main), and API/data layers.
- Use dependency injection for all services and integrations.
- All modules must be independently testable and replaceable.
- All business logic must be encapsulated in service classes or hooks, not in UI components.

## Electron
- Main process handles window management, system-level APIs, and secure IPC.
- Renderer process is sandboxed; communicates with main only via secure, validated IPC channels.
- All native integrations (file system, key storage, git, etc.) are handled in main, never exposed directly to renderer.

## React
- Strict separation of presentational and container components.
- Use React context for global state, but extract complex logic to custom hooks or services.
- All UI state must be serializable for debugging and persistence.

## API/LLM Integrations
- All external API calls are routed through a dedicated service layer.
- API keys and secrets are never exposed to the UI; always handled in main process and passed via secure IPC.
- Pluggable provider pattern for LLM/media APIs (OpenAI, Anthropic, Gemini, Grok, Groq, FAL, etc.).
- All API responses are validated and sanitized before use.

## Project Management & Git
- Each project is a self-contained workspace with its own config, git repo, and metadata.
- Git operations are abstracted via a service and never called directly from UI.

## Extensibility
- All major features (chat, project management, research, media) are implemented as independent modules/plugins.
- New LLM/media providers can be added by implementing a provider interface and registering with the service layer.

## Security
- All IPC channels are validated and have strict input/output schemas.
- No direct access to Node.js APIs from renderer.
- All sensitive operations are audited and logged.

## Testing
- Each module must have its own test suite and mocks for all external dependencies.

## Documentation
- All modules must have architecture diagrams and usage docs in `/docs`.
