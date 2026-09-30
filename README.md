# Test Cloud w SAP — Learner's Handbook

A step-by-step learner's guide for the UiPath Software Testing Training. Built with [MkDocs](https://www.mkdocs.org/) and the [Material theme](https://squidfunk.github.io/mkdocs-material/).

**Live site:** _add your GitHub Pages URL here after the first deploy_

## What's inside

One continuous training (no separate modules), covering: UiPath Test Cloud, getting started with Test Manager (including creating your own project), Agentic Testing with Autopilot for Testers, getting started in Studio, building an Object Repository of SAP GUI elements, connecting Studio to Test Manager, turning a manual test case into an automated one, data-driven testing, Orchestrator, and publishing and executing test cases.

## Known content gaps

- Some screenshots in Manual to Automated Test Case and Publishing Test Cases still show the earlier UiBank sample project.

## Running locally

```bash
pip install "mkdocs>=1.6,<2" "mkdocs-material>=9.7,<10"
mkdocs serve
```

Then open http://127.0.0.1:8000/.

## Deploying

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site and publishes it to the `gh-pages` branch. GitHub Pages is configured to serve from that branch.
