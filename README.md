# Hold On landing page

Static English page: pain → 3 steps → **$9.99** → email intent.

Open locally: double-click `index.html`, or:

```bash
cd landing && python3 -m http.server 8765
# then http://127.0.0.1:8765/
```

Free host later: GitHub Pages / Cloudflare Pages / Netlify — drop this folder; no build step.

## Wire the form (free)

The live endpoint is `https://formspree.io/f/xqppdwdw`. Submissions POST to Formspree.

### Option A — Formspree (free tier)

1. Sign up at https://formspree.io (free).
2. Create a form → copy the endpoint, e.g. `https://formspree.io/f/xxxxxxxx`.
3. In `index.html`, change:

```html
<form action="https://formspree.io/f/xxxxxxxx" method="POST" id="intent-form">
```

4. Optionally remove or keep the small `<script>` — with a real `action`, the browser POSTs normally (script only intercepts `action="#"`).

### Option B — Tally (free)

1. Create a form at https://tally.so.
2. Either embed Tally, or use their form URL as CTA instead of the inline form.
3. For email-only: keep one Email block; set thank-you to “You're on the list”.

### Option C — mailto (zero account)

```html
<form action="mailto:YOU@example.com" method="POST" enctype="text/plain" id="intent-form">
```

Opens the visitor’s mail app — fine for tiny tests; not reliable for counting ≥10 intents.

## Counting intents (money gate)

Export emails weekly. Success bar for paying Apple **$99**: **≥10 unique intents in 7 days** — see `/workspace/hold-on-oss/MONEY_FUNNEL.md`.

Do **not** commit the email list into any public repo.
