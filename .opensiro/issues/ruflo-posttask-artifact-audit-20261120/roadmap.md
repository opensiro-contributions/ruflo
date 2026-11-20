# Ruflo — independent post-task artifact S3* constructor (Upstream #58 Wave 4)

- Receipt contract: proposal-gate
- Original repository: ruvnet/ruflo
- Original HEAD: 3c2ae9117091675878a1b52998c382570902ae39
- Observed at: 2026-11-20
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ru/ruflo.md
- Accepted assessment blob SHA: 4bb0859754b58e8f994e056f11cec1cdf0d33ddd
- Accepted review ref: 2602b642d92234c710ffbe96bfb33007d481ceab
- Accepted reviewed at: 2026-09-17
- Accepted Index commit: c2e43bf4750841277b3e58d8ba80314121734764
- Current Index main observed: 8f436270813b844aafc16917d69bc09661ef1544
- Accepted Profile version: 0.2.2
- Accepted Skills methodology version: 0.3.1
- Current Profile read: 0.2.4
- Published Upstream protocol: v0.18.0 at 28ea2cce06b517bc4550dceddb00210b1e0dc85c
- Accepted VSM vector: S1=A · S2=C · S3=C · S3*=— · S4=— · S5=—
- System in focus: First-party Ruflo ordinary swarm coordinator and agent task completion path; parent host/developer and original maintainer governance outside its autonomous policy ownership
- Matching working fork: opensiro-contributions/ruflo
- Fork owner control: ACTIVE/ALLOW confirmed on opensiro/meta before research and again before persistence
- Repository-wide source map: README.md, v3/@claude-flow/swarm/src/unified-coordinator.ts, v3/@claude-flow/swarm/src/consensus, v3/@claude-flow/security/src, v3/@claude-flow/memory/src, plugins/ruflo-metaharness, tests, original issues and open pull requests
- Evaluation object: Optional independent raw-artifact audit of ordinary swarm task outcomes after a worker reports completion, with binding correction and re-audit under developer authority
- Existing-work overlap: Coordinator trusts task_complete payload to mark completed; Issue #1309 proposes signed action receipts, open PR #3296 separately verifies opt-in federation fixtures, open PR #4477 grades managed-learning/provider effects; neither open PR is shipped main or proven equivalent whole-swarm audit
- Our on-top contribution: Developer-composable separate verifier and evidence path over pinned real output artifact/fixture, independent PASS/FAIL/UNKNOWN, auditable hold and rework into coordinator, and return-to-task re-audit without delegating parent policy
- Incremental benefit: Potential to catch a worker's inaccurate completion claim against actual raw artifacts; hypothetical outcome and performance savings not observed
- Decision scope: Proposal-stage S3* constructibility at ordinary swarm task-finalization boundary only; original maintainer alone decides adoption
- Priority rationale: S1=A and S2/S3=C already have supported owners; this separate S3* access and corrective return path is not established on inspected main; S4 external prospect and S5 parent policy do not become feature mandates
- Target transition: S3*=— -> S3*=C
- P1 dependencies: Prove lawful independent verifier identity/read scope, immutable output snapshot, audit authority binding, task-state race safety, and source-native positive/negative tests; research S4 only separately
- P2 optional: NONE
- Proposed C construction: Opt-in sample or explicit-task audit with separate evidence-grounded verifier, bounded artifact replay, recorded PASS/FAIL/UNKNOWN, selected-task acceptance held until verdict, return-to-S3 rework or escalation, re-audit after correction, revokeable parent config and unaudited compatibility
- C sufficiency falsifier: A shipped and enabled same-boundary independent raw-artifact verifier with separate judgment, binding hold/rework and re-observation already exists; or producer-controlled evidence, missing lawful owner, or task-state race prevents the proposed closure
- Scenario basis: HYPOTHETICAL
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Proposed validation: Matched correct and fabricated worker completion on real file/test artifact, stale or swapped artifact, absent audit identity, denied read, owner opt-out, verdict timeout, late duplicate completion, bounded retries, and re-audit feedback; contrast inline CI and self-review
- Validation state: NOT_RUN
- Proposal falsifier: The independent actor cannot access actual output separately from the claiming worker or its verdict cannot lawfully change later accepted state, or original main proves an equivalent complete S3* chain
- Result: NEEDS_EVIDENCE
- External issue: DRAFT — NOT PUBLISHED
- Public fork Issue: DRAFT — NOT PUBLISHED
- Cost status: NOT_MEASURED
- S1 disposition: Current agent/Claude/Codex task and tool execution exists; no S1 C construction priority
- S2 disposition: Topology, dependency and domain dispatch/consensus are current composable coordination; not an independent audit
- S3 disposition: Unified coordinator handles assignment, status, retries, task failure and health; it supplies a potential enforcement integration but does not independently decide audit truth
- S3* disposition: Worker task_complete immediately becomes completed in inspected coordinator code; propose separate raw-artifact verification and binding feedback, not just logs, signatures, or ordinary QA
- S4 disposition: Memory, SONA and Dream Cycle are mainly retrospective/internal or maintainer processes; no assumed runtime outside-and-then closure
- S5 disposition: Original maintainer/deployer sets legitimate ultimate policy; proposed optional audit cannot grant or rewrite that authority

