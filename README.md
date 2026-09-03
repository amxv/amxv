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

The systems I trust make their important boundaries explicit: one owner for state, typed contracts between layers, observable failures, and a verifier at the end of every autonomous loop. That discipline is what lets me move quickly without treating agent output as ground truth.

## Open source

### Agent runtimes, coordination, and protocols

- **[Gooselake](https://github.com/amxv/gooselake)** · `Rust` · [docs](https://gooselake.ashray.xyz): A headless runtime for Codex, Claude, and ACP with durable sessions, replayable SSE, background processes, worktree execution, recovery, and receipt-backed team messaging.
- **[Zodex](https://github.com/amxv/zodex)** · `Rust` · [docs](https://zodex.ashray.xyz): A tool that gives ChatGPT a real terminal on your Mac, so it can work with your existing files, tools, and credentials while you watch everything it does in Liveboard. The same setup can also run on a remote Linux workspace.
- **[Agentbox](https://github.com/amxv/agentbox)** · `Go` `TypeScript` · [app](https://agentbox.ashray.xyz): A shared inbox where remote agents connect over MCP and local agents use a Go CLI, backed by Postgres and R2, with a Next.js inbox UI and a Raycast extension for macOS.

### Agent-first developer tools

- **[Denju](https://github.com/amxv/denju)** · `Rust` · [docs](https://denju.ashray.xyz): An open registry and synchronization system for Agent Skills: discover and subscribe publicly, keep private skills synced across devices, bundle them into packs, and keep team skill sets current while projecting one managed copy into Codex and Claude Code.
- **[agentscript](https://github.com/amxv/agentscript)** · `Go` · [docs](https://agentscript.ashray.xyz): A CLI that turns Claude Code and Codex transcripts into clean, searchable handoffs, so agents can carry forward the useful context without passing around the whole session.
- **[webctx](https://github.com/amxv/webctx)** · `Go` · [docs](https://webctx.ashray.xyz): A web search and page scraping CLI that queries Brave, Tavily, and Exa concurrently, merges and ranks their results, extracts pages into context-efficient Markdown, and maps sites into URL inventories.
- **[Fidelius](https://github.com/amxv/fidelius)** · `Go` `Swift` · [docs](https://fidelius.ashray.xyz): A tiny desktop tool that lets agents ask you for secrets when they need them, then gives them short-lived private files they can use without exposing the values in chat or terminal output.
- **[cargo-warm](https://github.com/amxv/cargo-warm)** · `Rust` · [docs](https://cargowarm.ashray.xyz): A CLI that makes new Rust worktrees start warm by reusing build state from an existing checkout while keeping each worktree's Cargo cache private.
- **[cf-cli](https://github.com/amxv/cf-cli)** · `Go` · [docs](https://cf.ashray.xyz): An agent-first Cloudflare operations CLI for DNS, recent Workers logs, R2, account profiles, Wrangler switching, and minting narrowly scoped tokens for API operations it does not wrap yet.
- **[icloud-cli](https://github.com/amxv/icloud-cli)** · `Go` · [docs](https://icloud.ashray.xyz): A CLI for Apple's iCloud ecosystem, with a comprehensive iCloud Mail client for account setup, synchronization, search, reading, attachments, drafts, sending, organization, import/export, S/MIME, recovery, and automation.
- **[spaceship-cli](https://github.com/amxv/spaceship-cli)** · `Go` · [npm](https://www.npmjs.com/package/spaceship-domains-cli): A least-privilege Spaceship.com domains and DNS CLI whose binary intentionally contains no domain transfer, registration, or deletion capability.
- **[procoder](https://github.com/amxv/procoder)** · `Go`: A CLI for getting real Git commits out of ChatGPT's locked-down sandbox: it exports a sanitized offline repo, then verifies and imports only the new history with `git bundle`.
- **[ZueDocs](https://github.com/amxv/zuedocs)** · `Astro` `TypeScript` · [demo](https://zuedocs.vercel.app): A versioned documentation shell and scaffold CLI shared across my projects, with raw Markdown routes, Mermaid, theme support, page actions, and automated npm releases.

### AI products and full-stack applications

- **[Zodega](https://github.com/amxv/zodega)** · `Next.js` `PostgreSQL` · [app](https://ecom.ashray.xyz): A mult-vendor apparel marketplace with storefront, seller, and admin surfaces, plus realtime voice shopping, generative product search, reference-photo try-on, and AI media workflows over one commerce model.
- **[Icephone](https://github.com/amxv/icephone)** · `Next.js` `PostgreSQL` · [app](https://icephone.ashray.xyz): A self-hosted voice agents platform with configurable agents, a CRM, cold-calling campaigns, queues, scheduling, and Twilio, Telnyx, and Vonage behind a durable call-lifecycle model.
- **[HR Agent](https://github.com/amxv/hr-agent)** · `Next.js` `PostgreSQL` · [app](https://hr-agent.ashray.xyz): An enterprise HR assistant with tool-layer RBAC, RAG, auditable conversations, leave and approval flows, SLA-aware cases, budgets, and model observability.
- **[AgentStudio](https://github.com/amxv/agentstudio)** · `Next.js` `PostgreSQL` · [app](https://agentstudio.ashray.xyz): An agentic image studio where a chat model operates multiple image models for you, automatically routing between generation and editing while preserving every result as a versioned artifact.
- **[Product Pics](https://github.com/amxv/product-pics)** · `Next.js` `PostgreSQL` · [app](https://product-pics.ashray.xyz): A batch apparel-photo pipeline for turning up to 100 flat product images into varied lifestyle shots, with direct R2 uploads, asynchronous generation, per-image retries, and zip export.
- **[Presentation AI](https://github.com/amxv/presentation-ai)** · `Next.js` `PostgreSQL` · [app](https://presentation.ashray.xyz): An AI presentation maker that turns long-form source material into designed slide decks: a reasoning model plans the narrative and theme, then an image model renders each slide as a complete visual composition.
- **[Digital Business Cards](https://github.com/amxv/digital-business-cards)** · `Next.js` `PostgreSQL` · [app](https://businesscards.ashray.xyz): A white-label platform for managed contact profiles, branded QR and NFC entry points, mobile public pages, and one-tap vCard downloads that work across Android and iOS.
- **[ChatGPT App Template](https://github.com/amxv/chatgpt-app-template)** · `Next.js` `MCP` · [demo](https://gg-chatgpt-app.vercel.app): A starter for OpenAI Apps SDK products with the MCP metadata, iframe asset handling, cross-origin RSC support, browser patches, and a working tool-to-widget example already wired.

## Selected writing

- [Git is my multi-agent protocol](https://ashray.xyz/blog/git-is-my-multi-agent-protocol): Why exact commit ranges, cherry-pick, and disposable integration branches became the coordination layer underneath my agent teams.
- [Find the verifier](https://ashray.xyz/blog/find-the-verifier): A model of agent work built around objective gates, fresh reviewer contexts, and the rule that implementers never certify their own output.
- [The frontend was harder than the runtime](https://ashray.xyz/blog/the-frontend-was-harder-than-the-runtime): What happens when a React frontend becomes a replica and scheduler for dozens of concurrent, history-rewriting streams.
- [Every harness gets background processes wrong](https://ashray.xyz/blog/every-harness-gets-background-processes-wrong): Why long commands need owned lifecycles, observable logs, and completion-driven wakeups instead of polling inside an agent turn.
- [The answer is almost always a CLI](https://ashray.xyz/blog/the-answer-is-almost-always-a-cli): Where CLI priors, context cost, self-documentation, and MCP's stateful identity lead to different tool choices.
- [Agents don't pay the Rust tax](https://ashray.xyz/blog/agents-dont-pay-the-rust-tax): Why Rust's compile-fix loop becomes a correctness subsidy when agents write the code and durable state is on the line.

If the difficult part of your product lives between the model, the runtime, and the person using it, [send me a note](mailto:a@ashray.xyz).
