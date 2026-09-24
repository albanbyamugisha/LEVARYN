# Documentation roadmap

Status: revised planning baseline · Date: 2026-09-24

## Writing sequence

| Step | Focus | Exit criterion |
| --- | --- | --- |
| 1 | Charter | Vision, mission, problem, philosophy and assistant/platform/models boundaries are clear |
| 2 | Users and recurring problem | A first audience and workflow hypothesis has a validation method and comparison baseline |
| 3 | Prototype and MVP scope | Included features and non-goals are explicit; first workflow is bounded |
| 4 | Success criteria | Representative evaluation tasks and provisional quality, latency and cost criteria exist |
| 5 | Constraints and budget | Developer capacity, operating context, data boundaries, initial threats and spending ceiling are stated |
| 6 | Essential AI foundations and system flows | Concepts needed now are explained; request/data/permission/failure flows are understandable |
| 7 | Technology research and ADRs | Near-term choices have verified sources, alternatives, consequences and rationale |
| 8 | AI engine, data, API and UX | First-release contracts and behavior are consistent end to end |
| 9 | Memory, retrieval, tools and multimodality | Included capabilities have concrete designs; deferred capabilities have adoption triggers |
| 10 | Testing and operations | Evaluation, delivery, recovery, monitoring and detailed cost controls are specified |
| 11 | Repository policies and development milestones | Solo-developer deliverables have dependencies, tests and exit criteria |
| 12 | Independence roadmap and readiness review | Future stages are realistic and near-term blockers are resolved or explicitly deferred |

Foundations learning continues alongside design. Advanced model training does not block application planning. Revisit assumptions when research produces new evidence.

## Implementation-readiness gate

Before application coding begins, establish:

- An agreed user problem and bounded prototype with explicit non-goals.
- A primary end-to-end workflow, including failure and cancellation behavior.
- Initial data ownership, lifecycle, privacy, permission and threat designs.
- A spending ceiling and actionable controls for reaching it.
- Representative evaluation tasks and release acceptance criteria.
- Researched near-term technology decisions recorded in ADRs.
- A first implementation milestone with deliverables and meaningful verification.

Unresolved issues must be classified as blockers or documented deferrals. Detailed designs for distant capabilities are not required. Repository creation is preparation, not authorization to start application implementation.

## Later roadmap requirements

For each development milestone, record objectives, features, dependencies, deliverables, testing requirements and exit criteria. Use research → architecture → prototype → alpha → MVP → beta → production → platform expansion as a planning sequence, not a promise of dates.

For each model-independence stage, record knowledge, infrastructure, difficulty, benefits, risks, cost assumptions and adoption conditions. Training frontier-scale models must not be presented as a low-budget solo-developer activity.
