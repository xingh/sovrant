# Web App User Flow

A screen-by-screen walkthrough of the Sovrant Web app (Blazor Server, `http://localhost:5100`), captured from a live run of version 2.1.0 in embedded mode with a fresh database and no provider configured. Each image shows dark mode on the left and light mode on the right (1440×900 each). All screenshots are in [`docs/images/`](images/) with the `web-flow-` prefix.

The screens are in the order a new user meets them: first-run setup, Chat, Home, then the Knowledge, Agents and Projects sections, Settings and provider setup, and finally the Admin pages.

---

## 1. First-run: create the administrator account

**Route:** `/login`

On a fresh install no accounts exist, so the login page switches to first-time setup: the first account created becomes the administrator, with control over registration, approvals, providers and workspaces. After that, this page shows the normal sign-in form.

![Login — first-run setup](images/web-flow-01-login-first-run.png)

## 2. Chat

**Route:** `/`

The empty state asks "What are you working on?" and offers starter prompts (custom agent, research team, swarm, workflow, multi-agent pipeline, MCP server). Below them is a "What Sovrant can do" strip. The top bar has the model picker ("No model · Add a provider" until a provider exists), the workspace and project selectors, and the Integrations menu. The sidebar lists conversations, with search and folders. The composer has a **Private** toggle and a **+ Remember** control.

![Chat](images/web-flow-02-chat.png)

## 3. Home

**Route:** `/dashboard` (rail: Home; `/welcome` redirects here)

"Welcome back" overview: activity counters, a role-aware "Set up Sovrant for your team" checklist (connect a model provider, enable providers for a workspace, add your team, connect an integration, create your first agent), and "What Sovrant can do" cards. The Activity tab shows cross-workspace activity.

![Home](images/web-flow-03-dashboard.png)

## Knowledge section

### 4. Memory — `/memory`

Notes, patterns, incidents and summaries that agents recall across sessions. Each entry can be marked private.

![Memory](images/web-flow-04-memory.png)

### 5. Documents — `/documents`

Built-in document templates (business, construction, education, …) with output formats; select one to view its details.

![Documents](images/web-flow-05-documents.png)

### 6. Document Templates — `/documents/templates`

User-defined document templates (**+ New** to create).

![Document Templates](images/web-flow-06-document-templates.png)

### 7. Artifacts — `/artifacts`

Files produced by agent runs, grouped per run.

![Artifacts](images/web-flow-07-artifacts.png)

### 8. Code Templates — `/guidelines`

Per-language coding conventions (.NET, C++, Go, Java, Kotlin, Python, Rust, …) that agents follow.

![Code Templates](images/web-flow-08-guidelines.png)

## Agents section

### 9. Library — `/agents`

Built-in agent templates with their tier and tool set, plus recent agent runs.

![Agents](images/web-flow-09-agents.png)

### 10. Skills — `/skills`

The built-in skill catalog with agent and tool counts per skill.

![Skills](images/web-flow-10-skills.png)

### 11. Tools — `/tools`

Every built-in tool, with a description of each.

![Tools](images/web-flow-11-tools.png)

### 12. Tool Templates — `/tools/templates`

Tool templates (e.g. CodeCreate, CodeCreateMulti, CodeValidate).

![Tool Templates](images/web-flow-12-tool-templates.png)

### 13. Orchestration — `/orchestration`

Teams and their default run profiles.

![Orchestration](images/web-flow-13-orchestration.png)

### 14. Workflows — `/workflows`

Planned and scheduled workflows.

![Workflows](images/web-flow-14-workflows.png)

## Projects

### 15. Projects — `/projects`

Create and list projects.

![Projects](images/web-flow-15-projects.png)

### 16. Workspaces — `/workspaces`

The user's workspaces (Personal by default), with a form to create a team workspace.

![Workspaces](images/web-flow-16-workspaces.png)

### 17. Code Scaffolds — `/code`

Project scaffolds per stack (C++ CMake, Blazor Server, .NET Console/Web API/Worker, Go, Java, Node, …).

![Code Scaffolds](images/web-flow-17-code.png)

## Settings and provider setup

### 18. Settings — `/settings`

Permission mode, dark/light theme, and sign-out (this browser or all browsers).

![Settings](images/web-flow-18-settings.png)

### 19. Provider setup — `/setup`

"Welcome to Sovrant": pick a provider, enter an API key and base URL, then **Get Started**.

![Provider setup](images/web-flow-19-provider-setup.png)

## Admin

### 20. Command Center — `/command`

Live counts of workflows, team runs, agent runs, sessions and Claws, plus what is currently in flight.

![Command Center](images/web-flow-20-command-center.png)

### 21. Users — `/admin`

User list with role and status, plus tabs for Registration & sign-in and Password Reset.

![Users](images/web-flow-21-admin.png)

### 22. Providers — `/admin/providers`

Configured LLM providers and an Add Provider form, scoped to workspaces.

![Providers](images/web-flow-22-admin-providers.png)

### 23. Platform Integrations — `/admin/integrations`

MCP servers (connected and gallery), with import via JSON, stdio or HTTP.

![Platform Integrations](images/web-flow-23-admin-integrations.png)

### 24. System Integrations — `/admin/system-integrations`

The active storage backend (SQLite by default) and optional PostgreSQL and Supabase connections.

![System Integrations](images/web-flow-24-admin-system-integrations.png)

### 25. Workspaces (admin) — `/admin/workspaces`

All team workspaces and the personal-workspace defaults.

![Admin Workspaces](images/web-flow-25-admin-workspaces.png)

### 26. Governance — `/governance`

Governance level, audit logging, file/shell permissions, blocked commands, protected files and secret-detection patterns.

![Governance](images/web-flow-26-governance.png)

### 27. Diagnostics — `/diagnostics`

System info, health checks (API key, database, artifacts directory, connectivity), provider health and paths.

![Diagnostics](images/web-flow-27-diagnostics.png)

### 28. Trust Boundary — `/trust-boundary`

Master switch, sanitizer mode, corporate domains, allow list, exempt providers, custom patterns and intent verification.

![Trust Boundary](images/web-flow-28-trust-boundary.png)
