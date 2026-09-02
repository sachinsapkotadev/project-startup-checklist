# Project Startup Checklist — Prompts & Resources

**Last Updated:** September 2, 2026

Copy-paste prompt templates, essential tool links, and quick reference for every phase.

---

## Prompt Templates

### Idea Validation

```
I want to build [one-sentence description].
My target users are [who].
Existing solutions: [list 3–5 competitors].

What am I missing? What's the MVP? What should I cut?
What's the smallest version that proves this works?
```

### Tech Stack Recommendation

```
Given this project [description], recommend a tech stack.
Constraints:
- Must work with [AI tool: OpenCode / Claude Code / Cursor]
- Hosting budget: [free / $X per month]
- Team size: [solo / small team]
- Target scale: [hobby / startup / enterprise]

Give me specific tools, not just categories. Explain why each pick.
```

### Architecture Planning

```
Design the architecture for [project description].
Tech stack: [list]
Requirements:
- [requirement 1]
- [requirement 2]
- [requirement 3]

Give me:
1. Folder structure
2. Data model (entities and relationships)
3. API routes if applicable
4. Component hierarchy if frontend
5. Key architectural decisions and why
```

### Project Scaffolding

```
Initialize a new [framework] project in this directory.
Set up:
- [Framework] with [template: basic / minimal / full]
- [CSS framework] configured
- [Linting and formatting]
- [Testing framework]
- Git initialized with .gitignore
- README.md with setup instructions

Run the dev server and confirm it works.
```

### Feature Building

```
Build [feature name].

Spec:
- [what it does]
- [input/output]
- [edge cases to handle]

Architecture:
- Use [pattern: component / API route / utility function]
- Follow existing code patterns in the project
- [specific constraints]

Write the code, add error handling, and write tests for critical paths.
```

### Code Review

```
Review the code in [file / directory / recent changes].

Check for:
- Bugs and logic errors
- Security vulnerabilities
- Performance issues
- Code style consistency with the rest of the project
- Missing error handling
- Missing edge cases

Give me specific fixes, not just warnings.
```

### Testing

```
Write tests for [function / component / API endpoint].

Cover:
- Happy path (normal input, expected output)
- Edge cases: empty input, null, max values, special characters, unicode
- Error cases: invalid input, network failure, unauthorized access
- Boundary conditions

Use [test framework]. Follow the patterns in existing test files.
Aim for high coverage on critical business logic.
```

### Security Audit

```
Audit this project for security vulnerabilities.

Check:
- Security headers (CSP, HSTS, X-Frame-Options, X-Content-Type-Options)
- Input validation and sanitization (server-side)
- SQL injection / NoSQL injection vectors
- XSS vectors (stored, reflected, DOM-based)
- Authentication and authorization gaps
- Hardcoded secrets or API keys in source code
- Dependency vulnerabilities (npm audit, pip audit, etc.)
- CORS configuration
- Rate limiting on sensitive endpoints
- File upload validation

Give me a prioritized list: Critical → High → Medium → Low.
Include specific code fixes for each issue.
```

### SEO Optimization

```
Do on-page SEO for [page URL or description].

Main keyword: [keyword]
Supporting keywords: [list]

Generate:
1. Title tag (under 60 characters, primary keyword near start)
2. Meta description (under 160 characters, compelling, includes keyword)
3. Open Graph tags (og:title, og:description, og:image, og:url, og:type)
4. Twitter Card tags
5. Canonical URL
6. JSON-LD structured data for [type: Article / Product / FAQ / HowTo]
7. 800–1200 words of relevant, natural content incorporating keywords
8. Internal link suggestions to other pages on the site
```

### Performance Optimization

```
Optimize this [framework] app for performance.

Current state:
- [describe current issues or metrics if known]

Check and fix:
- Bundle size (tree shaking, code splitting, dynamic imports)
- Image optimization (compression, formats, lazy loading)
- Caching headers and strategies
- Third-party script impact
- Critical rendering path
- Core Web Vitals (LCP, INP, CLS)

Give me a prioritized list with expected impact.
```

### Deployment

```
Deploy this [framework] app to [platform].

Steps:
1. Build the project for production
2. Configure the deployment (build command, output directory)
3. Set up environment variables
4. Deploy to staging first, then production
5. Add the deploy script to package.json
6. Set up automatic deployment on push to main
7. Configure preview deployments for PRs

Verify the deployment works and report the live URL.
```

