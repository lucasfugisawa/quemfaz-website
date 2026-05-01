# quemfaz-website

Static site hosted at [https://quemfaz.com.br](https://quemfaz.com.br) via GitHub Pages.

## What's here

- `index.html` — landing page (custom design, fully self-contained HTML/CSS)
- `privacidade.md` — privacy policy (publication-ready, LGPD-compliant)
- `termos.md` — terms of use (publication-ready)
- `diretrizes.md` — community guidelines
- `_layouts/default.html` — Jekyll layout shared by the legal-doc markdowns
- `assets/css/{tokens,landing,docs}.css` — design tokens + page-specific styles
- `assets/fonts/` — Plus Jakarta Sans (5 weights, regular + italic)
- `assets/img/{app-icon,logo-wordmark}.svg` — favicon + wordmark
- `CNAME` — custom domain config (`quemfaz.com.br`)
- `_config.yml` — Jekyll config (no theme; layout + CSS are project-owned)

## How it deploys

Plain GitHub Pages — no GitHub Actions workflow needed. Pushes to `main` trigger an automatic Pages build via the built-in Jekyll renderer. The `CNAME` file at the repo root + a Route 53 A record from `quemfaz.com.br` to the GitHub Pages IPs handles the custom domain.

GitHub provisions the TLS cert via Let's Encrypt automatically (~5 min after first push + DNS resolves correctly).

## Linked from the app

The app's `/app-config` endpoint exposes:

- `privacyUrl: "https://quemfaz.com.br/privacidade.html"`
- `termsUrl: "https://quemfaz.com.br/termos.html"`
- `communityGuidelinesUrl: "https://quemfaz.com.br/diretrizes.html"`
- `supportEmail: "contato@quemfaz.com.br"` (rename pending — see main repo `docs/launch/email-provider-setup.md`)

When the privacy policy is updated in a way that requires user re-consent (e.g., adding a new sub-processor like Cloudflare Web Analytics), bump `LEGAL_REQUIRED_PRIVACY_VERSION` in the prod SSM parameter store. The client compares this against the version the user has accepted and re-prompts on mismatch.

## Editing

Pure HTML + Markdown. No build step needed locally; just edit and push.

To preview locally with Jekyll (optional):

```bash
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve
# http://localhost:4000
```

## Analytics

The landing has commented-out snippets for **Cloudflare Web Analytics** (recommended) and **GoatCounter** in `index.html` and `_layouts/default.html`. Both are zero-cookie, LGPD-friendly. Pick one, sign up, replace the placeholder token in BOTH files, and uncomment. Then add the provider as a sub-processor in `privacidade.md` Section 5 before going live. See `docs/launch/website-analytics-setup.md` in the main quemfaz repo for the playbook.

## Design system

The landing was built from a custom design brief (`docs/launch/landing-page-design-brief.md` in the main quemfaz repo) handed off by Claude Design. The "Confiança quente" palette + Plus Jakarta Sans typography are documented in `assets/css/tokens.css` as CSS custom properties — they're the same tokens the mobile app should use. If a color/spacing changes in the design system, update `tokens.css` and both surfaces stay in sync.
