# Documentation conventions

Status: active working convention · Date: 2026-09-24

- Write Markdown with clear headings, tables for comparisons and Mermaid for useful architecture/ER diagrams.
- Write one section at a time; distinguish proposed recommendations from accepted decisions.
- Identify status (draft, proposed, accepted, superseded), date and applicable scope.
- Include purpose, background, requirements, design, alternatives, decision, risks, open questions and next steps where appropriate. Avoid empty boilerplate.
- Explain concepts for a software engineering student, increasing depth as needed.
- Give first-release designs implementation-level detail; keep distant features at research depth.
- Verify changeable technical facts, prices, capabilities, licenses and security guidance using reliable, preferably official sources. Record URL, verification date and uncertainty beside the claim.
- Record requirement IDs when requirements are written; link them to ADRs, milestones and verification instead of duplicating their definitions.
- Keep the decision log as an index. Record major architecture decisions using ADRs with title, status, context, decision, alternatives, consequences and date.
- Preserve accepted decision history. Explicitly amend or supersede an ADR when its decision changes.
- Track assumptions, risks and unresolved questions. Do not silently turn a hypothesis into a requirement.
- Keep credentials, private user data and local environment files out of version control.

A glossary will be created as the charter and foundations introduce terms. Repository/release policy will be expanded before application implementation; the initial documentation baseline uses `main` and a descriptive `docs:` commit.