### Domain & DNS Setup

```
My app is deployed at [current URL].
I bought [domain.com] from [registrar].

Walk me through:
1. Adding the domain to [hosting platform]
2. Configuring DNS records (A, CNAME, MX, TXT)
3. Updating nameservers at the registrar
4. Verifying SSL is active
5. Setting up www redirect
6. Disabling indexing on the staging/preview URL
7. Submitting to Google Search Console

Give me exact steps with the specific values to use.
```

---

## Essential Tools

### Keyword Research & SEO

| Tool | URL | Purpose |
|------|-----|---------|
| Ahrefs Free Keyword Generator | https://ahrefs.com/keyword-generator | Keyword research, search volume |
| Ahrefs Traffic Checker | https://ahrefs.com/traffic-checker | Competitor traffic analysis |
| Google Search Console | https://search.google.com/search-console | Submit sitemap, monitor indexing |
| Bing Webmaster Tools | https://www.bing.com/webmasters | Submit to Bing |
| Google Trends | https://trends.google.com | Trend analysis |

### Domain & Hosting

| Tool | URL | Purpose |
|------|-----|---------|
| Instant Domain Search | https://instantdomainsearch.com | Find available domains |
| Cloudflare | https://dash.cloudflare.com | DNS, CDN, Pages, Workers |
| Vercel | https://vercel.com | Hosting, edge functions |
| Netlify | https://netlify.com | Hosting, serverless functions |
| Railway | https://railway.app | App hosting with databases |
| Fly.io | https://fly.io | Global app deployment |

### Design & Assets

| Tool | URL | Purpose |
|------|-----|---------|
| Vercel Design MD | https://getdesign.md/vercel/design-md | AI design system |
| logofast | https://logofa.st | Logo and favicon generator |
| Real Favicon Generator | https://realfavicongenerator.net | Favicon all sizes |
| Coolors | https://coolors.co | Color palette generator |
| Google Fonts | https://fonts.google.com | Web fonts |

### Analytics & Monitoring

| Tool | URL | Purpose |
|------|-----|---------|
| Google Analytics | https://analytics.google.com | Traffic analytics |
| Plausible | https://plausible.com | Privacy-friendly analytics |
| Sentry | https://sentry.io | Error tracking |
| Betterstack | https://betterstack.com | Uptime monitoring |
| Lighthouse | Built into Chrome | Performance auditing |

### Development Tools

| Tool | URL | Purpose |
|------|-----|---------|
| Git | https://git-scm.com | Version control |
| VS Code | https://code.visualstudio.com | Editor |
| Node.js | https://nodejs.org | JavaScript runtime |
| GitHub | https://github.com | Repository hosting |
| Postman | https://www.postman.com | API testing |
| DB Browser for SQLite | https://sqlitebrowser.org | Database GUI |

---

## AI Coding Tool Setup

### OpenCode

- Install: https://opencode.ai
- Works with any stack
- Load skills from `.config/opencode/skills/` or `.agents/skills/`
- MCP servers configured in `opencode.json`

### Claude Code

- Install: `npm install -g @anthropic-ai/claude-code`
- Run: `claude` in your project directory
- Use `/clear` between features to reset context
- Skills loaded via `npx skills add`

### Cursor

- Download: https://cursor.sh
- VS Code fork with built-in AI
- Use `.cursorrules` for project-specific instructions
- Composer mode for multi-file edits

### GitHub Copilot

- Install via VS Code extension
- Use `#file` to reference files in prompts
- Tab completion for inline suggestions

---

## Framework-Specific MCP Servers

### Astro

```bash
# Search "Astro MCP server" → copy install command
# Or add manually to your MCP config:
{
  "mcpServers": {
    "astro-docs": {
      "command": "npx",
      "args": ["-y", "@anthropic-ai/mcp-server-astro"]
    }
  }
}
```

### Next.js

```bash
# Check Vercel's MCP server for Next.js docs
# Add to your MCP config
```

### General Pattern

1. Search "[framework] MCP server"
2. Find the official or community server
3. Add to your MCP config (location depends on your AI tool)
4. Test by asking a framework-specific question

---

## Common .gitignore Patterns

### Node.js

