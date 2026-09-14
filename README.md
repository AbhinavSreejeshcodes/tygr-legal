# tygr.site

This repo publishes `tygr.site`: the landing page, and the two legal documents
App Review opens. GitHub Pages builds it from `main`.

| File | Serves | Notes |
|---|---|---|
| `index.html` | `/` | Hand-written, no build step. It has no front matter, so Jekyll copies it untouched. |
| `img/` | `/img/…` | Mascot and icons, resized from the app's asset catalog. |
| `privacy.md` | `/privacy/` | Rendered by Jekyll with the primer theme. |
| `terms.md` | `/terms/` | Same. |

`permalink: pretty` in `_config.yml` is what puts the legal pages at `/privacy/`
and `/terms/`. `/privacy.html` is a 404 — don't link to it.

## The app links here

`tygr/AppLinks.swift` in the app repo holds the only copies of the legal URLs.
They point at `abhinavsreejeshcodes.github.io/tygr-legal/…`. Once `tygr.site` is
the custom domain, GitHub redirects those addresses to `tygr.site`, so builds
already shipped keep working. Switch the constants to `https://tygr.site/privacy/`
and `/terms/` in a later build if you like — never before the custom domain is
serving, or the app ships dead links.

## Custom domain

DNS for `tygr.site` is on Cloudflare. For GitHub Pages to serve it:

- apex `A` records → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
  `185.199.111.153`, **DNS only** (grey cloud — the proxy gets in the way of
  GitHub issuing the certificate)
- `www` `CNAME` → `abhinavsreejeshcodes.github.io`, DNS only
- Settings → Pages → Custom domain `tygr.site`, then **Enforce HTTPS** once it's
  offered

Setting the custom domain in GitHub's UI commits a `CNAME` file to `main`, so
pull before your next push.

Leave the `MX` and `TXT` records alone. They are Cloudflare Email Routing, which
is what makes `support@tygr.site` receive mail.

## Keeping it true

- The privacy policy describes exactly what the app does today. If the app starts
  collecting something new — HealthKit, analytics, location — the policy, its
  "Last updated" date and `Support/PrivacyInfo.xcprivacy` all change with it.
- The landing page names specific features. If one leaves the app, it leaves the
  page too.
- `support@tygr.site` has to keep receiving mail: both documents name it as the
  way to exercise data rights, and Settings → Contact Support opens it.
