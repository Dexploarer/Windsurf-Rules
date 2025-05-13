# Performance Guidelines

## General
- Optimize for responsiveness and resource efficiency on all platforms (Windows, Mac, Linux).
- All code must be profiled and optimized for startup time and runtime performance.
- Avoid unnecessary re-renders and memory leaks in React components.
- Use lazy loading and code splitting for large modules and assets.

## Electron
- Minimize main process workload; offload heavy computation to worker threads or external processes.
- Use hardware acceleration where appropriate, but disable for security if not needed.
- Monitor and limit memory/CPU usage of all windows and processes.

## React
- Use memoization (`React.memo`, `useMemo`, `useCallback`) to avoid unnecessary renders.
- Use virtualization for large lists/tables (e.g., react-virtualized, react-window).
- Avoid deep prop drilling; use context or state libraries for global state.
- Debounce or throttle expensive operations (search, API calls, etc.).

## Node.js
- Use asynchronous I/O for all file and network operations.
- Avoid blocking the event loop; use worker threads for CPU-bound tasks.
- Monitor and optimize event loop lag and memory consumption.

## API/LLM/Media
- Batch and cache API requests where possible.
- Use streaming APIs for large responses (LLM, media generation).
- Implement retry, backoff, and circuit breaker patterns for reliability.

## Testing
- All performance-sensitive code must have benchmarks and regression tests.
- Monitor and report performance metrics in CI/CD.

## Documentation
- All performance-critical modules must document bottlenecks, optimization strategies, and known limitations.
