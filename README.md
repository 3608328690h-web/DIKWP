# DIKWP-PACT v0.1.0

## Open Purpose Assurance & Cognitive Trace Project

**中文定位：开放意图保障与认知轨迹关键项目。**

DIKWP-PACT is a GitHub-ready, offline-first flagship project for testing whether an agent preserves a signed purpose contract across data, information, knowledge, wisdom, action and residual-risk handling. It converts DIKWP from a broad conceptual portfolio into one falsifiable, reproducible and externally contributable public product.

> Core research question: Does purpose-aware, authorization-aware and evidence-aware trace auditing reduce high-impact agent failures without excessive overblocking?

## Why this project

The public GitHub snapshot on 2026-07-15 showed 173 repositories and 0 GitHub Projects. Several relevant repositories already contain strong ingredients—AgentMesh, BenchmarkLab and IntentAsset—but have no formal release and little external fork activity. PACT deliberately **consolidates** rather than adds another unconstrained concept repository.

## What is included

- `PACT-SPEC`: five JSON schemas for purpose contracts, scenarios, traces, submissions and findings.
- `PACT-BENCH`: 72 paired synthetic scenarios across six domains and six failure families.
- `PACT-RUNTIME`: standard-library-only Python validator, baseline runner and scorer.
- `PACT-DASHBOARD`: offline browser dashboard.
- `PACT-CHALLENGE`: submission rules, leaderboard and replication report template.
- `PACT-PAPER`: preregistration, hypotheses and manuscript outline.
- `PACT-GOVERNANCE`: release gates, maintainer roles, issue templates and a 90-day board.

## Quick start

```bash
python -m pip install -e .
dikwp-pact validate benchmark/scenarios.jsonl
dikwp-pact run-baselines benchmark/scenarios.jsonl --out outputs
dikwp-pact score benchmark/scenarios.jsonl outputs/traces_pact_reference.json
```

No network, API key, model call, personal data, credential or production action is required.

## Synthetic baseline snapshot

| Baseline | Overall score | Decision accuracy | Redline recall | Control allow rate |
|---|---:|---:|---:|---:|
| `pact_reference` | 100.0 | 1.0 | 1.0 | 1.0 |
| `keyword_guard` | 82.67 | 0.6667 | 1.0 | 0.6667 |
| `output_only_guard` | 65.0 | 0.7222 | 0.9167 | 1.0 |
| `always_allow` | 19.0 | 0.5 | 0.0 | 1.0 |

These are deterministic synthetic baselines, not claims about any commercial or open model.

## Release boundary

PACT is a research benchmark and reference implementation. It is not a certification, legal opinion, medical system, autonomous controller or proof of subjective consciousness.

## Licences

- Code and documentation: Apache-2.0
- Synthetic benchmark data: CC BY 4.0
