# Project Startup Checklist — Step by Step

**Last Updated:** September 2, 2026

The full checklist. 22 phases from idea to maintenance. Check each box as you go. Nothing skipped, nothing forgotten.

Open this alongside your AI coding tool. Follow it top to bottom.

---

## Phase 1: Project Idea

- [ ] Define the problem in one sentence
- [ ] Identify who has this problem (target user)
- [ ] Find 3–5 existing solutions or competitors
- [ ] Note what existing solutions do well and what they miss
- [ ] Define your unique angle — what makes yours different
- [ ] Validate demand — check Reddit, Twitter, forums, search volume
- [ ] Scope it — what's the MVP vs. "nice to have"

**Prompt for AI:**
```
I want to build [one-sentence description].
My target users are [who].
Existing solutions are [list competitors].
What am I missing? What's the MVP? What should I cut?
```

---

## Phase 2: Planning

- [ ] Break the project into 5–10 core features
- [ ] Prioritize: Must Have / Should Have / Could Have / Won't Have (MoSCoW)
- [ ] Choose architecture pattern (monolith, microservices, serverless, MPA, SPA, SSR)
- [ ] Sketch the data model — what entities exist, how they relate
- [ ] Map the user flow — what does a user do from landing to completion
- [ ] Set milestones — what ships in week 1, week 2, week 4
- [ ] Estimate effort per feature (hours, not days — forces precision)

**Prompt for AI:**
```
Break this project into features. For each, estimate hours and mark
Must Have / Should Have / Could Have. Suggest an architecture pattern
and data model. What should I build first?
Project: [description]
```

---

## Phase 3: Tech Stack

- [ ] Choose primary language (TypeScript, Python, Go, Rust, etc.)
- [ ] Choose frontend framework (Astro, Next.js, React, Vue, Svelte, etc.)
- [ ] Choose backend framework if needed (Express, FastAPI, Django, Go Fiber, etc.)
- [ ] Choose database (PostgreSQL, MySQL, SQLite, MongoDB, etc.)
- [ ] Choose ORM or query builder (Prisma, Drizzle, SQLAlchemy, etc.)
- [ ] Choose hosting platform (Vercel, Cloudflare, AWS, Railway, etc.)
- [ ] Choose deployment method (CI/CD, manual deploy, Docker)
- [ ] Document the stack in a `STACK.md` or project README

**Prompt for AI:**
```
Given this project [description], recommend a tech stack.
Consider: simplicity, AI tool compatibility, free hosting options,
deployment ease, and long-term maintainability. Give me the
specific tools, not just categories.
```

---

## Phase 4: AI Skills

- [ ] Install AI coding tool (OpenCode, Claude Code, Cursor, Copilot, Windsurf)
- [ ] Install stack-specific agent skills for your framework
- [ ] Install design system skills if building UI (e.g., Vercel design.md)
- [ ] Install documentation skills for your framework (e.g., Astro docs skill)
- [ ] Install language-specific best practices skills
- [ ] Create a `DESIGN.md` or project style guide the AI can reference

**Common AI Skills:**

| Skill | Purpose | Install |
|-------|---------|---------|
| web-design-guidelines | UI/UX patterns from Vercel | `npx skills add https://github.com/vercel-labs/agent-skills --skill web-design-guidelines` |
| tailwind-4-docs | Tailwind CSS reference | `npx skills add https://github.com/lombiq/tailwind-agent-skills --skill tailwind-4-docs` |
| framework-specific docs | Official docs access | Search "[framework] agent skill" |

---

## Phase 5: MCP Servers

- [ ] Add Model Context Protocol server for your framework's docs
- [ ] Add database MCP if using a managed database (Supabase, Neon, PlanetScale)
- [ ] Add deployment platform MCP if available (Cloudflare, Vercel)
- [ ] Test the MCP connection — ask AI a framework-specific question

**How to install MCP servers:**
1. Search "[framework] MCP server" on Google
2. Find the official or highest-starred repo
3. Copy the install command
4. Paste in your editor terminal or MCP config

**Prompt for AI:**
```
Test the MCP connection. Ask: "What is the latest way to do [X]
in [framework]?" Verify the answer matches current documentation.
```

---

## Phase 6: LSPs (Language Server Protocol)

- [ ] Confirm your editor has LSP support for your language
- [ ] Install language server if not bundled (e.g., `gopls` for Go, `rust-analyzer` for Rust)
- [ ] Enable type checking / strict mode in your language
- [ ] Configure auto-imports and go-to-definition
- [ ] Set up hover documentation

**By Language:**

