# @core/seo

[![genpm](https://api.genpm.net/v1/badge/@core/seo.svg)](https://genpm.net/p/@core/seo) ![license](https://img.shields.io/badge/license-MIT-blue)

> SEO for GenPM sites: metadata with canonical and hreflang, chunked sitemaps, robots.txt, llms.txt and safe JSON-LD

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/lib/seo`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/seo
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/seo`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/seo with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Everything search engines and crawling agents read: page metadata with site defaults (title template, description,
canonical, hreflang, Open Graph, Twitter, robots), a sitemap index with chunks of 50,000 URLs built from any
registered `SitemapSource`, `robots.txt`, `llms.txt` and schema.org JSON-LD builders with script-safe escaping.
No tables. OG image generation is out of scope for 1.0.

## At a glance

- **GenPM dependencies** (installed with it): [@core/site](https://genpm.net/p/@core/site), [@core/contracts](https://genpm.net/p/@core/contracts)
- **npm dependencies** (proposed, never installed without asking): `zod`
- **Environment variables** (added to `.env.example`): `SITE_URL`, `SEO_NOINDEX`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/lib/seo`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
