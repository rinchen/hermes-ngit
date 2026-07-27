# hermes-ngit

Hermes skill for decentralized Git over Nostr via [ngit](https://gitworkshop.dev/ngit).

## What is this?

A skill file for Hermes that provides instructions and workflows for working with
Nostr-based Git repositories. ngit is a sovereign, decentralized Git hosting protocol
built on Nostr — no central forge, no daemon required.

## Links

- **GitHub:** https://github.com/rinchen/hermes-ngit
- **Nostr:** published via `ngit init`; view on [gitworkshop.dev](https://gitworkshop.dev)
- **Radicle:** `rad:<rid>` (set after `rad init`)

## Features

- Announce repos to Nostr (`ngit init`) and keep gitworkshop current via `git push`
- Native `git clone` / `git push` against `nostr://` remotes (no daemon)
- Session repo detection for Nostr-enabled projects
- Commands for issues, PRs, and syncing
- Triple-push configuration (GitHub + Radicle + Nostr)

## Key Lesson

`ngit sync` only pushes git refs — it does **not** update the NIP-34 announcement that
gitworkshop.dev reads. To keep gitworkshop current, add the `nostr://` URL as an `origin`
pushurl so `git push` drives `git-remote-nostr` and re-announces HEAD automatically.

## Usage

Copy `SKILL.md` into your Hermes skills directory to enable ngit workflows.

## License

MIT
