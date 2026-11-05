[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [日本語](README.ja.md)

# Hold On — landing site

Static landing site for **Hold On** (Chinese name: 先别买), an iOS app concept that adds a cool-down before impulse purchases. The app is **not released yet** and is not on the App Store; the landing page collects early-access emails.

Live site: https://xuqijx.github.io/hold-on-landing/

## What Hold On is meant to do

1. **Share a product** from a shopping app into Hold On.
2. **Cool down by price** — the wait timer scales with the item's cost.
3. **Decide later** — when the timer ends, buy it or let it go, and see what you didn't spend.

Planned pricing shown on the page: $9.99 one-time unlock, no subscription, no ads.

## Repository layout

- `index.html` — Hold On landing page with an email "notify me" form (Formspree endpoint).
- `packs/` — separate static sales pages for digital packs (templates/kits for freelancers); hub at `/packs/`. Buy buttons link to Gumroad. See `packs/README.md`.
- `guides/` — long-form guides (e.g. impulse-buying cool-down, fixed-fee scope creep) at `/guides/`. See `guides/README.md`.
- `favicon.ico`, `favicon-32.png` — site icons.
- `robots.txt`, `sitemap.xml`.

## Run locally

No build step.

```bash
python3 -m http.server 8765
# open http://127.0.0.1:8765/
```

Note: favicon paths use the GitHub Pages project prefix `/hold-on-landing/`, so icons may not show when served from the root locally.

## Email form

The form in `index.html` POSTs to Formspree (`https://formspree.io/f/xqppdwdw`). To use your own, replace the form `action`. Do not commit collected email lists to this repo.