```
node_modules/
.env
.env.local
.env.*.local
dist/
build/
.next/
.nuxt/
.vercel/
*.log
.DS_Store
```

### Python

```
__pycache__/
*.py[cod]
.env
venv/
.venv/
*.egg-info/
dist/
build/
.pytest_cache/
```

### Go

```
/bin/
/vendor/
.env
*.exe
*.exe~
*.dll
*.so
*.dylib
```

### Rust

```
/target/
.env
*.swp
*.swo
```

---

## Security Headers Template

### Cloudflare `_headers` file

```
/*
  X-Content-Type-Options: nosniff
  X-Frame-Options: DENY
  X-XSS-Protection: 1; mode=block
  Referrer-Policy: strict-origin-when-cross-origin
  Permissions-Policy: camera=(), microphone=(), geolocation=()
  Content-Security-Policy: default-src 'self'; script-src 'self' 'unsafe-inline' https://www.googletagmanager.com; style-src 'self' 'unsafe-inline'; img-src 'self' data: https:; font-src 'self'; connect-src 'self' https://www.google-analytics.com; frame-ancestors 'none';

/static/*
  Cache-Control: public, max-age=31536000, immutable

/*
  Strict-Transport-Security: max-age=31536000; includeSubDomains; preload
```

### Next.js `next.config.js`

```js
const securityHeaders = [
  { key: 'X-Content-Type-Options', value: 'nosniff' },
  { key: 'X-Frame-Options', value: 'DENY' },
  { key: 'X-XSS-Protection', value: '1; mode=block' },
  { key: 'Referrer-Policy', value: 'strict-origin-when-cross-origin' },
  { key: 'Permissions-Policy', value: 'camera=(), microphone=(), geolocation=()' },
  {
    key: 'Content-Security-Policy',
    value: "default-src 'self'; script-src 'self' 'unsafe-inline' https://www.googletagmanager.com; style-src 'self' 'unsafe-inline'; img-src 'self' data: https:; font-src 'self'; connect-src 'self' https://www.google-analytics.com; frame-ancestors 'none'"
  }
];

module.exports = {
  headers: async () => [{ source: '/(.*)', headers: securityHeaders }]
};
```

---

## CI/CD Template (GitHub Actions)

```yaml
name: CI/CD

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: npm
      - run: npm ci
      - run: npm run lint
      - run: npm run typecheck
      - run: npm test
      - run: npm run build

  deploy:
    needs: test
    if: github.ref == 'refs/heads/main'
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm run build
      # Add your deployment step here
```

---

## .env.example Template

```bash
# ============================================
# Environment Variables
# Copy this to .env.local and fill in values
# ============================================

# Database
DATABASE_URL=

# Authentication
AUTH_SECRET=
OAUTH_GOOGLE_ID=
OAUTH_GOOGLE_SECRET=

# API Keys
API_KEY=

# App Configuration
NODE_ENV=development
PORT=3000
APP_URL=http://localhost:3000

# Email (if applicable)
SMTP_HOST=
SMTP_PORT=
SMTP_USER=
SMTP_PASS=

# Storage (if applicable)
S3_BUCKET=
S3_REGION=
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY

# Analytics
GA_MEASUREMENT_ID=
```

---

## EditorConfig Template

```ini
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

[*.md]
trim_trailing_whitespace = false

[Makefile]
indent_style = tab
```

---

## Quick Reference Links

| Need | Go To |
|------|-------|
| Find a domain | https://instantdomainsearch.com |
| Keyword research | https://ahrefs.com/keyword-generator |
| Competitor traffic | https://ahrefs.com/traffic-checker |
| Deploy to Cloudflare | https://dash.cloudflare.com |
| Deploy to Vercel | https://vercel.com |
| Google Analytics | https://analytics.google.com |
| Google Search Console | https://search.google.com/search-console |
| Bing Webmasters | https://www.bing.com/webmasters |
| Sentry error tracking | https://sentry.io |
| Lighthouse audit | Chrome DevTools → Lighthouse tab |
| Design inspiration | https://dribbble.com / https://mobbin.com |
| Accessibility check | https://wave.webaim.org |

---

## Reference

- [README](README.md) (overview)
- [Guide 1 — Step by Step](Guide%201.md) (full checklist)
- [Guide 2 — Prompts & Resources](Guide%202.md) (this file)
