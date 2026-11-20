# Ruflo S3* post-task independent artifact audit — AI constructor contract

**Target transition:** S3*=— -> S3*=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

[issue.md](issue.md) (Human) · [roadmap.md](roadmap.md) (canonical authoritative six-function vector). **PLAN_ONLY / HYPOTHETICAL**, NOT IMPLEMENTED.

## System boundary and evidence

Original `ruvnet/ruflo@3c2ae9117091675878a1b52998c382570902ae39`. Historical [included Index](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ru/ruflo.md) is `S3*=—` but not evidence that a new feature is required. Current main [`UnifiedSwarmCoordinator`](https://github.com/ruvnet/ruflo/blob/3c2ae9117091675878a1b52998c382570902ae39/v3/%40claude-flow/swarm/src/unified-coordinator.ts) processes `task_complete` from a worker and marks its reported result completed without a complementary external artifact inspection in that method. Internal team/test/security checks are not automatically separate S3*. Owner grants ordinary coordinator actions; developer/deployer retains S5 and credential authority. The proposed auditor must be independent for the *specific completion claim*, not merely another self-critic controlled by the same agent.

## Track A — what can be reused, but is not equivalent

- Native coordinator: message bus, status, retry and re-assignment are useful legitimate S3 enforcement channels.
- [Issue #1309](https://github.com/ruvnet/ruflo/issues/1309): Ed25519 action-receipt proposal tracks provenance, not independent test oracle or factual correctness.
- [PR #3296](https://github.com/ruvnet/ruflo/pull/3296), OPEN: independently verifiable opt-in federation-fixture worker results and separate signed identities; may supply verifier concepts but not demonstrated same normal swarm task consumer/hold path on main.
- [PR #4477](https://github.com/ruvnet/ruflo/pull/4477), OPEN: independent grading of controlled managed-learning / provider-effect experiment, not a shipped normal swarm audit loop.
- Original [#3191](https://github.com/ruvnet/ruflo/issues/3191) concerns pre-action feasibility, not post-action artifact truth. Its old negative OpenSiro assessment is retained as a different scoped evaluation.

## Track B — minimal composable S3* constructor and authority

1. **Authorized selection:** developer chooses task types/sampling budget and a verifier identity with read-only access to real work outputs; no implicit privilege upgrade. Stamp task ID, runner/worker ID, output digest and audit policy version.
2. **Independent access:** on selected completion, capture immutable file diff/test output or constrained replay fixture from storage separate from producer-generated summary. A signature on the producer's own text is *insufficient* evidence.
3. **Independent judgment:** auditor has separate credential/evidence ownership and produces `PASS | FAIL | UNKNOWN` with raw evidence digest, bounds, reason and reproducible verifier version. It cannot rewrite the producer artifact or self-authorize tool effects.
4. **Legitimate correction:** coordinator records a pending-audit state before selected completion acceptance, rejects stale/duplicate worker completion, routes FAIL/UNKNOWN to authorized `HOLD / REWORK / ESCALATE` decision, and enforces bounded retries or owner escalation; on rework new artifact must be audited again.
5. **Return and revocation:** later result re-observed after corrective action, positive audited acceptance committed, audit timeout and authority denial kept as UNKNOWN rather than PASS. Disabled mode retains original completion semantics.

This requires explicit **S3* separate evidence owner and corrective closure**, not an extra in-path test stage. The production contract, true task-state state machine, auth policy and native integration tests must determine real method names and count. No implementation claims here.

## Native acceptance (unrun)

**Positive:** real correct code+test artifact gets separately checked and accepted; real failure gets FAILED judgment and bounded corrective re-audit. **Adversarial:** lying worker `task_complete` with valid signed summary but failing raw artifact must not be accepted. **Authority:** unavailable auditor, revoked read capability, unauthorized artifact path, parent denial, stale revision and timeouts must not auto-pass. **Races:** late duplicate complete, concurrent task cancel, worker re-assignment and audit re-run must not bypass pending state. **Compatibility:** unaudited task path remains unchanged. Baseline: ordinary native test/inline review alone under same tasks, models, budget and latency, then independent auditor; report false-hold and true defect detection without assuming cost savings.

**Falsifier:** original current main demonstrably already ships an equivalent independent real-artifact verifier with a distinct decision owner, binding ordinary task acceptance/rework and re-observation; or available rights do not permit independent evidence plus lawful control of completion state. Open PRs require new head/diff review if implementation begins.

## Decision and historical attribution

Proposal-stage **GO / NEEDS_EVIDENCE** for `S3*=— -> S3*=C`, not shipped C, not grade change, not user-value claim. [Old feasibility case](https://github.com/opensiro-contributions/ruflo/blob/cdf3e021c87f9f971661728253213f7343b91d75/.opensiro/issues/feasibility-review-20261118/roadmap.md) remains **NO_GO** for distinct **pre-action** contradiction/feasibility; do not overwrite it with this **post-action** scope. External Issue and public fork Issue **DRAFT — NOT PUBLISHED**; native tests **NOT_RUN**, cost **NOT_MEASURED**.