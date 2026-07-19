# sharibako-web

The website for [Sharibako](https://github.com/sageframe-no-kaji/sharibako) —
a native Mac app and CLI that keeps development secrets in one encrypted,
git-backed vault behind Touch ID.

Static site, no build step: four HTML pages sharing one stylesheet, wearing
the pālana palette the app itself wears (light + dark via
`prefers-color-scheme`).

- `index.html` — landing page
- `how-it-works.html` — the technical deep dive (secrets from zero, the
  "encrypting your working .env is theater" argument, architecture, threat
  model, alternatives)
- `faq.html` — question-shaped answers, corrections-first
- `help.html` — every workflow step by step + full CLI reference

Copy is sourced from the product repo's `docs/secrets-explained.md` — when
the story changes, change it there first, then re-derive these pages.

## Deploy

Cloudflare Workers static assets, same pattern as m4Bookmaker:

```
npx wrangler deploy
```

Target: `sharibako.sageframe.net`.
