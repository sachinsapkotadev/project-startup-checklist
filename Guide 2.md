# Micro-Tool Website Builder — Complete Guide

**Last Updated:** September 2, 2026

A complete checklist to build, deploy, and monetize micro-tool websites using AI.

**The model:** Build one small, focused web tool per month → rank on Google → earn passive income via Google AdSense. Cost: ~₹1,000/year (domain only). Hosting is free on Cloudflare.

> Affiliate disclosure: Some links below are affiliate links. If you buy through them I earn a small commission at no extra cost to you — it helps me keep making free videos.

---

## Must Watch Videos

| Topic | MacOS | Windows |
|-------|-------|---------|
| Installing Git | [MacOS](https://tothe.app/JjR7GHy) | [Windows](https://tothe.app/QqAHA29) |
| Installing NodeJS | [MacOS](https://tothe.app/bfUq5kQ) | [Windows](https://tothe.app/ginvdkk) |
| Installing VS Code | [MacOS](https://tothe.app/alsATnI) | [Windows](https://tothe.app/KxjAunQ) |

| Topic | Link |
|-------|------|
| How to Code with AI for FREE | [Watch](https://tothe.app/NzMc7pu) |
| How to use Claude Code | [Watch](https://tothe.app/kjob1WE) |
| Full 3Hr+ Video Tutorial | [Watch](https://compilefuture.com/blog/making-50-lpa-from-my-own-ai-business/) |

---

## CompileFuture Website Checklist

- [ ] Create website with Prompt (give competitor url)
- [ ] Use [logofa.st](https://logofa.st/) for the logo & favicon
- [ ] Add Favicon (use real favicon generator)
- [ ] Website should be mobile responsive
- [ ] Do SEO with prompt (write about the tool 800–1200 words)
- [ ] Add FAQ section
- [ ] Add privacy policy, about us, terms & conditions, contact us pages
- [ ] Add error pages (404, 500)
- [ ] robots.txt
- [ ] sitemap.xml
- [ ] Add Google Analytics code
- [ ] Add `_headers` file for Cloudflare Pages / if using Workers then disable workers.dev domains after connecting the .com domain
- [ ] Add mail routing in Cloudflare for getting emails in your Gmail

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

---

## Step 4: Setup Dev Environment

- [ ] Install [Git](https://git-scm.com/) — [MacOS](https://tothe.app/JjR7GHy) | [Windows](https://tothe.app/QqAHA29)
- [ ] Install [VS Code](https://code.visualstudio.com/) — [MacOS](https://tothe.app/alsATnI) | [Windows](https://tothe.app/KxjAunQ)
- [ ] Install [Node.js](https://nodejs.org/) — [MacOS](https://tothe.app/bfUq5kQ) | [Windows](https://tothe.app/ginvdkk)
- [ ] Install an AI coding tool ([Claude Code](https://tothe.app/kjob1WE) / Cursor AI free tier / Gemini CLI)
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

Also add proper OG meta tags. Write 800 - 1200 words about the tool on the home page for SEO.
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

NOTE: Use JSON-LD for FAQ SEO
```

JSON-LD Example:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "How to find an apprenticeship?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "<p>We provide an official service to search through available apprenticeships. To get started, create an account here, specify the desired region, and your preferences. You will be able to search through all officially registered open apprenticeships.</p>"
    }
  }, {
    "@type": "Question",
    "name": "Whom to contact?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "You can contact the apprenticeship office through our official phone hotline above, or with the web-form below. We generally respond to written requests within 7-10 days."
    }
  }]
}
</script>
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

## Step 9: Deploy to Cloudflare

### Is my website static or dynamic?

Ask Claude Code: *"this website is static or not? and should i deploy it in cloudflare pages or workers?"*

### Cloudflare Pages (for static sites)

```bash
npx wrangler login
```

Prompt:

```
I have already loggedin to cloudflare wrangler, now deploy this astrojs website to
cloudflare pages and take info from astro docs mcp if needed. Also add deploy script to package.json
```

- [ ] Run `npm run deploy` — site goes live at `*.pages.dev` instantly
- [ ] Commit changes regularly via VS Code Source Control

### Cloudflare Workers (for dynamic sites with backend logic)

```
I have already loggedin to cloudflare wrangler, now deploy this astrojs website to
cloudflare workers and take info from astro docs mcp if needed. Also add deploy script to package.json
```

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

### Disable pages.dev / workers.dev domains indexing

**If deployed in CF Pages:**

Add `_headers` file in `/public` folder:

```
https://project.pages.dev/*
  X-Robots-Tag: noindex
```

**If deployed in CF Workers:**

Just turn off workers domains after adding a custom domain in the workers settings.

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

## Bonus: Single Language Website Convert Prompt

Use this to convert an English website to target a specific language/country.

```
website built using this: [YOUR_ENGLISH_WEBSITE_URL]

this is my english website, convert this full website to rank on "[TARGET_KEYWORD]"
and domain: [TARGET_DOMAIN], we want to rank in [TARGET_COUNTRY] and every
[SPEAKING_LANGUAGE] countries.

Add hreflang markup of [TARGET_LANGUAGE].

NOTE: Do not just give a /lang pages, convert this whole website to a [TARGET_LANGUAGE]
website only. we only want [TARGET_LANGUAGE] language no other languages.

Change the full content of this website to rank on main keyword: [TARGET_KEYWORD]
Supportive keywords:
[keyword 1]
[keyword 2]
[keyword 3]
[keyword 4]
[keyword 5]
```

**Example — Portuguese (Brazil):**

```
website built using this: https://reguatamanhoreal.com/

this is my english website, convert this full website to rank on "regua tamanho real"
and domain: reguatamanhoreal.com, we want to rank in brazil and every portuguese countries.

Add hreflang markup of Portuguese.

NOTE: Do not just give a /lang pages, convert this whole website to a portuguese
website only. we only want portuguese language no other languages.

Change the full content of this website to rank on main keyword: regua tamanho real
Supportive keywords:
régua online
regua virtual
fita metrica online
régua tamanho real celular
regua tamanho real online
régua online anel
régua online tamanho real
régua online celular
régua online gratis
```

---

## Bonus: Make Website Multi Language

Use this to add multi-language support to an existing site using Astro i18n.

```
website built using this: [YOUR_WEBSITE_URL]

https://docs.astro.build/en/recipes/i18n/ use this to provide multi lang support
to this website so that it ranks on other languages keywords.

provide support for:
Español
日本語
Français
Deutsch
Português
한국어
Italiano

note: Add hreflang markup for each language.
```

---

## Example Prompts

### Website Creation Prompt

```
I have initialized a new astrojs project, use astro docs mcp and tailwind-4-docs skill
for creating the website. Also use @DESIGN.md file for the website design.

Name: Font Finder AI
Domain: fontfinderai.com

Website Description:
Create a font finder website that will have option to find fonts using image and the
results should contain both paid and free fonts but user can filter only free fonts easily.

My competitor website is fontdetector.org and it have some features which we need and
we need to make a website better than it. Give me ideas how to make it better. go on to
this website and check what exactly we need to make. Do not copy design or ui from that website.
```

### SEO Prompt

```
Do the On Page SEO of this Website for

Main Keyword: Font Finder
Supporting Keywords:
font finder by image
free font finder
font finder from image free
font finder free
font finder from image
ai font finder
font finder upload image
font finder by text
google font finder
what the font finder
image font finder

these above keywords, also use proper og meta tags for SEO
on home page write 800 - 1200 words about the tool for SEO
```

### FAQ Section Prompt

```
add seo friendly FAQ section for these below questions:

what the font finder
Can Google identify a font?
How can I identify a type of font?
How to see which font is used?
Can I use AI to identify a font?
Is there a free font finder?
How to match a font?
Can I take a picture of a font and find it?
Where can I find free fonts?
How to find a specific text font?
How do I use Google Fonts?
How to identify a font in a PDF?
Can I create a font using AI?

NOTE: Use JSON-LD for FAQ SEO
```

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

## Buying Domains

| Registrar | Link | Notes |
|-----------|------|-------|
| Namecheap | [Buy](https://namecheap.pxf.io/c/7622160/386170/5618) | Card required |
| Spaceship | [Buy](https://spaceship.sjv.io/c/7622160/1794549/21274) | Supports channel |
| BigRock | [Buy](https://www.bigrock.in/) | UPI supported (~₹883/yr) |
| GoDaddy | [Buy](https://www.godaddy.com/en-in) | UPI supported |
| Hostinger | [Buy](https://www.hostinger.com/in) | UPI supported (~₹904/yr) |

---

## All Links

### Tools
- [Logo & Favicon](https://logofa.st/)
- [Ahrefs Keyword Generator](https://ahrefs.com/keyword-generator)
- [Ahrefs Traffic Checker](https://ahrefs.com/traffic-checker)
- [Instant Domain Search](https://instantdomainsearch.com/)
- [Google Analytics](https://analytics.google.com)

### Design & AI Skills
- [Vercel Design MD](https://getdesign.md/vercel/design-md) — `npx getdesign@latest add vercel`
- [Web Design Guidelines Skill](https://www.skills.sh/vercel-labs/agent-skills/web-design-guidelines)
- [Tailwind v4 Docs](https://www.skills.sh/lombiq/tailwind-agent-skills/tailwind-4-docs) | [GitHub](https://github.com/Lombiq/Tailwind-Agent-Skills)

### AstroJS
- [AstroJS Docs](https://docs.astro.build/en/getting-started/)
- [AstroJS Cloudflare Deploy](https://docs.astro.build/en/guides/deploy/cloudflare/)
- [AstroJS MCP Server](https://docs.astro.build/en/guides/build-with-ai/#astro-docs-mcp-server)
- [AstroJS i18n Recipe](https://docs.astro.build/en/recipes/i18n/)

### Cloudflare
- [Cloudflare Dashboard](https://dash.cloudflare.com/login)

### SEO & Search Engines
- [Google Search Console](https://search.google.com/search-console/about)
- [Bing Webmaster](https://www.bing.com/webmasters/about)
- [Google AdSense](https://adsense.google.com/start/)

### More from CompileFuture
- [Rejected By IIT. Now Making 50 LPA From My Own AI Business.](https://compilefuture.com/blog/making-50-lpa-from-my-own-ai-business/)
