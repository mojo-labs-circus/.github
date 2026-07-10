# mojo-labs

**Give everyone a persistent AI identity that's genuinely theirs — a Jarvis —
by refusing to let any single product weld together the pieces an AI system is
actually made of. The lock-in that matters was never "can I read the code";
it's "can I leave with what I've built up." So the actual work is a standard:
the contract at every seam, adopting the industry's real answers where they
exist, building the two pieces nobody with the resources has any incentive to
build — and keeping everything else swappable through those contracts,
permanently. Success isn't Mojo's own implementation winning. It's the idea
winning.**

## A vision of the future

This is how I think the future should look: every person has an AI that is genuinely theirs. It lives on hardware in their home, always on. It grows with them over years — learning how they think, how they work, what they value — until it becomes a real extension of themselves. Not a tool they use. A counterpart that knows them. The longer they have it the more valuable it becomes, and it's theirs in the same way their memories are theirs. No company owns it. No subscription can take it away.

That AI gives them capabilities that only technical people have access to right now. It controls their machines, manages their files, automates the things they don't want to think about, and acts as a proxy to the best AI models in the world — delegating the heavy lifting while keeping their private context on their own hardware. It follows them across every device they own as one coherent intelligence.

mojo-labs is an effort to make that possible.

---

## The problems in the way

**The capability gap.** The tools that make computers genuinely powerful — Linux, version control, system configuration, scripting, automation — are only accessible to people who spent years learning them. Technical users have an enormous advantage over everyone else, and AI is widening that gap: the people who already know these tools can use AI to go faster. Everyone else still clicks through menus. The agent closes that gap — full system capability, through conversation, no expertise required.

**Sovereignty.** Compute has centralised twice. Mainframes sat in institutions until the PC decentralised it. Then the cloud came with better UX as the bribe, and people handed back their data, their compute, their sovereignty without noticing. AI is the same inflection point. Every major assistant today routes through someone's cloud, learns from your data, and answers to a company whose incentives are not yours. Data is power — whoever holds the picture of who you are has power over you. The only real answer is ownership — and ownership has a second half: a fully open-source, self-hosted assistant still traps you if your accumulated memory sits in its private format. Sovereignty is ownership plus portability. Either one alone is branding.

**Context.** Every AI conversation starts from zero. You re-explain who you are, what you're working on, what you've already figured out — every single time. There's no persistent picture of you. A real personal AI fixes this: it carries your context permanently, across every device, and uses it to actually understand you rather than asking you to repeat yourself.

**Fragmentation.** When people work together today, each person brings their own separate AI tool, and coordination happens despite that, not through it. There's no shared system — just individuals, each with their own assistant, hoping it adds up.

---

## What Mojo actually is

