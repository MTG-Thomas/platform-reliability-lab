# Adversarial Engineering Review Policy

> Every major architectural principle must be accompanied by its strongest credible counterargument, the conditions under which it fails, and an experiment capable of changing our minds.

## When it applies

All substantive architecture decisions, platform proposals, reliability interventions, investigations, reference designs, and capstone recommendations. This is a **decision gate**, not optional reading or theater.

## Required record

1. **Claim and scope:** What is proposed? Which workloads, tenancy assumptions, teams and service obligations are in scope?
2. **Strongest counterargument:** Present the informed skeptical view with credible sources. Do not fabricate balance or strawmen.
3. **Simpler alternative:** Consider deleting a component, a modular monolith, direct vendor integration, a script/runbook, or not doing the work.
4. **Failure conditions:** Identify scale, latency, cost, operational complexity, failure coupling, skill constraints, or provider limits that invalidate the proposal.
5. **Precommitted test:** State competing hypotheses, predicted outcomes, evidence, metrics, evaluation criteria and decision-reversal thresholds **before** running an experiment.
6. **Decision and uncertainty:** Record observations, limitations, remaining risks, accepted tradeoffs, and explicit circumstances that trigger reconsideration.

If an experiment is not feasible, identify what operational observation or incident would justify changing the decision.

## Example

**Claim:** An independent worker queue improves event-to-ticket reliability.

**Steelman:** It creates a new component and deployment boundary, can hide delayed failures, and can generate replay storms; a straightforward synchronous pipeline may be safer at small scale.

**Discriminating test:** In disposable environments, compare event correctness, p99 latency, recovery after downstream outage, backlog draining, operator steps, and monthly cost. Declare thresholds before testing.

**Decision:** Keep, simplify, or reject the queue according to measured results; record the result even when it contradicts the preferred architecture.

## Guardrails

- Only synthetic or appropriately sanitized public evidence; do not disclose customer IDs, secrets, customer tickets, proprietary topology or unredacted logs.
- No fault injection into production or customer systems without explicit separate authorization and an operational rollback plan.
- No post-hoc metrics, ungrounded certainty, cargo-cult best practices, reflexive anti-complexity, or assuming vendor certifications prove operating outcomes.
- A negative result is a **successful learning result**, not an experiment failure.

## Applied tracks

- [Adversarial systems engineering](https://github.com/MTG-Thomas/platform-reliability-lab/issues/12)
- [External-provider reliability without full control](https://github.com/MTG-Thomas/platform-reliability-lab/issues/13)
- [Charter](https://github.com/MTG-Thomas/platform-reliability-lab/issues/1)