| Language | LSP | Notes |
|----------|-----|-------|
| TypeScript/JavaScript | Built into VS Code | Enable strict mode in tsconfig |
| Python | Pylance / basedpyright | Install via VS Code extensions |
| Go | gopls | `go install golang.org/x/tools/gopls@latest` |
| Rust | rust-analyzer | Install via VS Code or rustup |
| Java | Eclipse JDT LS | Via Java Extension Pack |
| C/C++ | clangd | `brew install llvm` or equivalent |

---

## Phase 7: Plugins

- [ ] Install linter (ESLint, Ruff, golangci-lint, Clippy)
- [ ] Install formatter (Prettier, Black, rustfmt, gofmt)
- [ ] Install editor config (`.editorconfig` for consistent indentation)
- [ ] Install Git hooks manager (Husky, pre-commit)
- [ ] Install error lens / inline diagnostics
- [ ] Install path autocomplete
- [ ] Set up format-on-save

**Prompt for AI:**
```
Set up linting and formatting for this [language] project.
Configure [linter] with sensible defaults. Add a format-on-save
config. Create a pre-commit hook that runs both.
```

---

## Phase 8: Project Initialization

- [ ] Scaffold the project with your framework's CLI
- [ ] Initialize Git repository
- [ ] Create folder structure (components, pages, lib, utils, styles, etc.)
- [ ] Add a basic layout/shell component
- [ ] Add a "hello world" page to confirm it runs
- [ ] Run `npm run dev` (or equivalent) and verify it works in browser
- [ ] Create `README.md` with project description and setup instructions

**Framework Scaffolding:**

```bash
# Astro
npm create astro@latest .

# Next.js
npx create-next-app@latest .

# SvelteKit
npx sv create .

# Django
django-admin startproject myproject .

# Go
go mod init github.com/user/project

# Rust
cargo init
```

---

## Phase 9: Dependencies

- [ ] Install core dependencies for your stack
- [ ] Install dev dependencies (linting, testing, build tools)
- [ ] Lock dependencies (`package-lock.json`, `poetry.lock`, `Cargo.lock`)
- [ ] Run security audit on dependencies
- [ ] Pin exact versions for critical packages
- [ ] Document non-obvious dependencies in README

**Prompt for AI:**
```
Install all dependencies needed for [framework] with [database],
[auth], and [deployment platform]. Separate prod from dev deps.
Run an audit and fix any vulnerabilities.
```

---

## Phase 10: Git + GitHub

- [ ] Create `.gitignore` (use gitignore.io or framework default)
- [ ] Make initial commit with clean project structure
- [ ] Create GitHub repository
- [ ] Push to GitHub
- [ ] Set up branch strategy (main for production, dev for development)
- [ ] Add branch protection rules on main (require PR reviews)
- [ ] Add `LICENSE` file
- [ ] Write `README.md` with setup instructions, tech stack, and contributing guide
- [ ] Set up CI/CD pipeline (GitHub Actions, GitLab CI, etc.)

**Branch naming convention:**
```
main            — production
develop         — integration branch
feature/xxx     — new features
fix/xxx         — bug fixes
chore/xxx       — maintenance, deps, config
```

---

## Phase 11: Environment Variables

- [ ] Create `.env.example` with all required variables (no values)
- [ ] Create `.env.local` for local development (never commit)
- [ ] Add `.env*` to `.gitignore`
- [ ] Document each variable with comments in `.env.example`
- [ ] Set up environment variables on your hosting platform
- [ ] Test that the app reads env vars correctly
- [ ] Create different configs for dev / staging / production

**.env.example template:**
```bash
# Database
DATABASE_URL=

# Auth
AUTH_SECRET=
OAUTH_CLIENT_ID=
OAUTH_CLIENT_SECRET=

# API Keys
API_KEY=

# App
NODE_ENV=development
PORT=3000
```

---

## Phase 12: UI/UX

- [ ] Choose a design system or component library (shadcn/ui, Radix, Chakra, etc.)
- [ ] Set up CSS framework (Tailwind, CSS Modules, Styled Components, etc.)
- [ ] Create base layout (header, footer, sidebar, main content area)
- [ ] Build responsive breakpoints (mobile, tablet, desktop)
- [ ] Add dark mode / theme toggle
- [ ] Create loading states and skeleton screens
- [ ] Add error boundaries / error states
- [ ] Test accessibility basics (keyboard nav, contrast, ARIA labels)
- [ ] Create a favicon and og:image

