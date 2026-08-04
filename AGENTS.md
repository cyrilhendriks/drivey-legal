# AGENTS.md — Drivie Legal & Support

Entry point for any coding agent working on this repository — Claude Code,
Kimi, Codex, Copilot Workspace, or a human.

Read **[`CLAUDE.md`](CLAUDE.md)** in full first (it's short — two pages of
context, no code). Written in Dutch, the project owner's working language.

## Operating notes

This repo is deliberately simple: two static HTML files, no build step, no
dependencies, no CI. GitHub Pages serves `main` directly — a push is live
within minutes with no review gate in between.

- **`index.html`'s legal text**: propose changes via a PR, per CLAUDE.md —
  this is the one place in the repo where "just push it" is explicitly
  discouraged, because a bad edit here goes live instantly and has real
  legal/App-Review consequences (it's the Privacy Policy URL and the basis
  for the Terms-of-Use link both apps and both app stores reference).
- **`support.html`**: lower stakes (contact form, FAQ, styling) — normal
  judgment applies.
- **No credentials of any kind live in or are needed for this repo.** The
  contact form talks to Web3Forms directly from the browser.
- **No simulator/emulator/API access is relevant here** — if a task
  touches this repo, it's plain HTML/CSS editing and nothing else.
- **This content is duplicated (not linked) inside both phone apps** — see
  CLAUDE.md's "Verband met de apps" section before changing the legal
  text's substance.
