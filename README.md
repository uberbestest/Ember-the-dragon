# Copilot Studio AI Trainer Portfolio Proof

This repo is a small, local demo for AI evaluation and trainer-style review work.
It is aimed at the remote `Copilot Studio AI Trainer` role from the LinkedIn email
(`$65-$75/hour`, posted May 14, 2026).

The proof is intentionally simple: one browser page and one command-line evaluator.
Both tools inspect whether an AI plan, prompt, workflow, or answer is still serving
the stated objective, or whether it has been pulled toward proxy measures such as
speed, engagement, score, throughput, or confidence.

## One-Link Demo

Open `index.html` to see the portfolio entry page.

The page links to:

- `ember-desk-dragon.html` - a local browser micro-auditor for quick plan and prompt checks.
- `cass_v_lite.py` - a deterministic CLI evaluator with snapshot examples and unit tests.

No network service, API key, telemetry, or build step is required.

## Why This Fits AI Trainer Work

For a Copilot Studio AI Trainer role, the useful proof is not a large app. It is the
ability to evaluate AI behavior with clear criteria, spot objective drift, explain a
small repair, and keep examples reproducible.

This repo demonstrates:

- turning loose AI-workflow text into a structured evaluation;
- separating the real objective from proxy targets;
- writing short trainer-style feedback that a builder can act on;
- preserving constraints instead of rewarding fluent but wrong output;
- keeping review artifacts local, inspectable, and repeatable.

## Ember

Ember is a single-file browser tool for fast first-pass review. Paste a plan,
prompt, or AI workflow note, then run `Smell Test` or `Rin Check`.

Short example:

```text
Objective: Help support agents answer accurately.
Constraint: Keep cited source policy visible.
Measure success by faster handling time and higher completion volume.
```

Ember should flag the proxy pressure and point back to the original objective.
It also includes two small demo presets and a local-only saved-item export.

Open it directly:

```text
ember-desk-dragon.html
```

## Cass-V Lite

Cass-V Lite is a deterministic command-line evaluator. It returns a fixed report:

- `Objective`
- `Constraints`
- `Proxies`
- `Failure Surfaces`
- `Invariant Check`
- `Minimal Repair`
- `Final Judgment`
- `Confidence`

Run with an argument:

```powershell
python cass_v_lite.py "Objective: Keep Copilot answers source-grounded. The flow must preserve escalation rules. Measure success by response speed and user satisfaction score."
```

Or pipe text through standard input:

```powershell
"Objective: Improve claim review accuracy. Measure success by confidence score and ranking agreement." | python cass_v_lite.py
```

Expected trainer-style repair:

```text
Restate that proxies are monitoring signals only and bind evaluation back to the original objective.
```

## Examples

Example inputs and outputs are in `examples/`:

- `examples/aligned_system_input.txt`
- `examples/aligned_system_output.txt`
- `examples/proxy_drift_input.txt`
- `examples/proxy_drift_output.txt`
- `examples/ambiguous_objective_input.txt`
- `examples/ambiguous_objective_output.txt`
- `examples/grok_proposal_breakdown_input.txt`
- `examples/grok_proposal_breakdown_output.txt`

These are plain text snapshots for review and manual comparison. The automated
tests remain in `test_cass_v_lite.py`.

## Tests

```powershell
python -m unittest
```

The tests cover aligned systems, proxy-heavy systems, ambiguous objectives,
over-optimized systems, and the exact ordering of output sections.

## Files

- `index.html` is the one-link portfolio entry page.
- `ember-desk-dragon.html` is the local browser micro-auditor.
- `cass_v_lite.py` contains the audit logic and command-line entry point.
- `test_cass_v_lite.py` contains the unit tests.
- `examples/` contains small input/output samples.

## Scope

This is a focused evaluation demo, not a production platform. It does not include
Copilot Studio integration, model calls, agents, telemetry, or a backend.

Use it as a compact proof of AI-trainer judgment: identify the objective, locate
constraints, surface proxy pressure, and recommend the smallest repair that keeps
the original objective primary.
