# Binayak Sinha — Portfolio

A game-menu style portfolio. Plain HTML/CSS/JS, no build step, hosted on GitHub Pages.

## Updating content

All portfolio content lives in **`data.json`**:

| Key              | What it fills                    |
|------------------|----------------------------------|
| `skills`         | ARSENAL screen (grouped tags)    |
| `experience`     | QUESTS screen (`active: true` shows the IN PROGRESS stamp) |
| `projects`       | MISSIONS screen. Optional fields: `badge`, `link` (repo/demo URL) |
| `certifications` | TROPHIES screen (grouped by issuer) |

Counters on the menu and profile screen, and the project filter buttons, are calculated from this file automatically.
New project categories get their own filter button automatically.

Bio, education and contact links are in `index.html` (search for `p-profile` / `p-contact`).

## Previewing locally

`index.html` loads `data.json`, which browsers block when the file is opened by double-clicking.
Run a tiny local server from this folder instead:

```
python -m http.server 8000
```

then open http://localhost:8000. (VS Code's "Live Server" extension works too.)

## Deploying

Commit and push to `main`; GitHub Pages republishes automatically.