**Prompt for AI:**
```
Create a responsive layout for [app description] using [design system].
Include: header with navigation, main content area, footer.
Mobile-first. Dark mode support. Use [CSS framework].
```

---

## Phase 13: Development

- [ ] Build features in priority order (Must Have first)
- [ ] Write code in small, reviewable chunks
- [ ] Commit frequently with clear commit messages
- [ ] Review AI-generated code before committing — don't blind-merge
- [ ] Test each feature manually as you build it
- [ ] Handle error cases and edge cases as you go, not at the end
- [ ] Use `/clear` in AI tools between features to reset context

**Prompt for AI:**
```
Build [feature name]. Here's the spec: [description].
Use [pattern] architecture. Handle edge cases: [list].
Write tests for the critical paths.
```

---

## Phase 14: Testing

- [ ] Set up test framework (Vitest, Jest, pytest, Go testing, etc.)
- [ ] Write unit tests for utility functions and business logic
- [ ] Write integration tests for API endpoints and database operations
- [ ] Write E2E tests for critical user flows (Playwright, Cypress, etc.)
- [ ] Add accessibility testing (axe-core, Lighthouse)
- [ ] Run test suite and fix failures
- [ ] Set up test coverage reporting
- [ ] Add tests to CI pipeline

**Prompt for AI:**
```
Write tests for [function/component/API]. Cover:
- happy path
- edge cases (empty input, max values, special characters)
- error cases (network failure, invalid data, unauthorized)
Use [test framework]. Follow existing test patterns in the codebase.
```

---

## Phase 15: Security

