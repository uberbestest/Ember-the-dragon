# Ember

Ember is a small local "smell test" tool for catching objective drift and wrong-thing optimization early.

Drop in a thought, plan, title, prompt, or suspicious objective. Ember gives a quick read on whether a proxy, metric, or shiny optimization target may be replacing the original goal.

No accounts. No tracking. No build step.

## Files

- `ember-desk-dragon.html` is the standalone browser tool. It runs locally and stores hoarded notes in `localStorage`.
- `index.html` is a small launcher for static hosting.

## Run

Open `ember-desk-dragon.html` in a browser.

The page is self-contained HTML, CSS, and JavaScript. Nothing is sent anywhere.

## Scope

Ember is a lightweight first pass. It can point out likely drift, proxy substitution, missing constraints, or unclear objectives. It is not a full audit system and does not judge ethics, quality, or persuasiveness.

## Status

Local working prototype.
