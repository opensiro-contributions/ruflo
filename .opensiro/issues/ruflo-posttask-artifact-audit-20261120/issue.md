# Ruflo — optional independent post-task artifact audit (Human draft)

**Target transition:** S3*=— -> S3*=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

Canonical [roadmap.md](roadmap.md) · technical [constructor-sufficiency.md](constructor-sufficiency.md). **Internal fork-local plan only; public Issue NOT PUBLISHED.**

## Source-backed current state

Historical [accepted included Index](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ru/ruflo.md), dated 2026-09-17, Profile 0.2.2 / Skills 0.3.1, blob `4bb0859754b58e8f994e056f11cec1cdf0d33ddd`; latest studied original [3c2ae911](https://github.com/ruvnet/ruflo/commit/3c2ae9117091675878a1b52998c382570902ae39). This is not a current Index regrade.

| Function / role | Historical Index state | Current source and decisive owner | Candidate / priority |
| --- | --- | --- | --- |
| **S1 · Operations** | A | Claude/Codex workers and the task/tool execution loop | NO_TARGET |
| **S2 · Coordination** | C | Domain queues, dependencies, topology and consensus under configured owners | NO_TARGET |
| **S3 · Inside-and-now** | C | UnifiedSwarmCoordinator assigns, retries and handles current task status and health | NO_TARGET |
| **S3* · Complementary audit** | — | Task completion currently trusts worker result; no proven separate raw artifact challenge/re-audit on normal path | **P0 → optional S3*=C** |
| **S4 · Outside-and-then** | — | Memory/SONA internal learning and maintainer Dream Cycle do not alone close prospective environment sensing | DEFER |
| **S5 · Policy and identity** | — | Human/deployer retains ultimate permission and policy choices | NO_TARGET |

## Operator question and answer

Ruflo's [current coordinator](https://github.com/ruvnet/ruflo/blob/3c2ae9117091675878a1b52998c382570902ae39/v3/%40claude-flow/swarm/src/unified-coordinator.ts) marks a worker task complete from the worker's reported result. Could a **separately authorized auditor** read the actual resulting code/test artifact, challenge the completion claim, and return a binding `HOLD/REWORK/re-audit` signal to current coordination? This is a plausible and source-located **S3* construction hypothesis**, not a diagnosed user incident or a request to force a new product feature.

**Track A:** existing swarm tests, logs, security/consensus, [action-receipt Issue #1309](https://github.com/ruvnet/ruflo/issues/1309) and **open** [federation verifier PR #3296](https://github.com/ruvnet/ruflo/pull/3296) help but do not prove an ordinary-task independent audit with corrective closure on main. **Track B:** opt-in separate read-only verifier, pinned raw artifacts, independent verdict, parent-authorized hold/rework, and subsequent re-audit. A cheaper deterministic test or self-review may suffice in many actual deployments and should be compared, not dismissed.

**Decision: GO / NEEDS_EVIDENCE (proposal-stage only).** The maintainer decides whether to build it. Native tests and costs **NOT_RUN / NOT_MEASURED**. No source product patch, new Index C, or third-party publication.

## Historical comparison and next permitted action

The existing [feasibility-review-20261118](https://github.com/opensiro-contributions/ruflo/blob/cdf3e021c87f9f971661728253213f7343b91d75/.opensiro/issues/feasibility-review-20261118/roadmap.md) says **NO_GO** about a *different* native [#3191 pre-action feasibility gate](https://github.com/ruvnet/ruflo/issues/3191). Its evidence remains unchanged: this new post-task audit is **not a reversal** of that separate verdict. The immediate next step, if authorized for implementation later, is to test actual worker result vs raw artifact, separate identity and correction/feedback under matching baseline. Public original/fork Issue publication requires distinct exact approval.