# Support

Need help with ComponentLocator? Here's where to go:

## 📖 Start here

- The [README](README.md) — what the extension does, supported frameworks, settings, known limitations
- [fortunato.dev](https://fortunato.dev) — the author's website (a dedicated extension page is coming soon)

## 💬 Questions & setup help

Use **[GitHub Discussions](../../discussions)** for:

- "How do I make it open my editor X?"
- "Does it work with framework/bundler Y?"
- Setup and configuration help
- Sharing tips and workflows

## 🐛 Bugs & feature requests

Use **[Issues](../../issues)** with the appropriate template:

- [Bug report](../../issues/new?template=bug_report.md)
- [Feature request](../../issues/new?template=feature_request.md)
- [Framework support request](../../issues/new?template=framework_support.md)

## 🔒 Security

Never in public issues — see [SECURITY.md](SECURITY.md).

## Quick self-help checklist

Before asking, these solve most problems:

1. **Are you in dev mode?** The extension only works with a development server (`next dev`, `vite`, `npm run dev`…). Production builds contain no debug info.
2. **Is the app on `localhost`?** The extension deliberately runs only on `localhost` / `127.0.0.1`.
3. **Editor not opening?** Either set the `EDITOR` / `REACT_EDITOR` environment variable where your dev server runs (e.g. `code`), or switch to *Custom editor URL* in the extension popup and set your project root.
4. **Wrong or missing line numbers on Vue?** Without `vite-plugin-vue-inspector` (or Vue DevTools for Vite), Vue only exposes the component file — files open at line 1. Install the plugin for exact positions.
5. **Still stuck?** Run `__COMPONENT_LOCATOR_DEBUG__.inspect($0)` in DevTools with the element selected — the output tells you (and us) what the extension sees.
