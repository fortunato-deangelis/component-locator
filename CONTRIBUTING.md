# Contributing to ComponentLocator

Thanks for taking the time to help make ComponentLocator better! This repository collects bug reports, feature ideas and discussions about the extension.

> **Heads up:** the extension's source code is **not** hosted in this repository. Contributions here are reports, ideas and documentation — that's exactly what shapes the next releases.

## Ways to contribute

### 🐛 Report a bug

Use the **[Bug report](../../issues/new?template=bug_report.md)** template. The single most useful thing you can include is your **framework + versions**, because the extension behaves differently per framework:

- Framework and version (e.g. Next.js 16.1, Vue 3.5, Svelte 5, Astro 5)
- Bundler / dev server (Webpack, Turbopack, Vite, Vue CLI, CRA)
- React version if applicable (18 vs 19 changes the source-location strategy)
- Browser and extension version (shown in the popup)
- What you expected vs what happened (wrong file? wrong line? no highlight at all? editor didn't open?)

**Debug tip:** with the page open, run `__COMPONENT_LOCATOR_DEBUG__.inspect($0)` in DevTools (with the element selected in the Elements panel) and paste the output in the issue — it shows exactly what the extension sees.

### 💡 Suggest a feature

Use the **[Feature request](../../issues/new?template=feature_request.md)** template. Describe the problem you're trying to solve, not only the solution — there may be a simpler way to get you there.

### 🧩 Ask for a new framework

Use the **[Framework support](../../issues/new?template=framework_support.md)** template. If you know how the framework exposes source info in dev mode (a DOM property, an attribute, a dev-server endpoint), mention it — that's most of the work.

### 💬 Everything else

Questions, setup help, editor configuration, "is this possible?" — please use **[Discussions](../../discussions)** instead of issues, so issues stay actionable.

## Before opening an issue

1. **Search existing issues** (including closed ones) — your problem may already be tracked or fixed.
2. **Try the latest version** of the extension.
3. **Confirm you're in development mode** — production builds contain no debug info, so the extension has nothing to locate. This is by design, not a bug.
4. Check the known limitations in the README (e.g. Vue without an inspector plugin opens files at line 1).

## Pull requests

Since this repository only hosts documentation, pull requests are welcome for:

- Fixing typos or improving the docs (README, guides, templates)
- Improving the issue templates themselves
- Adding troubleshooting tips that helped you

For code contributions to the extension itself: open a **feature request or framework support issue first** — if it makes sense, we'll figure out together how to get your contribution in.

## Code of Conduct

By participating you agree to our [Code of Conduct](CODE_OF_CONDUCT.md). Be kind.