A standard, first: the **Mojo System Interface** — effectively a POSIX for
personal AI. It defines every piece a complete personal AI system is made of
and every seam between them, so that anyone can build a better implementation
of any piece and the owner runs whichever they want. The whole system, drawn
piece by piece and seam by seam, is
[anatomy.md](https://github.com/mojo-labs-circus/mojo/blob/main/anatomy.md) —
the most concrete statement of what Mojo is.

The standard doesn't invent what already exists. Where the industry has a
real, working answer, it's adopted — MCP for tools, SKILL.md for skills, the
already-converged model wire format, A2A for talking to agents outside your
system. Where the market should compete — how an agent runtime plans, how it
thinks — the inside is deliberately left open. What gets defined is only what
nothing existing covers: the portable shape of the identity data, and the
enforcement boundary that protects it. Those are also the two pieces
mojo-labs builds itself — the first kernel and the first memory layer —
because they're the seams nobody with the resources to build them has any
incentive to build: a neutral standard removes the moat.

Every piece Mojo builds is designed to be outcompeted through the same
contracts it publishes. A better kernel, a better memory implementation,
speaking the same standard, replacing Mojo's own — that's the standard
working, not losing. This is the same move that grew Linux: good interfaces,
and an ecosystem nobody owns.

The first Mojo system is a distro in the honest sense — assembled from
existing parts that already speak the adopted standards, around the kernel and
memory layer that make them one system. That's the proof, not a shortcut:
every seam in the standard gets tested by whether something real, built by
someone who never heard of Mojo, actually plugs into it.

---

## Jarvis — the identity

Jarvis is Mojo's core claim, not a specific piece of software. The identity is
data: your AI's memory of you, its persona, your policies and permissions —
plain portable files that live on your own hardware and get handed fresh to
whatever agent runtime or model is actually doing the thinking. Swap the
agent, swap the model, and nothing that matters moves: the character you know
is built on data that never lived inside either one. The system sits between
you and the frontier models — Claude, GPT, whatever is best — hiring them for
a task at a time and stripping your private context before anything leaves
your machine. You get access to the best AI in the world without handing it
your life.

Anything that speaks the standard can plug in and pick up the same identity,
the same memory, the same permissions, on any machine you own.

## MojOS — the OS

Mojo runs on any Linux distribution — that's a design constraint of the
standard, not a preference. MojOS is personal, not central: the OS I run
myself — NixOS plus the defaults that make a machine running this system
nicer to live on, the whole machine declarative and always safe to roll
back. Nothing in Mojo requires it; it's offered because the same defaults
that help me will probably help anyone doing the same thing. Best home,
never a requirement.

It's also a workshop with its own personality: modes that change how the
system looks and feels — dense and technical for deep work, plain and quiet
for when other people are around.

## Collectives

A bet the primitives have to earn, not a feature on a list: if the
individual-sovereignty primitives are right, the same structure that holds one
person and their machines should hold several people sharing a system — a
team, a family, a community — each member still sovereign, AI as a full
participant with real standing, always accountable back to a person.

A real, converging body of academic work — Hybrid Intelligence, Hybrid
Intelligence Teams, COHUMAIN, and legal theory on treating human-AI "hybrids"
as their own accountable entity — has been arguing the group is the right unit
of analysis since 2019. Nobody's built the system that treats it as one.
Deliberately second: reached only once the single-owner system is real. Full
lineage in
[collective-intelligence-research.md](https://github.com/mojo-labs-circus/mojo/blob/main/collective-intelligence-research.md).

---

## How this gets built

Mojo is designed the way an operating system is designed, not improvised by
wrapping existing AI tools together. Before any code ships, the system itself
gets defined: the anatomy first —
[anatomy.md](https://github.com/mojo-labs-circus/mojo/blob/main/anatomy.md),
every piece and seam of the whole system — then the Mojo System Interface,
worked out seam by seam and checked against real precedent (Unix, seL4,
Plan 9, Erlang/OTP) before anything gets built against it — and then proven by
a running system assembled from as many existing parts as possible, because a
standard earns authority from running code, never from being declared. The
thinking behind all of it is public, in the
[mojo](https://github.com/mojo-labs-circus/mojo) repo.

---

## Roadmap

**Now — the anatomy, then the Mojo System Interface, Mk1.** The whole system
mapped first, then the standard derived from it seam by seam, checked against
real precedent. No running software yet — a deliberate tradeoff, not an
oversight.

**Next — Mojo, Mk1.** The first system: existing compliant parts stitched
around Mojo's own kernel and memory layer, dogfooded as a daily driver, across
however many machines exist.

**Then — iterate.** Renting compute (borrowing more than you own, without
giving up sovereignty over what it's shown) and Collectives get built out
deeper as the system matures. The full detail lives in
[roadmap.md](https://github.com/mojo-labs-circus/mojo/blob/main/roadmap.md).

---

## Who's building this

One person, and honesty about that is part of the design. I've just finished
the first year of a CS degree. This is a personal, hands-on learning
experiment, done in the open — the same register Linux was announced in:
"just a hobby, won't be big and professional." I believe this is what AI
actually needs — interoperability is what makes sovereignty real instead of
branding — and I don't believe I can deliver the whole of it alone, or now.
I can build the seed: the first version of the standard, the first kernel,
the first memory implementation, the first stitched-together system. The
thing it should become — better implementations than mine, an ecosystem — is
not a solo project, definitionally. It's designed so that's an invitation.

If you find this interesting — whether you want to contribute, collaborate, or just talk about the ideas — reach out: [clarkehines@icloud.com](mailto:clarkehines@icloud.com)

---

## Repositories

| Repo | Purpose |
|---|---|
| [mojo](https://github.com/mojo-labs-circus/mojo) | The thinking — the anatomy, vision, philosophy, the Mojo System Interface |
| [mojos](https://github.com/mojo-labs-circus/mojos) | MojOS — the OS |
| [mojo-agent](https://github.com/mojo-labs-circus/mojo-agent) | Agent-side experiments — the first system aims to adopt existing runtimes, not build one |
| [dotfiles](https://github.com/mojo-labs-circus/dotfiles) | System dotfiles, deployed by MojOS |
| [ringmaster](https://github.com/mojo-labs-circus/ringmaster) | Early R&D — superseded |

---

## Philosophy

Sovereignty as an axiom, not a feature. Open source by necessity — the only
way "this is yours" is credible. Privacy by architecture, not policy. And
technical users are the start, not the destination — the agent exists to
lower that barrier over time, not keep it high.

Full philosophy, with the reasoning behind each:
[philosophy.md](https://github.com/mojo-labs-circus/mojo/blob/main/philosophy.md).

---

*The world can get its mojo back.*

Code: [AGPL-3.0](https://github.com/mojo-labs-circus/mojos/blob/main/LICENSE) · Docs: [CC BY-SA 4.0](https://github.com/mojo-labs-circus/mojo/blob/main/LICENSE)
