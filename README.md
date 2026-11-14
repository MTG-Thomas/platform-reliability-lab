# Platform Reliability Lab

An evidence-based engineering curriculum for **SRE, observability, distributed systems, resilience engineering, platform engineering, and managed services**.

The goal is to understand why complex systems succeed or fail, investigate those claims in safe experiments, and translate lessons into reliable operational practices for MSPs. This is an evergreen learning project, not a certification checklist.

## Start here

- [Program charter and learning map](https://github.com/MTG-Thomas/platform-reliability-lab/issues/1)
- [Canonical reading shelf](https://github.com/MTG-Thomas/platform-reliability-lab/issues/10)
- [Courses and certification syllabi](https://github.com/MTG-Thomas/platform-reliability-lab/issues/9)
- [Managed services engineering](https://github.com/MTG-Thomas/platform-reliability-lab/issues/11)
- [Adversarial systems engineering](https://github.com/MTG-Thomas/platform-reliability-lab/issues/12)
- [External-provider reliability](https://github.com/MTG-Thomas/platform-reliability-lab/issues/13)
- [All investigations](https://github.com/MTG-Thomas/platform-reliability-lab/issues)

## Core learning modules

| Module | Investigation |
| --- | --- |
| SRE, service indicators and objectives | [#2](https://github.com/MTG-Thomas/platform-reliability-lab/issues/2) |
| Observability and control theory | [#3](https://github.com/MTG-Thomas/platform-reliability-lab/issues/3) |
| Incident analysis and resilience engineering | [#4](https://github.com/MTG-Thomas/platform-reliability-lab/issues/4) |
| Distributed systems and recovery | [#5](https://github.com/MTG-Thomas/platform-reliability-lab/issues/5) |
| Platform engineering and golden paths | [#6](https://github.com/MTG-Thomas/platform-reliability-lab/issues/6) |
| Queueing theory, toil, and reliability economics | [#7](https://github.com/MTG-Thomas/platform-reliability-lab/issues/7) |
| MSP reliability field guide (capstone) | [#8](https://github.com/MTG-Thomas/platform-reliability-lab/issues/8) |

## The standing rule

> **Every major architectural principle must be accompanied by its strongest credible counterargument, the conditions under which it fails, and an experiment capable of changing our minds.**

The skeptic must be steelmanned, not caricatured. State what would disprove the favored architecture before evaluating an experiment. Simplifying or rejecting the original solution counts as success when evidence supports it.

Read the [Adversarial Review Policy](docs/adversarial-review.md) and use the [investigation issue template](.github/ISSUE_TEMPLATE/investigation.yml).

## Method

**Theory → investigate → adversarial review → experiment → evidence → apply → reflect.**

Each investigation asks for a precise claim, the strongest opposing argument, a simpler option, failure conditions, precommitted evidence and reversal thresholds, and an operational consequence.

All public examples use fictional customers, synthetic data and sanitized architectures. No client identities, production topology, secrets, proprietary logs, or unauthorized failure injection. Tests must be performed in disposable or explicitly authorized environments.

## Contributing

Corrections, skeptical case studies, reading suggestions, negative results, and reproducible experiments are welcome. The curriculum should change when the evidence changes.
