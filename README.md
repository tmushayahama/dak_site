# bv_site

Published demo build of **BuildVerify Hub** — the construction-progress
verification app from the Diaspora Trust Platform suite.

Live: https://tmushayahama.github.io/bv_site/

## This repo is generated output

`dist/` is a Vite production bundle built from `build-verify-hub-site` in the
`trust-tools` monorepo. **Do not edit it by hand.** To publish a new version:

```bash
cd ../trust-tools
./scripts/deploy-bv-demo.sh
cd ../bv_site && git add -A && git commit -m 'deploy' && git push
```

Pushing to `main` triggers `.github/workflows/pages.yml`, which uploads `dist/`
to GitHub Pages.

The demo runs entirely in the browser — no backend. State is Redux + seed data
in `localStorage`.
