# WLA release notes

Public, read-only data feed consumed by the WLA app at runtime for its
in-app "What's new" screen and mandatory-update gate. An already-installed
build fetches `manifest.json` from this repo (via jsDelivr) to know the
latest release's changelog and the minimum version it must be running.

**This repo is a publish target, not a source.** Do not edit `manifest.json`
here directly — it is auto-published by CI from the private `WLA_APP`
repo's `docs/release-notes/manifest.json` every time that file changes on
`main`. Edits made here will be overwritten on the next publish.

Served to the app via jsDelivr:
```
https://cdn.jsdelivr.net/gh/eSignus/wla-release-notes@main/manifest.json
```
