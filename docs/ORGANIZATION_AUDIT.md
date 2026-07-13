# Public account audit

Audit date: 2026-07-13

GitHub currently classifies `truefoxaiinc` as a personal account. This repository therefore provides shared standards, while the visible profile is served by `truefoxaiinc/truefoxaiinc`.

## Public repository inventory

| Repository | Purpose | Language | Last update | README | License | CI/CD | Security documentation | Recommendation |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `adhd-assessment-platform` | Django REST backend for authentication, ADHD self-assessment, learning progress, content delivery, payments and attention-session summaries | Python | 2026-07-10 | Good technical detail; missing product status, architecture, privacy, license, support and roadmap | Missing | Missing | Missing | Make private pending privacy and licensing review; retain and consider renaming afterward |

## Findings

- Potential user or customer images are committed under `media/profile_images/`. Do not expose or reproduce their contents during remediation.
- A roughly 95 MiB model artifact is committed at `files/shape_predictor_68_face_landmarks.dat`.
- Generated and vendor assets appear duplicated under `assets/` and `static/`.
- The README contains a production-style IP address that should be replaced with a neutral placeholder.
- No root project license, CI workflows or security policy were found.
- Development configuration includes predictable fallback values; production must fail closed when secrets are absent.
- JWT lifetimes should be reviewed and shortened according to the product's threat model.
- No committed private-key, AWS access-key, database-URL or real `.env` pattern was detected in the inspected checkout. Full-history secret scanning is still required.

## Manual controls to verify

- Secret scanning and push protection
- Protected default branch
- Required pull-request reviews and CI checks
- Dependabot and dependency review
- CodeQL or equivalent static analysis
- Signed or attestable releases
- Semantic versioning and release notes
