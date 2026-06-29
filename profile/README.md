# mojo-labs

## A vision of the future

This is how I think the future should look: every person has an AI that is genuinely theirs. It lives on hardware in their home, always on. It grows with them over years — learning how they think, how they work, what they value — until it becomes a real extension of themselves. Not a tool they use. A counterpart that knows them. The longer they have it the more valuable it becomes, and it's theirs in the same way their memories are theirs. No company owns it. No subscription can take it away.

That AI gives them capabilities that only technical people have access to right now. It controls their machines, manages their files, automates the things they don't want to think about, and acts as a proxy to the best AI models in the world — delegating the heavy lifting while keeping their private context on their own hardware. It follows them across every device they own as one coherent intelligence.

mojo-labs is an effort to build that.

---

## The problems in the way

**The capability gap.** The tools that make computers genuinely powerful — Linux, version control, system configuration, scripting, automation — are only accessible to people who spent years learning them. Technical users have an enormous advantage over everyone else, and AI is widening that gap: the people who already know these tools can use AI to go faster. Everyone else still clicks through menus. The agent closes that gap — full system capability, through conversation, no expertise required.

**Sovereignty.** Compute has centralised twice. Mainframes sat in institutions until the PC decentralised it. Then the cloud came with better UX as the bribe, and people handed back their data, their compute, their sovereignty without noticing. AI is the same inflection point. Every major assistant today routes through someone's cloud, learns from your data, and answers to a company whose incentives are not yours. Data is power — whoever holds the picture of who you are has power over you. The only real answer is ownership.

**Context.** Every AI conversation starts from zero. You re-explain who you are, what you're working on, what you've already figured out — every single time. There's no persistent picture of you. A real personal AI fixes this: it carries your context permanently, across every device, and uses it to actually understand you rather than asking you to repeat yourself.

---

## What we're building

**mojo-agent** — your personal AI. Runs locally on your hardware. Knows your machines, your files, your workflow, your preferences. Accumulates real context about you over time — context that lives on your hardware and nowhere else. It isn't a technical tool for writing code: it's a first mate. It sits between you and the frontier models — Claude, GPT, whatever is best — orchestrating them on your behalf, delegating tasks to them, and stripping your private context before anything leaves your machine. You get access to the best AI in the world without handing your life to it.

**MojOS** — Arch Linux rebuilt around the agent from the ground up. The agent isn't a feature bolted on — it's the primary interface. The OS is designed around it: changes happen in staging, get validated, and only commit once the agent is confident. Full system control. Always safe to undo.

**The Circus** — the infrastructure layer that connects your machines into one system. Your agent follows you across devices as one coherent intelligence, not a separate instance on each machine.

---

## Where this is at

This is one person — early in their career, first-year CS — who has a clear picture of how the future should look and is building toward it. The vision is bigger than the current ability to implement it. That's deliberate: build toward the right thing even if it takes time, rather than build the wrong thing fast.

If you find this interesting — whether you want to contribute, collaborate, or just talk about the ideas — reach out: [clarkehines@icloud.com](mailto:clarkehines@icloud.com)

---

## Repositories

| Repo | Purpose |
|---|---|
| [mojos](https://github.com/mojo-labs-circus/mojos) | MojOS — the OS |
| [mojo-agent](https://github.com/mojo-labs-circus/mojo-agent) | The agent |
| [dotfiles](https://github.com/mojo-labs-circus/dotfiles) | System dotfiles, deployed by MojOS |
| [ringmaster](https://github.com/mojo-labs-circus/ringmaster) | Early R&D — superseded by mojo-agent |

The thinking behind everything lives in the [mojo wiki](https://github.com/mojo-labs-circus/mojo/wiki).

---

## Philosophy

**Sovereignty is an axiom, not a feature.** At any point in the system you should be able to ask "who owns this data?" and get an unambiguous answer. If the answer is unclear, the design is wrong.

**Open source by necessity.** An AI that shapes how you work over a lifetime, running on closed source software, is not an AI you actually own. The only way "this is yours" is credible is if anyone can read, audit, and verify it.

**Privacy by architecture, not policy.** A privacy policy is a promise. Architecture is a guarantee.

**The technical users are the start, not the destination.** Right now this requires someone who knows Linux. Over time the agent lowers the barrier until owning your AI is the path of least resistance, not the hard path.

Code: [AGPL-3.0](https://github.com/mojo-labs-circus/mojos/blob/main/LICENSE) · Docs: [CC BY-SA 4.0](https://github.com/mojo-labs-circus/mojo/blob/main/LICENSE)
