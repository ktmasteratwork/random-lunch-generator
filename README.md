# 🍽️ Random Lunch Generator

A01 project for the LLM4Rec course: a lightweight web recommender that suggests a random lunch option and displays a verified visual representation.

## Live demo

- **GitHub Pages:** https://ktmasteratwork.github.io/random-lunch-generator/
- **Source code:** https://github.com/ktmasteratwork/random-lunch-generator

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

The application is deployed with GitHub Pages from the `main` branch and is available over HTTPS at:

https://ktmasteratwork.github.io/random-lunch-generator/
