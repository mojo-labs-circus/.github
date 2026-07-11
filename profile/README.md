# mojo-labs

**Personal AI is heading somewhere specific: always-on systems that remember
you, act for you, and follow you across every machine you own. A Jarvis. Every
product building one today welds it together as a monolith, and the piece that
matters most, the accumulated picture of you, is trapped inside. mojo-labs
exists to make Jarvis-style systems interoperable instead: a standard for the
pieces and the seams between them, so the open-source community can build these
the way it built Linux. Every piece competing and improving independently, no
lock-in, local and sovereign if you want it, and your data yours no matter what
you swap. Success isn't our implementation winning. It's the idea winning, and
if a better standard than ours is how it wins, that counts too.**

---

## The problem

Pick any personal AI product and you get everything as one inseparable block:
which model does the thinking, what loop drives it, where memory lives, what
tools it can reach, how it reaches you. None of those pieces need to be welded
together, and the one piece that genuinely matters, your accumulated context,
is locked inside the weld. The lock-in that matters was never "can I read the
code". It's "can I leave with what I've built up". A year of accumulated
memory inside any product's private format is a year of switching cost,
whatever the license says. Sovereignty is ownership plus portability. Either
one alone is branding.

And this is the moment it gets decided. Every serious product now pitches
persistence (an AI that knows you) as the product itself. The industry has
already started standardizing the easy seams on its own: MCP for tools,
SKILL.md for skills, A2A for agent-to-agent traffic, a converged wire format
for models. Nobody is standardizing the two seams that make the rest matter,
the portable shape of the identity data and the enforcement boundary that
protects it, because whoever holds those two holds the moat. That's the gap
this org exists to fill.

## What Mojo is

A standard, first: the **Mojo System Interface (MSI)**, effectively a POSIX
for personal AI. It defines every piece a complete Jarvis-style system is made
of and every seam between them, so that anyone can build a better
implementation of any piece and the owner runs whichever they want. The whole
system, drawn piece by piece and seam by seam, is
[anatomy.md](https://github.com/mojo-labs-circus/mojo/blob/main/anatomy.md),
the most concrete statement of what Mojo is.

One rule sits under everything: every piece is a replaceable implementation
except one. The identity, which is data. Your AI's memory of you, its persona,
your policies and permissions: plain portable files on your own hardware,
handed fresh to whatever agent runtime or model is actually doing the
thinking. Swap the agent, swap the model, and nothing that matters moves. The
assistant you know is built on data that never lived inside either one. That's
the Jarvis claim, and it's the falsifiable core of the whole project: if
identity doesn't survive the swap, Mojo has failed.

The standard doesn't invent what already exists. Where the industry has a real
answer, it's adopted. Where the market should compete (how an agent runtime
plans, how it thinks), the inside is deliberately left open. What gets defined
is only what nothing existing covers: the identity's shape, and the
enforcement boundary. That boundary is a kernel that checks every
consequential action against what the owner allowed, records what happened,
and keeps working offline. Those are also the two pieces mojo-labs builds
itself, because they're exactly the ones nobody with the resources has any
incentive to build: a neutral standard removes the moat. Every piece we build
is designed to be outcompeted through the same contracts it publishes. A
better kernel or memory layer replacing ours is the standard working, not
losing. A better standard replacing MSI itself would be too. It doesn't
matter whose name is on it, only that it exists.

## Why this instead of a monolith

Every builder in this space is currently forced to also build the parts they
don't actually care about. An agent-runtime builder ends up building
identity, memory, and permissions too, because there's nothing to plug into.
A memory-provider builder faces an N runtimes times M providers integration
matrix that punishes everyone but the biggest player. MSI turns both into one
shared contract: build the piece you're actually good at, and get access to
everyone else who speaks the same seam. Model vendors keep getting hired as
the best model for the job in every compliant system, the way AWS profits
enormously from Linux without owning it. Enterprises get what procurement
already needs and today can't get: portable context that isn't a
switching-cost trap, and an audit trail that answers "what did our AI do and
who allowed it." Open source gets eleven real seams to build into instead of
one project to fork and abandon. A vertical market, where whoever welds the
most together first wins the user, becomes a horizontal one, where whoever
builds the best version of one piece wins that layer.

## How this gets built

