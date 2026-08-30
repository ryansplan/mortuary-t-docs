# Contributing

Use a branch and pull request for every documentation change. This creates a
visible review history and demonstrates a genuine docs-as-code workflow.

## Create a documentation branch

```powershell
git switch main
git pull
git switch -c docs/describe-change
```

Replace `describe-change` with a short description, such as
`docs/add-getting-started`.

## Preview and validate

```powershell
mkdocs serve
```

Review the changed pages locally. The automated checks will run after you push
the branch and open a pull request.

## Commit and push

```powershell
git add .
git commit -m "docs: add concise description"
git push -u origin docs/describe-change
```

Open a pull request on GitHub. Explain the audience, purpose, technical source,
validation performed, and privacy review.

## Merge and publish

Merge only after the quality checks pass and the content has been reviewed.
The publishing workflow builds and deploys the approved `main` branch.
