# Flashback updates

`latest.json` tells the Flashback app which version is current. Flashback reads it once a day to show an "update available" banner. Nothing else lives here.

Each release replaces `latest.json` with the `dist/latest.json` that `packaging/build.sh` writes:

```json
{"version": "2.0.1", "released": "2026-11-05",
 "notes_url": "https://github.com/djhitchMNDH/photo-recap-wall/releases/tag/v2.0.1",
 "download_url": "https://github.com/djhitchMNDH/photo-recap-wall/releases/tag/v2.0.1",
 "summary": "One line for the banner."}
```

Publish the release first, then update this file, so the banner never points at a release that doesn't exist yet.