The system gets defined before code ships: the anatomy first, then the MSI
worked out seam by seam against real precedent (Unix, seL4, Plan 9,
Erlang/OTP), because a foundational layer has to get its abstractions right
before things depend on them. Then it gets proven the only way a standard can
be: a running system. The first Mojo system is a distro in the honest sense.
Existing parts that already speak the adopted standards, stitched around our
kernel and memory layer, dogfooded as a daily driver. Every seam is tested by
whether something real, built by someone who never heard of Mojo, actually
plugs into it. The milestone ends public: the MSI draft and a release a
stranger can stand up, posted online, to make the case that this is the way
forward and to invite people to make the MSI better and build implementations
of their own.

Our own implementations will be first and crude on purpose. Proof the seams
hold, not the best version of anything. How we build ours: Nix (the package
manager, which runs on any Linux distro) assembles and deploys the system,
with parts pinned, installs reproducible, and upgrades always safe to roll
back. MojOS, the OS I run myself, takes the same idea to the whole machine
(NixOS plus the defaults that make a machine running this system nicer to live
on). None of that is the standard's business: an implementer builds their
pieces however they want, and everything we learn about what helps gets
documented rather than required.

## Roadmap

**Now: the anatomy, then the MSI, Mk1.** The whole system mapped first, then
the standard derived from it seam by seam. No running software yet. A
deliberate tradeoff, not an oversight.

**Next: the first system.** Existing compliant parts stitched around our own
kernel and memory layer, lived with daily across real machines, then published
where people can pick it apart.

**Then: iterate in the open.** The standard and the system versioned together
as real use teaches what the first pass got wrong. Renting compute without
giving up sovereignty over what it's shown. And one experiment we're honest
about: once one Jarvis-style system is real, whether several of them can form
a group (a family, a team) without any member giving up what's theirs. We
think the primitives will support it. We won't claim it until we've tested it.
Full detail in
[roadmap.md](https://github.com/mojo-labs-circus/mojo/blob/main/roadmap.md).

## Who's building this

One person, and honesty about that is part of the design. I've just finished
the first year of a CS degree. This is a personal, hands-on learning
experiment, done in the open, the same register Linux was announced in: "just
a hobby, won't be big and professional." I believe interoperability is what
makes sovereignty real instead of branding, and I don't believe I can deliver
the whole of it alone, or now. I can build the seed: the first version of the
standard, the first kernel, the first memory layer, the first
stitched-together system. The thing it should become (better implementations
than mine, an ecosystem) is not a solo project, definitionally. It's designed
so that's an invitation.

If you find this interesting, whether you want to contribute, collaborate, or
just talk about the ideas, reach out:
[clarkehines@icloud.com](mailto:clarkehines@icloud.com)

---

## Repositories

| Repo | Purpose |
|---|---|
| [mojo](https://github.com/mojo-labs-circus/mojo) | The thinking: the anatomy, vision, philosophy, the Mojo System Interface |
| [mojos](https://github.com/mojo-labs-circus/mojos) | MojOS, the OS |
| [mojo-agent](https://github.com/mojo-labs-circus/mojo-agent) | Agent-side experiments; the first system aims to adopt existing runtimes, not build one |
| [dotfiles](https://github.com/mojo-labs-circus/dotfiles) | System dotfiles, deployed by MojOS |
| [ringmaster](https://github.com/mojo-labs-circus/ringmaster) | Early R&D, superseded |

---

## Philosophy

Sovereignty as an axiom, not a feature: the test at any point in the system
is "who owns this data," and if the answer is unclear, the design is wrong.
The standard itself doesn't mandate open source or local-only, the same way
POSIX allowed proprietary Unixes. It requires exactly one thing: identity
data stays in the portable shape, so nobody gets trapped. My own
implementation goes further by choice, not by requirement, open to the bone
and local by default, because a sovereignty claim is only credible if it can
be verified rather than promised. Privacy by architecture, not policy.

And built to lose on purpose. Every piece here, including the standard
itself, exists to be outcompeted: if someone builds a better kernel, a
better memory layer, even a better standard than the MSI, that's the idea
winning, not mojo-labs losing. Wanting credit and wanting the thing to exist
pull apart the moment they conflict, and this project already knows which
one it picks.

Full philosophy, with the reasoning behind each:
[philosophy.md](https://github.com/mojo-labs-circus/mojo/blob/main/philosophy.md).

---

*The world can get its mojo back.*

Code: [AGPL-3.0](https://github.com/mojo-labs-circus/mojos/blob/main/LICENSE) · Docs: [CC BY-SA 4.0](https://github.com/mojo-labs-circus/mojo/blob/main/LICENSE)
