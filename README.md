<div align="center">

# Ashray

**AI systems and product engineer**

I build the infrastructure, tools, and product surfaces that turn model capability into dependable software.

[Website](https://ashray.xyz) · [Projects](https://ashray.xyz/projects) · [Writing](https://ashray.xyz/blog) · [LinkedIn](https://linkedin.com/in/ashraym) · [Email](mailto:a@ashray.xyz)

</div>

My work sits across two layers that are usually treated separately. I build agent runtimes with durable state, typed provider boundaries, replayable events, permission controls, process execution, delivery receipts, and recovery. I also build the products on top: voice systems, commerce, enterprise assistants, image workflows, and the interfaces that make autonomous behavior understandable, trustworthy, and delightful to use.

Right now, my main project is [goldengoose](https://goldengoose.ashray.xyz), a native desktop environment for running teams of coding agents in parallel. I use it every day to build itself and the rest of the projects below. I extracted its runtime lessons into [Gooselake](https://github.com/amxv/gooselake), a headless control plane for agent applications.

## What I work on

| Area | Technical focus |
| --- | --- |
| Agent infrastructure | Durable sessions, state machines, event replay, recovery, provider abstraction, MCP, SSE, worktrees, background processes, and agent-to-agent delivery |
| Developer tools | Go CLIs, single-binary distribution, Git and GitHub automation, API adapters, least-privilege credentials, and tag-driven releases |
| AI products | Tool-calling agents, realtime voice over WebRTC, RAG, generative UI, image pipelines, multi-tenant applications, and operational dashboards |
| Product engineering | TypeScript, React, Next.js, PostgreSQL, SQLite, Drizzle, object storage, typed contracts, observability, and browser-level verification |
| Systems engineering | Rust, Tauri, Axum, bounded concurrency, lifecycle invariants, idempotency, delivery semantics, and failure recovery |

My default is to make important boundaries explicit: one owner for state, typed contracts between layers, observable failures, and a verifier at the end of every autonomous loop. That discipline is what lets me move quickly without treating agent output as ground truth.

## Open source

### Agent runtimes, coordination, and protocols

- **[Gooselake](https://github.com/amxv/gooselake)** · `Rust` · [docs](https://gooselake.ashray.xyz): A headless runtime for Codex, Claude, and ACP with durable sessions, replayable SSE, background processes, worktree execution, recovery, and receipt-backed team messaging.
- **[Zodex](https://github.com/amxv/zodex)** · `Rust` · [docs](https://zodex.ashray.xyz): A remote coding MCP server that gives ChatGPT a real Linux workspace through the three Codex-native tools, with separate operator and agent binaries enforcing the permission boundary.
- **[Agentbox](https://github.com/amxv/agentbox)** · `Go` `TypeScript` · [app](https://agentbox.ashray.xyz): A shared inbox where remote agents connect over MCP, local agents connect through a Go CLI, and both exchange threads, messages, and files through Postgres and R2.
- **[mcp-code](https://github.com/amxv/mcp-code)** · `Go`: A small stateless MCP server that gives remote AI clients a deliberately tight GitHub surface for repository discovery, code search, reading, issues, pull requests, branches, and light writes.
- **[Terminal MCP](https://github.com/amxv/terminal-mcp)** · `TypeScript` `Bun`: A zero-dependency MCP client built when Codex had no native MCP support, with a full developer binary and a separate locked-down binary that can only call approved tools.
- **[MCP Manager](https://github.com/amxv/mcp-manager)** · `TypeScript` · [app](https://mcp-manager.ashray.xyz): An early, entirely client-side GUI for configuring Claude Desktop MCP servers without sending the API tokens in its config file to a backend.
- **[adm](https://github.com/amxv/adm)** · `Go` `SQLite` · archived: The local, poll-free agent messaging CLI that explored at-least-once delivery, passive hook injection, direct messages, broadcasts, and soft file claims before those ideas moved into goldengoose.

### Agent-first developer tools

- **[agentscript](https://github.com/amxv/agentscript)** · `Go` · [docs](https://agentscript.ashray.xyz): A terminal reader that normalizes Claude Code and Codex JSONL into stably addressed blocks, then exports small, context-efficient Markdown handoffs instead of raw transcript noise.
- **[webctx](https://github.com/amxv/webctx)** · `Go` · [docs](https://webctx.ashray.xyz): A research CLI that queries Brave, Tavily, and Exa concurrently, merges and ranks their results, extracts pages as clean Markdown, and maps sites into URL inventories.
- **[cf-cli](https://github.com/amxv/cf-cli)** · `Go` · [docs](https://cf.ashray.xyz): An agent-first Cloudflare operations CLI for DNS, recent Workers logs, R2, account profiles, Wrangler switching, and minting narrowly scoped tokens for API operations it does not wrap yet.
- **[cricinfo-cli](https://github.com/amxv/cricinfo-cli)** · `Go` · [docs](https://cricinfo-docs.vercel.app): A cricket analytics CLI that turns ESPN Cricinfo's undocumented API into parallel, paginated queries across matches, players, leagues, ball-by-ball data, pitch maps, and derived analysis.
- **[spaceship-cli](https://github.com/amxv/spaceship-cli)** · `Go` · [npm](https://www.npmjs.com/package/spaceship-domains-cli): A least-privilege Spaceship.com domains and DNS CLI whose binary intentionally contains no domain transfer, registration, or deletion capability.
- **[Actions Watcher](https://github.com/amxv/actions-watcher)** · `Go`: A fail-fast GitHub Actions monitor that lets an agent block once and resume on the first useful signal instead of spending turns polling a doomed workflow.
- **[procoder](https://github.com/amxv/procoder)** · `Go`: A Git-native bridge that sends a sanitized repository into ChatGPT's offline coding sandbox and brings back verified, incremental commits through `git bundle`.
- **[apply-patch-go](https://github.com/amxv/apply-patch-go)** · `Go`: A behaviorally faithful port of Codex's Rust `apply_patch`, checked against the upstream test corpus so parsing, fuzzy matching, file operations, CLI behavior, and failure semantics stay compatible.
- **[ZueDocs](https://github.com/amxv/zuedocs)** · `Astro` `TypeScript` · [demo](https://zuedocs.vercel.app): A versioned documentation shell and scaffold CLI shared across my projects, with raw Markdown routes, Mermaid, theme support, page actions, and automated npm releases.

### AI products and full-stack applications

- **[Zodega](https://github.com/amxv/zodega)** · `Next.js` `PostgreSQL` · [app](https://ecom.ashray.xyz): An open-source apparel marketplace with storefront, seller, and admin surfaces, plus realtime voice shopping, generative product search, reference-photo try-on, and AI media workflows over one commerce model.
- **[Icephone](https://github.com/amxv/icephone)** · `Next.js` `PostgreSQL` · [app](https://icephone.ashray.xyz): A self-hosted voice operations platform with configurable agents, a CRM, campaigns, queues, scheduling, and Twilio, Telnyx, and Vonage behind a durable call-lifecycle model.
- **[HR Agent](https://github.com/amxv/hr-agent)** · `Next.js` `PostgreSQL` · [app](https://hr-agent.ashray.xyz): An enterprise HR assistant with tool-layer RBAC, cited retrieval, auditable conversations, leave and approval flows, SLA-aware cases, budgets, and model observability.
- **[AgentStudio](https://github.com/amxv/agentstudio)** · `Next.js` `PostgreSQL` · [app](https://agentstudio.ashray.xyz): A conversational image studio where an LLM plans generations and edits while deterministic code owns model selection, capability routing, provider parameters, persistence, and artifact history.
- **[Product Pics](https://github.com/amxv/product-pics)** · `Next.js` `PostgreSQL` · [app](https://product-pics.ashray.xyz): A batch apparel-photo pipeline for turning up to 100 flat product images into varied lifestyle shots, with direct R2 uploads, asynchronous generation, per-image retries, and zip export.
- **[Presentation AI](https://github.com/amxv/presentation-ai)** · `Next.js` `PostgreSQL` · [app](https://presentation.ashray.xyz): A presentation maker where a reasoning model plans the narrative and visual system, an image model renders complete slides, and the product handles parallel jobs, editing, history, SSE progress, and PDF export.
- **[Digital Business Cards](https://github.com/amxv/digital-business-cards)** · `Next.js` `PostgreSQL` · [app](https://businesscards.ashray.xyz): A white-label platform for managed contact profiles, branded QR and NFC entry points, mobile public pages, and one-tap vCard downloads that work across Android and iOS.
- **[ChatGPT App Template](https://github.com/amxv/chatgpt-app-template)** · `Next.js` `MCP` · [demo](https://gg-chatgpt-app.vercel.app): A starter for OpenAI Apps SDK products with the MCP metadata, iframe asset handling, cross-origin RSC support, browser patches, and a working tool-to-widget example already wired.

## Selected writing

- [Git is my multi-agent protocol](https://ashray.xyz/blog/git-is-my-multi-agent-protocol): Why exact commit ranges, cherry-pick, and disposable integration branches became the coordination layer underneath my agent teams.
- [Find the verifier](https://ashray.xyz/blog/find-the-verifier): A model of agent work built around objective gates, fresh reviewer contexts, and the rule that implementers never certify their own output.
- [The frontend was harder than the runtime](https://ashray.xyz/blog/the-frontend-was-harder-than-the-runtime): What happens when a React frontend becomes a replica and scheduler for dozens of concurrent, history-rewriting streams.
- [Every harness gets background processes wrong](https://ashray.xyz/blog/every-harness-gets-background-processes-wrong): Why long commands need owned lifecycles, observable logs, and completion-driven wakeups instead of polling inside an agent turn.
- [The answer is almost always a CLI](https://ashray.xyz/blog/the-answer-is-almost-always-a-cli): Where CLI priors, context cost, self-documentation, and MCP's stateful identity lead to different tool choices.
- [Agents don't pay the Rust tax](https://ashray.xyz/blog/agents-dont-pay-the-rust-tax): Why Rust's compile-fix loop becomes a correctness subsidy when agents write the code and durable state is on the line.

I am based in Bangalore, India, and open to staff engineer and founding engineer roles, plus a small amount of focused client work. If the difficult part of your product lives between the model, the runtime, and the person using it, [send me a note](mailto:a@ashray.xyz).
