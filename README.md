# tygr.site

This repo publishes `tygr.site`: the landing page, and the two legal documents
App Review opens. GitHub Pages builds it from `main`.

| File | Serves | Notes |
|---|---|---|
| `index.html` | `/` | Hand-written, no build step. It has no front matter, so Jekyll copies it untouched. |
| `CNAME` | — | The custom domain, `tygr.site`. |
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

The `CNAME` file in this repo is what tells GitHub Pages to serve the site at
`tygr.site`. Delete it and the site goes back to `github.io`.

DNS for `tygr.site` is on Cloudflare: two records, both **DNS only** (grey cloud —
the proxy gets in the way of GitHub issuing the certificate).

| Type | Name | Target |
|---|---|---|
| `CNAME` | `@` | `abhinavsreejeshcodes.github.io` |
| `CNAME` | `www` | `abhinavsreejeshcodes.github.io` |

A CNAME on the bare domain isn't normally allowed; Cloudflare flattens it into
GitHub's addresses, which is what makes it work next to the mail records. The
target is the host name only — DNS can't point at a path like `/tygr-legal/`.
GitHub works out which repo to serve from the `CNAME` file.

Once GitHub has issued the certificate, tick **Enforce HTTPS** under
Settings → Pages.

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
