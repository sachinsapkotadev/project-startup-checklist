# Step 5: Building the Website with AI — Setup Checklist

## 1. Install AstroJS

Open VS Code terminal (separate from Claude Code terminal):

```bash
npm create astro@latest .
```

- Press Enter for all defaults
- Choose the **"Basic"** template
- Say **Yes** to initialize Git

AstroJS is now installed in your project root.

---

## 2. Add Vercel's design.md

Vercel publishes a design system document that trains AI agents to produce clean, professional UI.

```bash
npx shadcn@latest init
```

Or search "Vercel design.md" on Google and follow the install command in the description.

This single file dramatically improves the visual quality of AI-generated websites.

---

## 3. Install AI Skills

Claude Code supports "skills" — specialized knowledge packs that guide the AI.

### Web Design Guidelines (consistent, professional UI):

```bash
claude mcp add web-design-guidelines
```

### Tailwind 4 Docs (fixes Tailwind v4 knowledge gaps):

```bash
claude mcp add tailwind-v4-docs
```

---

## 4. Add Astro JS MCP Server

AI agents are trained on older versions of Astro. The Astro JS MCP server gives Claude Code access to the latest Astro documentation in real time.

1. Search "Astro JS MCP" on Google
2. Go to the first link
3. Copy the install command
4. Paste it in VS Code terminal

This ensures Claude Code writes modern, correct Astro syntax.

---

## Done

Your AstroJS project template is ready. You can now start building with AI assistance.