- [ ] Add security headers (CSP, X-Frame-Options, X-Content-Type-Options, HSTS)
- [ ] Implement authentication properly (don't roll your own)
- [ ] Validate all user input on the server side
- [ ] Sanitize output to prevent XSS
- [ ] Use parameterized queries (never string concatenation for SQL)
- [ ] Implement rate limiting on API endpoints
- [ ] Audit dependencies for known vulnerabilities
- [ ] Check for hardcoded secrets or API keys in code
- [ ] Enable HTTPS everywhere
- [ ] Set up CORS properly

**Prompt for AI:**
```
Audit this project for security vulnerabilities. Check:
- Security headers (CSP, HSTS, X-Frame-Options)
- Input validation and sanitization
- SQL injection / XSS vectors
- Authentication/authorization gaps
- Hardcoded secrets
- Dependency vulnerabilities
Give me a prioritized list of fixes.
```

---

## Phase 16: SEO

- [ ] Set `<title>` tag with primary keyword (under 60 characters)
- [ ] Set `<meta description>` with keyword (under 160 characters)
- [ ] Add Open Graph tags (og:title, og:description, og:image, og:url)
- [ ] Add Twitter Card tags
- [ ] Add canonical URL
- [ ] Create `sitemap.xml` with all pages
- [ ] Create `robots.txt` with sitemap reference
- [ ] Add structured data (JSON-LD) for relevant content types
- [ ] Ensure all images have descriptive `alt` attributes
- [ ] Use clean, descriptive URLs
- [ ] Add internal linking between pages

**Prompt for AI:**
```
Do on-page SEO for this page.
Main keyword: [keyword]
Supporting keywords: [list]
Add: title tag, meta description, OG tags, canonical URL,
structured data, and 800–1200 words of relevant content.
```

---

## Phase 17: Performance

- [ ] Measure Core Web Vitals (LCP, INP, CLS)
- [ ] Optimize images (compress, convert to WebP/AVIF, lazy load)
- [ ] Implement code splitting / lazy loading
- [ ] Minify CSS and JavaScript
- [ ] Enable tree shaking
- [ ] Set up caching headers
- [ ] Use a CDN for static assets
- [ ] Minimize third-party scripts
- [ ] Preload critical resources
- [ ] Test on slow networks (Chrome DevTools → Network throttling)

**Prompt for AI:**
```
Optimize this app for performance. Check:
- Bundle size — can we tree-shake or lazy-load anything?
- Images — are they compressed and using modern formats?
- Caching — are headers set correctly?
- Third-party scripts — can we defer or remove any?
Give me a prioritized list of improvements.
```

---

## Phase 18: Production Build

- [ ] Run production build locally
- [ ] Verify no console errors or warnings
- [ ] Check bundle size — is it reasonable?
- [ ] Test production build locally (`npm run preview` or equivalent)
- [ ] Verify environment variables load correctly in production mode
- [ ] Test all features in production mode (not just dev mode)
- [ ] Check that source maps are generated (for error tracking)
- [ ] Verify no development-only code leaks into production build

**Prompt for AI:**
```
Run the production build. Check for:
- Build errors or warnings
- Bundle size analysis
- Missing optimizations
- Development code leaking into production
Fix anything you find.
```

---

## Phase 19: Deployment

- [ ] Choose deployment platform (Vercel, Cloudflare, Netlify, AWS, Railway, etc.)
- [ ] Connect GitHub repository to deployment platform
- [ ] Set up environment variables on the platform
- [ ] Configure build command and output directory
- [ ] Deploy to staging first
- [ ] Test staging environment thoroughly
- [ ] Set up automatic deployments on push to main
- [ ] Configure preview deployments for pull requests
- [ ] Set up rollback strategy

**Prompt for AI:**
```
Deploy this [framework] app to [platform].
Set up automatic deployments on push to main.
Configure preview deployments for PRs.
Add the deploy command to package.json.
```

---

## Phase 20: Domain + DNS + SSL

- [ ] Buy domain from registrar (Namecheap, Cloudflare Registrar, Porkbun, etc.)
- [ ] Add domain to your hosting platform
- [ ] Update nameservers at registrar to point to hosting platform
- [ ] Configure DNS records (A, CNAME, MX, TXT)
- [ ] Wait for DNS propagation (10–30 minutes, up to 48 hours)
- [ ] Verify SSL certificate is active and auto-renewing
- [ ] Set up redirect from www to non-www (or vice versa)
- [ ] Set up redirect from staging/preview domain to production
- [ ] Disable staging/preview subdomain indexing (no duplicate content)

**Prompt for AI:**
```
My site is deployed at [platform]. I bought [domain.com].
Walk me through DNS setup step by step.
Disable indexing on [preview.pages.dev] or [staging.app.vercel.app].
```

---

## Phase 21: Analytics

- [ ] Set up Google Analytics or alternative (Plausible, Fathom, Umami)
- [ ] Set up error tracking (Sentry, LogRocket, Bugsnag)
- [ ] Set up uptime monitoring (Betterstack, UptimeRobot, Checkly)
- [ ] Add analytics tracking code to the app
- [ ] Verify tracking works (real-time analytics check)
- [ ] Set up conversion tracking if applicable
- [ ] Create a dashboard or alerts for key metrics

**Prompt for AI:**
```
Add [analytics tool] tracking to this [framework] app.
Add [error tracking tool] for production error monitoring.
Set up [uptime monitoring] for the deployed URL.
```

---

## Phase 22: Final QA

- [ ] Test on Chrome, Firefox, Safari, Edge
- [ ] Test on mobile (iOS Safari, Android Chrome)
- [ ] Test all user flows end-to-end
- [ ] Test with JavaScript disabled (graceful degradation)
- [ ] Test on slow network (3G simulation)
- [ ] Run Lighthouse audit (aim for 90+ on all categories)
- [ ] Check all links — no broken links
- [ ] Check all forms — submission, validation, error states
- [ ] Check 404 page — does it exist and look decent?
- [ ] Check SEO — all pages have titles, descriptions, OG tags
- [ ] Verify robots.txt and sitemap.xml are accessible
- [ ] Verify HTTPS works on all pages
- [ ] Check for console errors in production

**Prompt for AI:**
```
Run a full QA check on this app. Test:
- Cross-browser compatibility
- Mobile responsiveness
- All user flows
- SEO tags on every page
- Accessibility (keyboard nav, contrast, ARIA)
- Performance (Lighthouse score)
- Error handling (what happens on bad input, network failure?)
Give me a report with pass/fail for each item.
```

---

## Phase 23: Launch

- [ ] Soft launch to a small group first (friends, beta users)
- [ ] Monitor error tracking for new issues
- [ ] Monitor analytics for unexpected behavior
- [ ] Fix any critical issues before public launch
- [ ] Announce on social media, Product Hunt, Hacker News, Reddit
- [ ] Send to relevant communities
- [ ] Respond to feedback and bug reports quickly

---

## Phase 24: Maintenance

- [ ] Set up dependency update automation (Dependabot, Renovate)
- [ ] Schedule regular security audits (monthly)
- [ ] Monitor uptime and performance continuously
- [ ] Back up your database regularly
- [ ] Review and update documentation quarterly
- [ ] Plan feature iterations based on user feedback
- [ ] Track and resolve technical debt
- [ ] Keep AI skills and MCP servers updated

---

## Reference

- [Guide 1 — Step by Step](Guide%201.md) (this file)
- [Guide 2 — Prompts & Resources](Guide%202.md) (prompt templates, tool links)
- [README](README.md) (overview)
