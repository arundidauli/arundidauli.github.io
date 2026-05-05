# Repository Guidelines

## Project Structure & Module Organization
This repository is a small static site. [`index.html`](/Users/arunkumar/Documents/arundidauli.github.io/index.html) contains the full application: HTML markup, embedded CSS, and any inline behavior. [`README.md`](/Users/arunkumar/Documents/arundidauli.github.io/README.md) is a short portfolio summary. There is no `src/`, `tests/`, or build output directory today, so keep changes localized and avoid introducing tooling unless the repo grows enough to justify it.

## Build, Test, and Development Commands
No build step is required.

- `open index.html`
Opens the page in a browser for a quick visual check on macOS.

- `python3 -m http.server 8000`
Serves the site locally at `http://localhost:8000` and is the preferred option when validating relative asset paths or browser behavior.

- `git diff -- index.html`
Review page changes before committing.

## Coding Style & Naming Conventions
Use 2-space indentation in HTML and CSS to match the existing file. Prefer semantic sectioning and keep styles grouped by component area, as the current page does. Reuse existing CSS custom properties in `:root` instead of adding hard-coded colors repeatedly. Use clear class names such as `hero-*`, `badge-*`, or `project-*`; avoid one-letter or purely presentational names.

## Testing Guidelines
There is no automated test suite in this repository. Every change should include manual verification in at least one desktop browser and one narrow/mobile viewport. Check for layout regressions, broken links, and console errors. If JavaScript is added later, place simple smoke checks near the feature or introduce a minimal test runner with a clear reason.

## Commit & Pull Request Guidelines
Recent history favors short imperative commits like `Update index.html`, `Fix missing newline at end of index.html`, and `Update HTML meta description and add certification badge`. Keep that style, but make the subject specific to the user-visible change. PRs should include:

- a concise summary of what changed
- before/after screenshots for visual updates
- linked issue or task reference when applicable
- notes on manual verification performed

## Content & Asset Notes
Optimize any added images before committing and keep externally hosted dependencies intentional. If the page starts accumulating assets, create an `assets/` directory and update this guide accordingly.
