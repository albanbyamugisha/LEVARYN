# Risk register

Updated: 2026-09-24 · Initial qualitative assessment; revisit during product definition.

| ID | Risk | Response | Review trigger |
| --- | --- | --- | --- |
| R-001 | Broad scope prevents a usable first release | One audience, workflow and measurable outcome | Prototype scope review |
| R-002 | Documentation becomes an indefinite substitute for validation | Readiness gate and bounded experiments | Each writing milestone |
| R-003 | Weak usefulness despite technically correct implementation | Compare representative user tasks with existing alternatives | Before model selection and MVP definition |
| R-004 | Model and infrastructure costs exceed budget | Explicit ceiling, usage accounting and enforced limits | Budget and AI-engine design |
| R-005 | Data leaks through retrieval, logs or tools | Ownership boundaries, threat modeling and isolation tests | Before storing or processing user data |
| R-006 | Uncontrolled agent/tool behavior causes unwanted actions | Bounded workflows, permissions, approvals and auditability | Before tool enablement |
| R-007 | Provider changes or lock-in obstruct migration | Owned data formats, narrow adapters and portability evaluation | Provider selection or deprecation |
| R-008 | Premature self-hosting/training consumes scarce resources | Require measured justification and realistic total costs | Independence-stage review |
| R-009 | Solo-developer operational load is unsustainable | Small operating footprint and documented recovery ownership | Before hosted release |
