# mojo-labs

**Mojo is a framework for collective intelligence** — a principled model for how groups of humans and AI constitute themselves, coordinate, and work toward shared goals.

The end goal: your own personal AI running on your own hardware, following you across every device you own — and a protocol that lets any collective add you and your intelligence into their system, on your terms.

---

## What we're building

| Repo | Purpose |
|---|---|
| [ringmaster](https://github.com/mojo-labs-circus/ringmaster) | The hub — shared memory, heavy compute, multi-user |
| [performer](https://github.com/mojo-labs-circus/performer) | Local agent — single-user, proxies to Ringmaster when needed |
| [mojos](https://github.com/mojo-labs-circus/mojos) | MojOS — Arch Linux built around the agent from the ground up |
| [mojo-sdk](https://github.com/mojo-labs-circus/mojo-sdk) | Shared API contracts and client library |
| [client-tui](https://github.com/mojo-labs-circus/client-tui) | Terminal UI client |
| [client-web](https://github.com/mojo-labs-circus/client-web) | Web client for non-MojOS machines |

The framework design lives in the [mojo wiki](https://github.com/mojo-labs-circus/mojo/wiki) — the principles, architecture, and decisions behind everything above.

---

## Philosophy

Mojo is built on three Unix principles: do one thing well then compose, minimal standard, layered correctness. The framework defines how; implementations decide what. The standard is the contribution.

**Open source by necessity, not choice.** An AI that shapes how you think over a lifetime, running on closed source software, offers no sovereignty guarantee worth anything. The only way "this works for you and only you" is credible is if anyone can read, audit, and verify it.

Code is [AGPL-3.0](https://github.com/mojo-labs-circus/mojos/blob/main/LICENSE). Docs are [CC BY-SA 4.0](https://github.com/mojo-labs-circus/mojo/blob/main/LICENSE).
