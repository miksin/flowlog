# Flowlog

A dead-simple quick-note web app. One input box, Enter saves, notes stack into a time-ordered feed. Zero dependencies, zero build step — data lives in your browser and never leaves your machine.

## Features

- Single composer, Enter to save — new notes flash with a highlighter sweep
- Automatic day grouping (TODAY / YESTERDAY / date + weekday)
- Instant search (`/` focuses it, Esc clears)
- Click a note to edit in place, hover to delete
- localStorage persistence, offline-capable PWA (installable to home screen)
- Warm paper-grain retro light theme

## Deploy

It is a static bundle; drop it on any web server (service worker requires HTTPS or localhost):

```bash
python3 -m http.server 8000
# -> http://localhost:8000/
```

## Data shape

Notes are a plain array of `{id, text, ts}` under the `flowlog.v1` localStorage key — future sync or export is trivial.

## Not built yet (on purpose)

Tags, todo checkboxes, cross-device sync. Add them only once real usage asks for them.
