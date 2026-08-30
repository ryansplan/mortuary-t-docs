# Mortuary T Documentation Portfolio

This repository is a sanitized documentation portfolio based on Mortuary T. It
demonstrates a docs-as-code workflow without connecting to the production app,
source repository, database, secrets, or deployment process.

## What this portfolio demonstrates

- Markdown documentation managed in Git
- Branch-and-pull-request reviews
- Automated Markdown, link, and site-build checks
- Automated publication through GitHub Pages
- Technical-writing and business-analysis artifacts

## Preview the site locally on Windows

Install Python 3.11 or later, open PowerShell in the repository folder, and run:

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
mkdocs serve
```

Open `http://127.0.0.1:8000` in a browser. Press `Ctrl+C` to stop the preview.

## Recommended contribution workflow

1. Create a branch from `main`.
2. Edit or add Markdown files under `docs/`.
3. Preview the site locally.
4. Commit and push the branch.
5. Open a pull request.
6. Confirm the automated checks pass.
7. Review the rendered changes and merge the pull request.
8. Let the Pages workflow publish the approved `main` branch.

See [Contributing](docs/contributing.md) for sample commands.

## Publish with GitHub Pages

After uploading this repository to GitHub:

1. Open **Settings > Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Open the **Actions** tab and confirm that workflows are enabled.
4. Push or merge a change into `main`.
5. Open the completed **Publish documentation site** workflow to find the URL.

The expected public address is:

```text
https://ryansplan.github.io/mortuary-t-docs/
```

## Safety boundary

Only sanitized portfolio content belongs here. Do not add production source,
credentials, access tokens, environment files, real customer information,
protected health information, or proprietary implementation details.
