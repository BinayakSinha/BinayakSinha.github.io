# Binayak Sinha — Portfolio

A game-menu style portfolio. Plain HTML/CSS/JS, no build step, hosted on GitHub Pages.

## Updating content

All portfolio content lives in **`data.json`**:

| Key              | What it fills                    |
|------------------|----------------------------------|
| `profile`        | Bio paragraphs (wrap words in `**…**` to highlight), location/language tags, education card |
| `skills`         | ARSENAL screen. Each item is a string, or `{"name": "Kubernetes", "level": "Basic"}` to show it dashed as foundational |
| `experience`     | QUESTS screen: `points` (bullets), `tech` (chips), optional `location`; `active: true` shows the IN PROGRESS stamp |
| `projects`       | MISSIONS screen. Optional fields: `badge`, `link` (repo/demo URL; no link = no button) |
| `certifications` | TROPHIES screen (grouped by issuer) |

Counters on the menu and profile screen, and the project filter buttons, are calculated from this file automatically.
New project categories get their own filter button automatically.

Contact links are in `index.html` (search for `p-contact`).

## Previewing locally

`index.html` loads `data.json`, which browsers block when the file is opened by double-clicking.
Run a tiny local server from this folder instead:

```
python -m http.server 8000
```

then open http://localhost:8000. (VS Code's "Live Server" extension works too.)

## Deploying

Commit and push to `main`; GitHub Pages republishes automatically.
