# Legal pages

`privacy.md` and `terms.md` are the two pages App Review opens. Both are required
before submission: 5.1.1(v) and 3.1.2 respectively.

## Publishing on GitHub Pages

1. Push this repo (or just this `legal/` folder) to GitHub.
2. **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*,
   branch = `main`, folder = `/legal` (or `/` if the folder is the repo root).
3. GitHub renders the Markdown through Jekyll, so `privacy.md` publishes at
   `/privacy` and `terms.md` at `/terms`.

That gives you, for example:

```
https://<username>.github.io/<repo>/privacy
https://<username>.github.io/<repo>/terms
```

To use `tygr.app` instead, point the domain at GitHub Pages and set it under
**Settings → Pages → Custom domain**. The URLs then become `https://tygr.app/privacy`
and `https://tygr.app/terms`, which is what the app already links to.

## Then update the app

Whichever URLs you end up with, they must match `AppLinks` in
[`tygr/PaywallView.swift`](../tygr/PaywallView.swift). Those two constants are
the only place the app names them — the paywall footer and Settings → About both
read from there.

## Check before submitting

- [ ] Both URLs load in a private browser window, with no login and no redirect
      to a parking page.
- [ ] `support@tygr.app` receives mail. Both pages name it as the way to exercise
      data rights, and Settings → Contact Support opens it.
- [ ] The controller name at the top of each page ("Abhinav Sreejesh") is the
      name you actually want to trade under. If you incorporate, change both.
- [ ] The governing-law clause in `terms.md` says England and Wales. Change it if
      that is not where you are.
- [ ] The privacy policy URL is also entered in App Store Connect, separately
      from the app itself.

## Keeping the policy true

The policy describes exactly what the code does today, including the split of
what the app collects. If you add a framework that collects something
new — HealthKit, an analytics SDK, location — the policy and
`Support/PrivacyInfo.xcprivacy` both have to change with it.
