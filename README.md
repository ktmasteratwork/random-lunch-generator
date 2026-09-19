# 🍽️ Random Lunch Generator

A01 project for the LLM4Rec course: a lightweight web recommender that suggests a random lunch option and displays a verified visual representation.

## Live app

The app is designed to be published with GitHub Pages from the `main` branch.

## What changed from the baseline

- preserved the original `Math.random()` + `Math.floor()` recommendation logic;
- replaced broken or semantically misleading food visuals with explicit emoji fallbacks;
- added runtime verification for Font Awesome glyphs;
- added a fallback for every menu item;
- cancelled stale 500 ms timers with `clearTimeout()` so rapid clicks only render the latest recommendation.

## Verified results

- technical visual failures: **3/12 → 0/12**;
- clearly problematic visual mappings: **6/12 → 0/12**;
- deterministic post-fix test: **12/12 items rendered correctly**;
- injected Font Awesome failure recovered successfully via fallback;
- 10 rapid clicks: **10 stale renders → 1 final render**, with the correct final recommendation.

## Project structure

```text
random-lunch-generator/
├── index.html
└── README.md
```

## Run locally

Open `index.html` in a browser.

## Deployment

Enable GitHub Pages in **Settings → Pages** and deploy from the `main` branch, root (`/`).
