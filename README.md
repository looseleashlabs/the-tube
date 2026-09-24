# The Tube

A 1990s cable-TV guide for your YouTube subscriptions, built for Google TV (open it in Firefox on the TV).

- Channels scheduled from the creators you subscribe to, plus For You, Unseen Today, a self-managing VCR, lists,
  and genre/group channels
- Remote-first: ↑/↓ channels, OK tunes in, → options, ←/→ browse while watching, Back closes
- Signs in with a code you approve on your phone (google.com/device)

## Publishing

Pushing to `main` deploys to GitHub Pages via `.github/workflows/pages.yml`. The TV sign-in client comes from the
repository secrets `TV_CLIENT_ID` and `TV_CLIENT_SECRET` (a Google Cloud OAuth client of type
"TVs and Limited Input devices") and is written into the site as `config.json` at deploy time.
