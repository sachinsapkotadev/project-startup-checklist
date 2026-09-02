# Project Startup Checklist

**Last Updated:** September 2, 2026

A complete, step-by-step checklist for starting, building, testing, securing, and deploying software projects with AI coding tools. Never forget a single setup step again.

**Use case:** You open OpenCode, drop your project idea, and follow the checklist from idea to production — no missed steps, no forgotten config, no "oh wait, I forgot env vars."

---

## The Workflow

```
PROJECT IDEA
    ↓
Planning
    ↓
Tech Stack
    ↓
AI Skills
    ↓
MCP Servers
    ↓
LSPs
    ↓
Plugins
    ↓
Project Initialization
    ↓
Dependencies
    ↓
Git + GitHub
    ↓
Environment Variables
    ↓
UI/UX
    ↓
Development
    ↓
Testing
    ↓
Security
    ↓
SEO
    ↓
Performance
    ↓
Production Build
    ↓
Deployment
    ↓
Domain + DNS + SSL
    ↓
Analytics
    ↓
Final QA
    ↓
Launch
    ↓
Maintenance
```

---

## Quick Start

| Guide | What It Covers |
|-------|----------------|
| [Guide 1 — Step by Step](Guide%201.md) | Full checklist from idea to launch, 22 phases with checkboxes |
| [Guide 2 — Prompts & Resources](Guide%202.md) | Prompt templates, tool links, AI skill installs, MCP configs |

---

## Why This Exists

- **AI coding tools are fast but chaotic** — Claude Code, Cursor, Gemini CLI, OpenCode all ship features fast, but they don't remind you to set up env vars, configure DNS, or add security headers
- **This checklist fills the gap** — it's the thing you keep open while you build, so nothing slips through
- **Works with any stack** — not tied to one framework. Astro, Next.js, React, Django, Go, Rust — the checklist adapts
- **Works with any AI tool** — OpenCode, Claude Code, Cursor, Copilot, Windsurf — the prompts are portable

---

## What Each Phase Covers

| Phase | What You Do | Why It Matters |
|-------|-------------|----------------|
| **Project Idea** | Validate the idea, find competitors, define scope | Build something people actually want |
| **Planning** | Break into features, pick architecture, set milestones | Avoid scope creep and endless "just one more thing" |
| **Tech Stack** | Choose language, framework, database, hosting | Every later decision depends on this |
| **AI Skills** | Install agent skills for your stack (design, docs, patterns) | AI writes better code when it has context |
| **MCP Servers** | Add Model Context Protocol servers for framework docs | AI gets real-time access to official documentation |
| **LSPs** | Set up Language Server Protocol for your language | Autocomplete, error detection, refactoring |
| **Plugins** | Editor plugins, linters, formatters, dev tools | Catch bugs early, enforce consistency |
| **Project Init** | Scaffold the project, initialize Git, set up structure | Clean foundation, no "we'll fix it later" tech debt |
| **Dependencies** | Install packages, lock versions, audit for vulnerabilities | Reproducible builds, no surprise breakages |
| **Git + GitHub** | Branch strategy, .gitignore, README, LICENSE, CI/CD | Collaboration ready from day one |
| **Env Variables** | .env files, secrets management, config per environment | Never hardcode secrets, never leak API keys |
| **UI/UX** | Design system, component library, responsive layout | Users judge your app in 3 seconds |
| **Development** | Build features, iterate, review code | The actual work |
| **Testing** | Unit, integration, E2E, accessibility | Ship with confidence, not hope |
| **Security** | Headers, auth, input validation, dependency audit | One vulnerability can tank the whole project |
| **SEO** | Meta tags, sitemap, structured data, performance | Get found without paying for ads |
| **Performance** | Core Web Vitals, lazy loading, caching, bundle size | Speed is a feature |
| **Production Build** | Optimize, minify, tree-shake, preview | What users get is what you tested |
| **Deployment** | CI/CD pipeline, staging, production deploy | Automated, repeatable, boring |
| **Domain + DNS + SSL** | Buy domain, configure DNS, enable HTTPS | Your project lives at a real address |
| **Analytics** | Tracking, error monitoring, uptime | Know what's happening without guessing |
| **Final QA** | Cross-browser, mobile, accessibility, smoke test | Last gate before users see it |
| **Launch** | Soft launch, monitor, announce | Ship it |
| **Maintenance** | Updates, backups, monitoring, iteration | Keep it alive |

---

## Who This Is For

- Solo developers using AI coding tools who want a systematic workflow
- Teams onboarding new projects who need a shared checklist
- Anyone who's ever deployed something and realized they forgot to set up environment variables

---

## Stack Agnostic

This checklist works with:

- **Frameworks:** Astro, Next.js, Nuxt, SvelteKit, Remix, Django, Flask, FastAPI, Rails, Go, Rust, Swift
- **AI Tools:** OpenCode, Claude Code, Cursor, GitHub Copilot, Windsurf, Gemini CLI
- **Hosting:** Vercel, Cloudflare Pages/Workers, Netlify, AWS, GCP, Azure, Railway, Fly.io
- **Databases:** PostgreSQL, MySQL, SQLite, MongoDB, Redis, Supabase, Neon, PlanetScale

---

## Contributing

PRs welcome. If you've found a step that's missing or a tool that should be listed, open an issue or submit a PR.

---

## License

MIT
