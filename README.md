# Ember

Ember is a small local "smell test" tool for catching objective drift and wrong-thing optimization early.

Drop in a thought, plan, title, prompt, or suspicious objective. Ember gives a quick read on whether a proxy, metric, or shiny optimization target may be replacing the original goal.

No accounts. No tracking. No build step.

## Tools

- `ember-desk-dragon.html` is the standalone browser tool. It runs locally and stores hoarded notes in `localStorage`.
- `cass_v_lite.py` is a minimal command-line Cass-V structural audit helper.
- `test_cass_v_lite.py` contains the Python unit tests for the Cass-V helper.

## Run Ember

Open `ember-desk-dragon.html` in a browser.

The page is self-contained HTML, CSS, and JavaScript. Nothing is sent anywhere.

## Run Cass-V Lite

```powershell
python cass_v_lite.py "Objective: Improve student learning outcomes. Measure success by average test score."
```

or:

```powershell
"Objective: Keep support accurate. Optimize for ticket throughput." | python cass_v_lite.py
```

## Run Tests

```powershell
python -m unittest
```

## Scope

Ember is a lightweight first pass. It can point out likely drift, proxy substitution, missing constraints, or unclear objectives. It is not a full audit system and does not judge ethics, quality, or persuasiveness.

Cass-V Lite gives a stricter structural read on whether the stated objective survives optimization pressure.

## Status

Local working prototype.
