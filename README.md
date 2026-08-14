# WLA release notes

Public, read-only data feed consumed by the WLA app at runtime for its
in-app "What's new" screen and mandatory-update gate. An already-installed
build fetches `manifest.json` from this repo (via `raw.githubusercontent.com`)
to know the latest release's changelog and the minimum version it must be
running.

**This repo is a publish target, not a source.** Do not edit `manifest.json`
here directly — it is auto-published by CI from the private `WLA_APP`
repo's `docs/release-notes/manifest.json` every time that file changes on
`main`. Edits made here will be overwritten on the next publish.

Served to the app via `raw.githubusercontent.com`, not jsDelivr — jsDelivr's
`@main`→commit resolution was live-tested and found to lag a confirmed, purged
push by several minutes to 10+ minutes, unacceptable for a mandatory-update
gate:
```
https://raw.githubusercontent.com/eSignus/wla-release-notes/main/manifest.json
```
