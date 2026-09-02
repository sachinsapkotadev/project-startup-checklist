# Micro-Tool Website Builder — Earn with AI

A complete checklist to build, deploy, and monetize micro-tool websites using AI.

**The model:** Build one small, focused web tool per month → rank on Google → earn passive income via Google AdSense. Cost: ~₹1,000/year (domain only). Hosting is free on Cloudflare.

---

## Step 1: Find a Problem Worth Solving

- [ ] Find a small, real-world problem that can be solved with a single-page web tool
- [ ] Check Google — if page 4 shows a government site or Quora thread, you've found a low-competition gold mine
- [ ] Note weaknesses in existing tools for that keyword
- [ ] Use AI to brainstorm: *"What are small everyday problems people face that could be solved with a simple web tool?"*
- [ ] Check Reddit, Quora for complaints in relevant subreddits

**Good traits:** affects you personally, seems small (less competition), no great tool exists yet.

---

## Step 2: Keyword Research with Ahrefs

- [ ] Go to [Ahrefs Free Keyword Generator](https://ahrefs.com/keyword-generator)
- [ ] Use [Ahrefs Traffic Checker](https://ahrefs.com/traffic-checker) to spy on competitor traffic numbers
- [ ] Enter your main keyword — check monthly search volume (even 1,000 US searches is enough)
- [ ] Go to **Questions tab** → copy all FAQs (these become your FAQ section)
- [ ] Check **Related terms tab** for supporting keywords
- [ ] Type your keyword in Google + Space — use autocomplete suggestions as additional keywords
- [ ] Target US-English phrasing for higher AdSense CPM

---

## Step 3: Choose Your Domain Name

- [ ] **.com only** — no exceptions
- [ ] Primary keyword must be in the domain
- [ ] Short, no hyphens
- [ ] Use [Instant Domain Search](https://instantdomainsearch.com) to find available .com
- [ ] **Do NOT buy domain yet** — write code first, confirm it works, then buy

**Where to buy:** Namecheap (card), GoDaddy (UPI), BigRock (~₹883/yr UPI), Hostinger (~₹904/yr UPI)

---

## Step 4: Setup Dev Environment

- [ ] Install [Git](https://git-scm.com/)
- [ ] Install [VS Code](https://code.visualstudio.com/)
- [ ] Install [Node.js](https://nodejs.org/)
- [ ] Install an AI coding tool (Claude Code / Cursor AI free tier / Gemini CLI)
- [ ] Create project folder named after your domain (e.g., `realonlineruler.com`)
- [ ] Open folder in VS Code → open terminal

---

## Step 5: Build the Website with AI

### 5.1 Install AstroJS

```bash
npm create astro@latest .
```

- Press Enter for all defaults, choose **Basic** template, Yes to initialize Git

### 5.2 Add Vercel's design.md

```bash
npx getdesign@latest add vercel
```

### 5.3 Install AI Skills

```bash
# Web Design Guidelines
npx skills add https://github.com/vercel-labs/agent-skills --skill web-design-guidelines

# Tailwind 4 Docs
npx skills add https://github.com/lombiq/tailwind-agent-skills --skill tailwind-4-docs
```

### 5.4 Add Astro JS MCP Server

- [ ] Search "Astro JS MCP" on Google → first link → copy install command → paste in VS Code terminal

### 5.5 Write the Prompt (in Claude Code)

```
I have initialized a new AstroJS project. Use the astro-docs MCP, tailwind-4-docs skill,
and web-design-guidelines skill. Also use @DESIGN.md. Keep the website design like Vercel.

Name: [Your Tool Name]
Domain: [yourdomain.com]

Create a [describe your tool]. My competitor is [URL] — analyze it, identify its weaknesses,
and build a better version. Use MPA (multi-page application) architecture for best SEO.
```

### 5.6 Review and Iterate

- [ ] Run `npm run dev` → test everything in browser
- [ ] For each issue: type `/clear` in Claude Code → describe the problem → let it fix
- [ ] Add dark mode toggle
- [ ] Test mobile responsiveness (Chrome DevTools → Inspect → mobile icon)
- [ ] Keep iterating until clearly better than every page-1 competitor

---

## Step 6: On-Page SEO

Run this prompt in Claude Code after `/clear`:

```
Do the on-page SEO of this website for:
Main Keyword: [your keyword]
Supporting Keywords: [comma-separated list from Ahrefs]

Also add proper OG meta tags. Write 600 words about the tool on the home page for SEO.
```

- [ ] `<title>` tag contains primary keyword
- [ ] `<meta description>` under 160 characters with keyword
- [ ] All images have descriptive `alt` attributes
- [ ] Clean URLs (e.g., `/online-ruler` not `/page?id=123`)

---

## Step 7: Add FAQ Section

- [ ] Paste questions from Ahrefs "Questions" tab and Google "People Also Ask"
- [ ] Use JSON-LD structured data for rich results in Google

Prompt:

```
Add an SEO-friendly FAQ section using JSON-LD structured data for these questions:
[paste your questions]
```

---

## Step 8: Required Pages for AdSense Approval

Prompt:

```
Create these pages as separate MPA routes for best SEO:
- Privacy Policy
- Terms & Conditions
- About Us
- Contact Us

Make these pages visible and linked in the home page footer and header.
```

- [ ] Privacy Policy page
- [ ] Terms & Conditions page
- [ ] About Us page
- [ ] Contact Us page
- [ ] All linked in header and footer
- [ ] Add `robots.txt` with sitemap link
- [ ] Generate `sitemap.xml` with all page URLs
- [ ] Add error pages (404, 500)
- [ ] Add Google Analytics tracking code

---

## Step 9: Deploy to Cloudflare Pages

```bash
npx wrangler login
```

- [ ] Ask Claude Code to add a deploy command to `package.json`
- [ ] Run `npm run deploy` — site goes live at `*.pages.dev` instantly
- [ ] Commit changes regularly via VS Code Source Control

---

## Step 10: Buy & Connect Your Domain

- [ ] Buy .com domain from registrar (after code works and deploys)
- [ ] Go to Cloudflare → Domains → Add Domain → select free plan
- [ ] Delete all existing DNS records
- [ ] Add A record: Name `@`, Value `8.8.8.8` (temporary)
- [ ] Copy Cloudflare nameservers → update at your registrar
- [ ] Wait 10–30 minutes for propagation
- [ ] Workers & Pages → your project → Settings → Custom Domains → add domain → Activate
- [ ] Repeat for `www` version

### Fix duplicate content (pages.dev):

Create `_headers` file in `/public` folder:

```
https://yoursite.pages.dev/*
  X-Robots-Tag: noindex
```

- [ ] Deploy again with `npm run deploy`
- [ ] Verify `X-Robots-Tag: noindex` header appears on `.pages.dev` but NOT on `.com`

---

## Step 11: Submit to Search Engines

### Google Search Console

- [ ] Go to [Google Search Console](https://search.google.com/search-console)
- [ ] Add domain property
- [ ] Verify via TXT DNS record in Cloudflare
- [ ] Submit sitemap: `sitemap.xml`
- [ ] URL Inspection → Request Indexing on homepage

### Bing Webmaster Tools

- [ ] Go to [Bing Webmaster Tools](https://www.bing.com/webmasters)
- [ ] Sign in with Google → Import from Google Search Console
- [ ] Submit URL for indexing

### Promote

- [ ] Post on Reddit in related subreddits
- [ ] Answer questions on Quora with tool link
- [ ] Share on social media
- [ ] Send to friends and family

---

## Step 12: Apply for Google AdSense

- [ ] Wait until you have **10+ daily users** consistently (check Google Analytics Real-time)
- [ ] Go to [ads.google.com](https://ads.google.com)
- [ ] Add site → paste AdSense code snippet → deploy
- [ ] Create and deploy `ads.txt` file
- [ ] Click Request Review
- [ ] Once approved, turn on **Auto Ads**

---

## Timeline

| When | What Happens |
|------|-------------|
| Month 1–3 | Site live, Google crawling, rankings low. Keep building more tools. |
| Month 4–6 | Rankings climb if SEO is solid. First meaningful traffic. |
| Month 6+ | 10+ daily users → apply for AdSense. First earnings appear. |
| Year 1 | 12 tools live, 1–3 driving organic traffic. Passive income begins. |
| Year 2 | 24 tools. Compounding effect. Revenue scales with traffic. |

---

## Resources

- [Ahrefs Keyword Generator](https://ahrefs.com/keyword-generator)
- [Ahrefs Traffic Checker](https://ahrefs.com/traffic-checker)
- [Instant Domain Search](https://instantdomainsearch.com)
- [Vercel design.md](https://getdesign.md/vercel/design-md)
- [Web Design Guidelines Skill](https://www.skills.sh/vercel-labs/agent-skills/web-design-guidelines)
- [Tailwind 4 Docs Skill](https://www.skills.sh/lombiq/tailwind-agent-skills/tailwind-4-docs)
- [AstroJS Docs](https://docs.astro.build/en/getting-started/)
- [Cloudflare Pages Deploy](https://docs.astro.build/en/guides/deploy/cloudflare/)
- [AstroJS MCP Server](https://docs.astro.build/en/guides/build-with-ai/#astro-docs-mcp-server)
- [Google Analytics](https://analytics.google.com)
- [Google Search Console](https://search.google.com/search-console/about)
- [Bing Webmaster](https://www.bing.com/webmasters/about)
- [Google AdSense](https://ads.google.com/start/)
- [Cloudflare Dashboard](https://dash.cloudflare.com/login)
