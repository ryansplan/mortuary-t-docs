# Documentation quality workflow

Every proposed change should be reviewed through a pull request before it is
merged and published.

## Automated checks

The quality workflow runs the following checks:

1. **Markdown style:** identifies inconsistent Markdown structure and syntax.
2. **Link validation:** detects broken internal and external links.
3. **Strict site build:** detects missing navigation pages, invalid references,
   and build warnings.

## Review workflow

```text
Create issue
  -> create branch
  -> write or revise Markdown
  -> preview locally
  -> open pull request
  -> pass automated checks
  -> complete editorial review
  -> merge to main
  -> publish to GitHub Pages
```

## Definition of done

A documentation change is complete when:

- The content is technically verified.
- Examples contain only fictional or sanitized information.
- The intended audience and user need are clear.
- Links and navigation work.
- Automated checks pass.
- The pull request records the review decision.
