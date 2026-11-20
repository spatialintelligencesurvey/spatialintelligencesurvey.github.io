# Spatial Intelligence Survey

This repository publishes a static academic survey at https://spatialintelligencesurvey.github.io/ using GitHub Pages.

## Files and boundaries

- `index.html` is the published entry point, including prose, references, styles, and the embedded taxonomy figure. Edit this file directly; there is no build step.
- `framework.png` is the original author-provided figure. Preserve it and the embedded image unless explicitly asked to replace them. Avoid printing the base64 image line in tool output.
- `VERSION` and the page's `survey-version` metadata identify the displayed survey version. Maintenance fixes may retain that version; do not overwrite original tags or reinterpret the source-snapshot hash as a hash of the current HTML.
- `README.md` documents publication and maintenance status.
- `TASKS.md` is the local task board. `audits/` contains local review snapshots, model output, and verification artifacts. Do not stage or publish these records as part of a website fix without a specific reason and authorization.
- Never put API keys, tokens, private model prompts, or credentials in published files. The Pages workflow uploads all tracked repository files.

## Environment and entry points

Open `index.html` directly in a browser, or preview with `python3 -m http.server 8000 --bind 127.0.0.1`. No backend, Node build, database, or GPU/server access is required.

## Validation and publication

- Run `git diff --check`, verify unique HTML IDs and internal link targets, and check the exact reference URL changed.
- For visibility/layout changes, inspect actual browser rendering at desktop and narrow/mobile viewport sizes. Temporarily hidden tables must also hide their captions, notes, and navigation references; keep the table source for restoration.
- Use a bounded browser check and retain screenshots locally under `audits/` when useful. No broad test suite or model experiment is needed for a citation/visibility fix.
- Before committing, inspect the staged file list and exclude local audit artifacts and unrelated changes.
- `.github/workflows/static.yml` deploys a push to `main`. Verify the workflow and the live page when publishing; do not call a local edit or a queued deployment a completed publication.

## Known failure modes

The local clone can lag behind the published survey. Fetch and compare the remote before editing; preserve untracked local records. Citation numbering alone does not establish source correctness: check the linked paper title. Some table cells remain overly generic; hiding a table does not repair its metrics, and a future restoration requires a separate metric review.

This is a presentation repository, not an experiment runner. Research probes, API calls, and model comparisons require task-specific records and are not prerequisites for routine website maintenance.