## Identity and pins

Accepted canonical [Index assessment](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ru/ruflo.md) has exact `included` review pin `2602b642d92234c710ffbe96bfb33007d481ceab`, source blob `4bb0859754b58e8f994e056f11cec1cdf0d33ddd`, historical Profile 0.2.2 and Methodology 0.3.1. Current original [main@3c2ae911](https://github.com/ruvnet/ruflo/commit/3c2ae9117091675878a1b52998c382570902ae39) is separate. The fixed historical vector is not changed or regraded. Current published Upstream [v0.18.0](https://github.com/opensiro/upstream/commit/28ea2cce06b517bc4550dceddb00210b1e0dc85c) applies its assessment-neutral constructor gate. Source-only [first-pass seal](https://github.com/opensiro/upstream/issues/58#issuecomment-7043548273) was posted before inspecting the historical case.

## Rights and authority

The verified `opensiro-contributions/ruflo` fork has parent `ruvnet/ruflo`, original MIT license, and owner control `ACTIVE/ALLOW`; this authorizes internal fork metadata, **not** a third-party Issue/PR or public fork GitHub Issue. A developer/deployer must opt in and supply/verifiably authorize the separate auditor identity and read-only artifact access. Coordinator may enforce the outcome only within that authorization. The upstream maintainer owns whether any design is desirable; a `GO` here cannot compel adoption, grant audit permissions, or replace a future Index assessment.

## Existing work / overlap

**Track A, shipped:** [`UnifiedSwarmCoordinator.handleTaskComplete`](https://github.com/ruvnet/ruflo/blob/3c2ae9117091675878a1b52998c382570902ae39/v3/%40claude-flow/swarm/src/unified-coordinator.ts) accepts a worker `task_complete` message, writes `task.status='completed'` and `task.output=data.result`, increments task metric, emits `task.completed`, and releases capacity. This is current-state regulation, not an independently sourced audit of what was actually changed or tested. [Ruflo README](https://github.com/ruvnet/ruflo/blob/3c2ae9117091675878a1b52998c382570902ae39/README.md) documents normal agent task execution. Consensus and coordinator health regulate the swarm; routine tests and `plugins/ruflo-metaharness` audit commands provide related machinery, not proof of ordinary run's separate audit owner/return path.

**Track A, original community work:** [Issue #1309](https://github.com/ruvnet/ruflo/issues/1309) proposes cryptographic chain of action receipts (provenance not factual correctness), [open PR #3296](https://github.com/ruvnet/ruflo/pull/3296) has distinct identities and independent verification for an *opt-in federation benchmark fixture* but is not merged or shown on the ordinary completion path, and [open PR #4477](https://github.com/ruvnet/ruflo/pull/4477) independently grades a *managed provider/learning experiment*, not normal swarm task acceptance. [Original Issue #3191](https://github.com/ruvnet/ruflo/issues/3191) proposes an **earlier, distinct** pre-action feasibility receipt; RuV reproduction is expressly pending. Open work may provide reusable ports, so inspect current heads again before implementation. These source facts neither veto nor certify this proposal.

## Function ownership

- **S1 / historical A:** operational coding/tool agents and worker result loop, NO_TARGET for a new C constructor.
- **S2 / historical C:** supported dependency, domain and topology coordination plus consensus, NO_TARGET.
- **S3 / historical C:** coordinator's current task/health/retry management, NO_TARGET; an auditing decision is not the same role.
- **S3* / historical —:** inspected normal task completion trusts the producer report and lacks proven separately owned raw-artifact challenge with binding corrective return. **P0** is proposed optional `S3*=C` by independent outcome evidence → judgment → coordinator hold/rework → later re-audit.
- **S4 / historical —:** internal learning/memory and maintainer Dream Cycle are insufficient for externally prospective adaptation at this boundary; **DEFER**, not an inferred product deficit.
- **S5 / historical —:** parent user/deployer and maintainer retain ultimate authority; **NO_TARGET**. Static policy is not autonomously owned S5.

## Parallel contribution-on-top review

| Candidate | Track A source facts and native alternative | Track B complete minimal on-top C path | Refutation |
| --- | --- | --- | --- |
| **P0 S3* independent outcome audit** | Coordinator consumes worker `task_complete` as completed; signatures, ordinary tests and in-path reviewer are cheaper but do not independently check claim against separately accessed raw artifact. Open federation and managed-learning PRs have different scope. | Explicit opt-in selects eligible tasks and authorized independent read-only checker; freeze actual output snapshot and task contract; independently replay/check changed files/tests/outputs; record verdict PASS/FAIL/UNKNOWN; prevent acceptance on selected task until completed check; on FAIL/UNKNOWN return to S3 for authorized HOLD/REWORK/ESCALATE; reobserve corrected artifact before accepting. Baseline no-audit semantics preserved. | If same-boundary native first-party independent evidence and corrective closure already exist, or separate identity/evidence/hold cannot be made lawful and race-safe, then no claimed C. |
| S4 prospective external adaptation | Internal SONA and Dream Cycle are not a sufficient outside-then decision | Requires a separately evidenced external source/forecast/trial/current-control loop | No actual external distinction/adaptation path; no present target |
| S5 policy | User/operator controls permissions and policy; RVM remains a separate authority boundary | None; no parent authority transfer | A proposed policy owner lacks legitimate identity-level mandate |

## Capability priority

**P0:** proposed `S3*=— -> S3*=C` (**GO**, **NEEDS_EVIDENCE**, PLAN_ONLY). **P1:** validate independent identity/evidence and current-coordinator race safe binding; explore S4 only if independently warranted. **P2:** NONE. Neither P0 nor its hypothetically possible benefit is required by original product management.

## Implementation options

An optional first-party `auditTaskCompletion` extension could be composed with a coordinator adapter around the current completion path. Its *logical* ports are trusted task+policy snapshot, independently read artifact/test-output accessor, verifier identity and decision, authorized task-hold and corrective response, and re-audit observation. Physical API names and number of ports must derive from actual tests and runtime integrations, not a generic template. Preserve existing task state when disabled. Verify duplicate and stale worker reports cannot evade or overwrite `HOLD`; the current synchronous completion path cannot merely add a post-hoc log and claim S3*. No real code was changed.

## Specification and domain alternatives

The [historical same-fork NO_GO receipt](https://github.com/opensiro-contributions/ruflo/blob/cdf3e021c87f9f971661728253213f7343b91d75/.opensiro/issues/feasibility-review-20261118/roadmap.md) evaluated **Issue #3191 pre-action feasibility** of contradictory/infeasible actions, requiring RuV reproduction and bounded RVM authority. Its NO_GO and earlier evidence **remain intact**. The new first pass identified a **different evaluation object** (post-operation, separately observed artifact correctness). Therefore it receives a new case ID instead of rewriting old NO_GO as a changed decision on the same object. Native #3191 may still be worth researching; no Profile/Skills semantics change is required. Contributor suggestions are optional; original maintainers decide product adoption.

## Cost experiment

**NOT_RUN / NOT_MEASURED.** Native acceptance to design and run later: accurate worker summary with real passing artifact; fabricated `task_complete` with failing artifact; independently checked patch+test under changed snapshot; stale/symlink-swap artifact; absent or revoked auditor rights; rejection when parent policy forbids read; audit timeout; duplicate completion race; audit FAIL → authorized correction → re-audit PASS; audit UNKNOWN → fail-closed selected-task status; unselected task compatibility; matched inline CI-only and self-review alternatives. Measure correctness, false holds, latency, tokens, user/operator cost and maintenance effort separately. No savings/benefit or independent `C` implementation is claimed.

## Delivery and publication

Human [issue.md](issue.md) and technical [constructor-sufficiency.md](constructor-sufficiency.md) derive the same `GO / NEEDS_EVIDENCE` and target. Historical older [pre-action NO_GO case](https://github.com/opensiro-contributions/ruflo/blob/cdf3e021c87f9f971661728253213f7343b91d75/.opensiro/issues/feasibility-review-20261118/roadmap.md) remains unchanged. Internal metadata receipt only; public fork GitHub Issue and original-source communication **DRAFT — NOT PUBLISHED**, no product change, tests **NOT_RUN**, original and Index grades unchanged.