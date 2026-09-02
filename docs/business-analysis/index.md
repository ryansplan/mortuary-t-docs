# Business-analysis artifacts

This section connects the Mortuary T First Call workflow from business need
through validation and release recommendation.

## Traceability chain

```text
Business need
  -> requirement
  -> user story
  -> acceptance criteria
  -> process flow
  -> UAT scenario
  -> test result
  -> release decision
```

## First Call case study

| Artifact | What it demonstrates |
| --- | --- |
| [First Call business requirements](first-call-requirements.md) | Business need, scope, actors, requirements, business rules, and testable acceptance criteria |
| [First Call requirements traceability](first-call-traceability.md) | Requirement-to-documentation and requirement-to-test coverage |
| [First Call UAT plan and results](first-call-uat.md) | Test planning, execution evidence, defect management, retesting, and release recommendation |

Together, these artifacts show how a technical writer or business analyst can
maintain alignment among user documentation, product requirements, test
evidence, and release readiness.

## Portfolio boundaries

- The package uses fictional or sanitized information.
- The test results represent a sanitized record of the documented product
  behavior; this public site is not the production test system of record.
- External message delivery is outside Mortuary T's verification boundary.
- Production source, credentials, real case records, and security-sensitive
  implementation details are excluded.
