# ComponentLocator

**Click straight from your running app to your code.**

ComponentLocator is a Chrome extension (Manifest V3) for web developers: hold `Alt`/`Option` while hovering your app in development and the element under the cursor is highlighted with its component name and source file. `Alt+Click` opens that file in your editor at the exact line.

🌐 Website: **[fortunato.dev/ComponentLocator](https://fortunato.dev/component-locator)**
🛍️ Chrome Web Store:  **[ComponentLocator](https://chromewebstore.google.com/detail/cgjiahdnbpgbjcihgnkbeoamipcegolh?utm_source=item-share-cb)**

---

## What it does

- **Highlights components on hover** — component name, source path and line, plus the chain of parent components.
- **Opens your editor with one click** — VS Code, Cursor, Windsurf, JetBrains IDEs, or anything reachable via a URL scheme or your `EDITOR`/`REACT_EDITOR` variable.
- **Detects your framework automatically** — zero configuration:

| Framework | Support |
|---|---|
| **Next.js** | App Router & Pages Router, Webpack & Turbopack, React 18 & 19, Server Components (labeled with a `server` badge) |
| **React** (without Next.js) | Vite, Create React App and other dev setups |
| **Vue 2 & 3** | Component file out of the box; exact line/column with `vite-plugin-vue-inspector` or Vue DevTools |
| **Svelte 3/4/5** | Exact line/column for every element; SvelteKit included |
| **Astro** | `.astro` templates and framework islands |

## Why not LocatorJS?

Tools built on React's old `_debugSource` field stopped working with React 19 and the Next.js App Router. ComponentLocator reads React 19's new owner stacks (`_debugStack`) and resolves original source positions through the dev server's own source-map endpoints (Next.js) or the modules' inline source maps (Vite) — and uses each framework's native dev metadata for Vue, Svelte and Astro.

## Usage

1. Install the extension and run your app's dev server (`next dev`, `vite`, `npm run dev`…)
2. Open `http://localhost:<port>`
3. Hold `Alt` (Option on Mac) and hover — elements light up with their component info
4. `Alt+Click` to open the source file in your editor

> **Development only.** Production builds strip all debug info — there is nothing to locate. The extension runs exclusively on `localhost` / `127.0.0.1` and collects no data whatsoever.

## Settings (extension popup)

- **Enabled** — global on/off
- **Trigger key** — Alt (default), Ctrl, Shift, Cmd/Win
- **Open files with**:
  - *Dev server (auto-detect)* — recommended; uses your framework's launch-editor endpoint (Next.js, Vue CLI, Nuxt, CRA) and respects `REACT_EDITOR`/`EDITOR`
  - *Custom editor URL* — a template like `vscode://file{file}:{line}:{column}` (presets for VS Code, Cursor, Windsurf, JetBrains) plus your absolute project root for relative paths

## This repository

> **Note:** this repository does **not** host the extension's source code. It is the public home for feedback on ComponentLocator — bug reports, feature ideas, framework requests and discussions.

- 🐛 **[Report a bug](../../issues/new?template=bug_report.md)** — something broken, wrong file opened, no highlight
- 💡 **[Request a feature](../../issues/new?template=feature_request.md)** — new ideas, UX improvements
- 🧩 **[Request framework support](../../issues/new?template=framework_support.md)** — Preact, Solid, Qwik, Angular…
- 💬 **[Discussions](../../discussions)** — questions, setup help, show & tell

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening an issue — a good report with your framework and versions gets fixed much faster. Security concerns go through [SECURITY.md](SECURITY.md).

## Author

**[Fortunato De Angelis](https://fortunato.dev)** — [github.com/fortunato-deangelis](https://github.com/fortunato-deangelis)
