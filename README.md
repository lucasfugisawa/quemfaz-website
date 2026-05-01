# quemfaz-website

Static site hosted at [https://quemfaz.com.br](https://quemfaz.com.br) via GitHub Pages.

## What's here

- `index.md` — landing page (placeholder)
- `privacidade.md` — privacy policy (DRAFT, awaiting lawyer review)
- `termos.md` — terms of use (DRAFT, awaiting lawyer review)
- `diretrizes.md` — community guidelines (DRAFT)
- `CNAME` — custom domain config (`quemfaz.com.br`)
- `_config.yml` — Jekyll theme + metadata

## How it deploys

Plain GitHub Pages — no GitHub Actions workflow needed. Pushes to `main` trigger an automatic Pages build via the built-in Jekyll renderer. The `CNAME` file at the repo root + a Route 53 A-alias from `quemfaz.com.br` to the GitHub Pages IPs handles the custom domain.

GitHub provisions the TLS cert via Let's Encrypt automatically (~5 min after first push + DNS resolves correctly).

## Linked from the app

The app's `/app-config` endpoint exposes:

- `privacyUrl: "https://quemfaz.com.br/privacidade.html"`
- `termsUrl: "https://quemfaz.com.br/termos.html"`
- `communityGuidelinesUrl: "https://quemfaz.com.br/diretrizes.html"`
- `supportEmail: "suporte@quemfaz.com.br"`

When the privacy policy is updated in a way that requires user re-consent (e.g., after the LGPD addendum lands per a lawyer's review), bump `LEGAL_REQUIRED_PRIVACY_VERSION` in the prod SSM parameter store. The client compares this against the version the user has accepted and re-prompts on mismatch.

## Editing

Pure Markdown. No build step needed locally; just edit `.md` files and push.

To preview locally with Jekyll (optional):

```bash
gem install bundler jekyll
bundle init
bundle add jekyll jekyll-theme-minimal
bundle exec jekyll serve
# http://localhost:4000
```
