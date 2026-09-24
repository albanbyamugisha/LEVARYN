# LEVARYN documentation plan

Status: revised planning baseline · Date: 2026-09-24

## Purpose and background

Translate the long-term LEVARYN brief into an achievable documentation program before application implementation. LEVARYN may initially use existing model APIs or open-weight models. Building a frontier model is not a prerequisite.

The assistant is the user-facing product; the platform is its supporting application infrastructure; LEVARYN models are a future model-development ambition. Keep these boundaries explicit.

## Recommended approach

1. **Validate one audience and recurring problem.** A software engineering student assistant is a hypothesis, not an accepted target market. Compare proposed workflows with existing alternatives and define why someone would return.
2. **Separate learning from implementation prerequisites.** Teach tokens, context, inference, embeddings, tool calling, and evaluation before the features that need them. Schedule advanced training topics later.
3. **Use two documentation depths.** Specify prototype and MVP workflows, requirements, data, and acceptance criteria concretely. Give later capabilities short outlines, dependencies, risks, and adoption triggers.
4. **Define evaluation before model selection.** Assemble representative tasks, expected behavior, scoring criteria, and quality/latency/cost measures before comparing providers.
5. **Distinguish conversation history from memory.** Decide what users need saved before designing automatic persistent personalization. Require review, correction, deletion, and clear ownership.
6. **Pursue portability first.** Own application logic, data formats, evaluations, and integration boundaries. Justify self-hosting and training with measured capability, privacy, or economic needs.
7. **Use an implementation-readiness gate.** Resolve near-term blockers without requiring exhaustive designs for distant capabilities.
8. **Create documents progressively.** This structure is a coverage map, not a directive to create empty files or speculative infrastructure.

## Scope labels

| Label | Meaning |
| --- | --- |
| Prototype | Tests the core product and technical assumptions |
| MVP | Supports a small intended audience reliably |
| Production | Meets the operating, security, and reliability needs of actual users |
| Later scale | Requires demonstrated demand or operational constraints |
| Research | Exploratory, without a delivery commitment |

Production readiness does not imply a distributed architecture. Every proposed capability must have a scope label and reason for inclusion.

## Coverage map

Paths below are planned; create them only when their content is written.

| Area | Planned documents | Required coverage |
| --- | --- | --- |
| Product | `product/charter.md`, `users-and-use-cases.md`, `requirements.md`, `scope-and-success.md` | Vision, mission, philosophy, problem, audience, validation, value proposition, functional/non-functional requirements, constraints, non-goals, prototype/MVP boundaries, measurable success |
| Foundations | `foundations/ai-and-language-models.md`, `context-embeddings-and-retrieval.md`, `tools-agents-and-multimodality.md`, `evaluation-and-model-adaptation.md` | AI, ML, deep learning, neural networks, transformers, attention, tokens, embeddings, context windows, inference, training/pretraining, fine-tuning, instruction tuning, alignment, quantization, distillation, hallucinations, prompts, structured outputs, tools, agents, reasoning and multimodal models, open-weight versus proprietary models |
| System architecture | `architecture/system-overview.md` | Frontend/backend boundaries, authentication, user management, conversations, orchestration, gateway needs, caching, storage, search, background work, queues, notifications, analytics, billing readiness, security and deployment; distinguish logical components from separate services |
| AI engine | `architecture/ai-engine.md` | Provider abstraction and capability differences, routing, switching, prompts, context budgets, structured responses, tool selection, streaming, retries, fallbacks, cancellation, accounting, cost, latency, evaluation |
| Data | `architecture/data-model.md` | Ownership, lifecycle, relational/object/vector storage boundaries, constraints, ER diagrams; add entities only when current requirements justify them |
| Memory | `architecture/memory.md` | History, working/semantic/episodic memory, preferences, retrieval, summaries, relevance, expiration, correction, deletion, privacy and user controls |
| Knowledge | `architecture/retrieval-and-knowledge.md` | PDFs, documents, notes, websites and uploads; ingestion, parsing, cleaning, chunking, embedding, indexing, retrieval, reranking, context assembly, citations, source/version tracking, updates, deletion and evaluation |
| Tools and agents | `architecture/tools-and-agents.md` | Registry, schemas, permissions, sandboxing, web search, code/file/API operations, approval, bounded loops, planning, recovery and auditing; evidence needed for multi-agent complexity |
| Multimodal | `architecture/multimodal.md` | Text, images, audio, speech recognition/synthesis, vision, image generation, documents and video; integration boundaries and adoption triggers |
| Research | `research/technology-options.md`, `provider-and-model-options.md`, `cost-model.md` | Languages, frameworks, databases/vector search, caching, identity, object storage, models/serving, RAG/agent libraries, search, voice/images, containers, cloud, delivery, observability, testing and security; cost formulas and dated price sources |
| Interfaces | `interfaces/api-design.md`, `user-experience.md` | API conventions, auth, versioning, pagination, streams, errors, limits, idempotency, webhooks, SDK strategy; chat/history, Markdown/code, uploads, search, voice, settings, memory/model/tool controls, accessibility, mobile and failure states |
| Security | `security/threat-model.md`, `security-and-safety.md`, `privacy-and-data-governance.md` | Authn/authz, tenant isolation, encryption, secrets, validation, SQL injection, XSS, CSRF, SSRF, prompt/indirect injection, exfiltration, malicious uploads, tool abuse, sandboxing, rate limits, audit, dependencies/supply chain, consent, retention, deletion, provenance and rights |
| Quality | `quality/testing-strategy.md`, `ai-evaluation.md` | Unit, integration, API, end-to-end, security, load and regression tests; model/prompt/RAG/tool evaluations, nondeterminism, representative datasets and scoring |
| Operations | `operations/development-and-delivery.md`, `deployment-and-observability.md`, `recovery-and-incident-response.md` | Local/configuration environments, Git, Docker when justified, staging/production, CI/CD, migrations, secrets, logs/metrics/traces, backups, restore exercises, rollback, scaling, support and incident ownership |
| Roadmaps | `roadmap/documentation-roadmap.md`, `development-milestones.md`, `model-independence.md` | Writing sequence; research through production/platform milestones; external APIs → multiple providers → open weights → self-hosting → fine-tuning → specialized models → foundation-model research |
| Governance | `governance/documentation-conventions.md`, `repository-and-releases.md`, decision/assumption/risk/question registers, `adrs/` | Traceability, ADR lifecycle, branch/commit/PR conventions, issue templates, versioning, releases, licensing and compatibility management |

