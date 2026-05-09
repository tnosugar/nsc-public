# public/website/

Rendered HTML pages for the North Star Communications website. This folder mirrors verbatim to `tnosugar/nsc-public-website` via the workflow at `.github/workflows/sync-public.yml`. Pages serve at `https://tnosugar.github.io/nsc-public-website/<filename>.html` (or at the configured CNAME, when one is set).

Canonical sources for each page live in `content/`. Edit `content/` first, regenerate the HTML, commit both. Do not edit these HTML files directly without an entry in the corresponding `content/` doc.

## Pages

- **`home.html`** — marketing landing page. Renders from [`content/web/pages/home/PAGE.md`](../../content/web/pages/home/PAGE.md). Five sections (hero, services, frameworks, work, values, team, contact).
- **`way-of-work.html`** — long-form Way of Work framework page. Primary entry for the WoW framework from the main nav. Renders from [`content/frameworks/way-of-work/FRAMEWORK.md`](../../content/frameworks/way-of-work/FRAMEWORK.md). Links out to the interactive diagram via a "See it in motion" callout.
- **`how-we-work.html`** — interactive Way of Work diagram. Clickable four-track cycle with a detail panel. Reached via callout from `way-of-work.html`; nav marks "The Way of Work" active.
- **`communications-compass.html`** — long-form Communications Compass framework page. Primary entry for the Compass framework from the main nav. Renders from [`content/frameworks/communications-compass/FRAMEWORK.md`](../../content/frameworks/communications-compass/FRAMEWORK.md). Links out to the interactive diagram via a "See it in motion" callout.
- **`value-communications-compass.html`** — interactive four-armed Communications Compass. Each arm reveals per-service and per-value breakdowns for one stakeholder group. Reached via callout from `communications-compass.html`; nav marks "The Communications Compass" active.

## Adding a new page

Mirror an existing page's structure rather than inventing a new pattern. Extend the main nav block across all files. Add the canonical source under `content/`. The folder-as-contract sync workflow picks up new files automatically — no manifest edit needed (legacy `.sync-public.yml` was retired during the 2026-05-09 migration).
