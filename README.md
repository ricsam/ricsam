# Richie / `ricsam`

I build tools that make complex systems feel predictable.

My work usually starts with a concrete problem, finds the reusable primitive inside it, then follows that primitive until the pieces form a stack.

## Current systems

### Agents with explicit capabilities

[`agentic-web-research`](https://github.com/ricsam/agentic-web-research) searches with SearXNG, renders selected pages in Playwright, converts them to Markdown, and streams model-guided research through an authenticated API.

[`isolate`](https://github.com/ricsam/isolate) runs JavaScript and TypeScript in V8 contexts whose files, modules, network access, browser sessions, and host functions are supplied as bindings. [`shell-dsl`](https://github.com/ricsam/shell-dsl) adds in-process pipes, redirects, scripts, registered commands, and a virtual filesystem.

### A typed Bun/React web stack

[`richie-rpc`](https://github.com/ricsam/richie-rpc) derives server validation, typed clients, OpenAPI, React Query options, streaming, SSE, and WebSockets from Zod contracts.

[`richie-router`](https://github.com/ricsam/richie-router) generates a React route tree and a separate server-safe manifest, so the backend can match SPA routes and resolve document head tags without executing frontend modules.

### Data interfaces in separate layers

[`react-tanstack-table-ui`](https://github.com/ricsam/react-tanstack-table-ui) renders virtualized TanStack tables with interchangeable skins. [`selection-manager`](https://github.com/ricsam/selection-manager) owns selection, navigation, editing, fill, merged cells, and clipboard behavior independently of the renderer. [`formula-engine`](https://github.com/ricsam/formula-engine) provides sparse workbook storage, A1 addressing, sheets, and named expressions while formula evaluation is developed.

### Files and scheduled work

[`nafs`](https://github.com/ricsam/nafs) presents a Node-style filesystem over memory, local disk, S3, and [`enstore`](https://github.com/ricsam/enstore). Enstore exposes streamed file operations over HTTP with users, roles, a CLI, and an `fs`-style client.

[`enschedule`](https://github.com/ricsam/enschedule) stores schedules and runs in PostgreSQL. Workers register typed jobs, claim work, and publish status and logs to the dashboard; Nafs keeps the worker-facing storage API consistent between local and remote deployments.

## Working backwards

The current agent runtimes build on typed application infrastructure developed in 2025–26. That work followed the data interface packages and the storage and scheduling stack. Earlier React libraries and command-line tools established the same pattern: put stateful mechanics in focused packages and leave presentation and deployment to the application.

[Read the full story on the portfolio site →](https://ricsam.github.io/ricsam/)
