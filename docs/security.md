# Security and privacy

This documentation repository is intentionally isolated from Mortuary T's
production systems.

## Never include

- Production source code
- Credentials, tokens, keys, or environment files
- Real customer, patient, decedent, or case information
- Protected health information or personally identifiable information
- Internal-only URLs, logs, or infrastructure details
- Security controls that would create unnecessary operational risk

## Safe portfolio practices

- Use fictional data in every example.
- Crop or recreate screenshots after removing identifying information.
- Describe architecture only at the level required to explain the workflow.
- Replace production endpoints and identifiers with clearly labeled examples.
- Review every pull request for privacy and security before merging.

## Repository isolation

The workflows in this repository read only its documentation files. They build
a static site and publish that output to GitHub Pages. They do not call,
deploy, modify, or authenticate to Mortuary T.