Root documentation will grow to include `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, and `CHANGELOG.md` when their policies are defined. Add `LICENSE` only after choosing the license. Keep architecture and API documentation under `docs/` rather than duplicate it at the repository root.

## Additional cross-cutting requirements

- Product validation against existing alternatives and repeat-use evidence.
- Data governance: ownership, licenses, consent, provider processing, and use in evaluation or training.
- Trust: communicate uncertainty and distinguish generated claims from tool results and cited evidence.
- Tenant isolation across storage, retrieval, caches, tools, and logs if serving multiple users.
- Accessibility, target languages, low-bandwidth operation, and interrupted connections.
- Operational ownership appropriate for a solo developer.
- Versioning and migration of prompts, models, embeddings, schemas, and API contracts.
- Provider deprecation, export and exit plans; test portability rather than merely claiming it.
- Requirements linked to decisions, milestones, and verification.

## Major decisions and timing

| Decision | Required before |
| --- | --- |
| Target audience, recurring problem and success measures | MVP scope and architecture |
| Local/private-hosted/multi-user deployment | Identity and ownership design |
| Data collection, consent, retention and provider processing | Persistent data handling |
| Component boundaries and background execution | Implementation planning |
| Languages and frameworks | Application implementation, following research |
| Provider contract and capability handling | AI-engine implementation |
| Persistence and retrieval approach | Storage implementation |
| Authentication and authorization | Multi-user release |
| Persistent memory and user controls | Personalization implementation |
| Tool authority and approvals | Tool enablement |
| Quality, reliability and spending targets | Prototype evaluation |
| Hosting, secrets, backup and rollback | Hosted release |
| License and release policy | Public distribution |

Compare alternatives by fit, advantages, disadvantages, complexity, cost, scalability, lock-in, evidence, and migration implications. Record major decisions in ADRs; do not silently replace them.

## Deliberately undecided

Exact vendors, model IDs, frameworks, databases, hosting, dedicated vector search, caching and queues; inclusion of RAG or memory in the MVP; orchestration frameworks; voice/image/video services; public APIs, billing, enterprise features and native mobile apps; self-hosting hardware, training methods, multi-region systems and distributed services.

Data ownership, privacy, permission boundaries, and a budget ceiling require early answers even while implementation technologies remain open.

## Overengineering guardrails

| Risk | Guardrail |
| --- | --- |
| Building a platform before proving utility | Evaluate one complete user workflow |
| Turning the capability list into MVP scope | Tie every included feature to a success criterion |
| Using agents for simple operations | Prefer explicit workflows until adaptive behavior has demonstrated value |
| Elaborate provider abstractions | Start with required capabilities and validate portability |
| Permanent memory by default | Separate history from deliberate user-controlled memory |
| Infrastructure for hypothetical traffic | Document measurable adoption triggers |
| Speculative tables and services | Require a current feature and lifecycle need |
| Training before evaluating existing models | Establish a measured capability, privacy or economic gap |
| Documentation without decisions | Tie each section to a decision, requirement, experiment or acceptance criterion |

## Next step

Write the charter one section at a time, then establish users/problem, prototype scope, success criteria, and constraints/budget. Do not begin application coding merely because the repository now exists.
