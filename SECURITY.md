# Security Policy

## Scope

ComponentLocator is deliberately built with a minimal attack surface:

- Runs **only** on `localhost` / `127.0.0.1` / `0.0.0.0` — never on public websites
- Requires a single permission: `storage` (to sync your preferences)
- Collects **no data**, makes no requests outside your own dev server, ships no remote code
- Only meaningful in development mode — production builds contain no debug info

That said, security issues are still possible (e.g. in how the page-world scripts handle untrusted page content), and we take them seriously.

## Reporting a vulnerability

**Please do not open a public issue for security vulnerabilities.**

Instead, report privately via one of:

- **GitHub private vulnerability reporting** — use the *"Report a vulnerability"* button in this repository's Security tab (preferred)
- The contact form on [fortunato.dev](https://fortunato.dev)

Include:

- A description of the vulnerability and its impact
- Steps to reproduce (a minimal PoC page/app is ideal)
- Affected extension version (shown in the popup)

## What to expect

- An acknowledgment within **7 days**
- A fix or mitigation plan communicated within **30 days** for confirmed issues
- Credit in the release notes, if you'd like it

## Supported versions

Only the **latest published version** on the Chrome Web Store receives security fixes. Older versions are not maintained — Chrome auto-updates extensions, so this affects very few users.
