# Paredros

**Personal AI has been moving in one direction for a while now: chatbots
first, one-off conversations with no memory between them, then agent
harnesses, loops that can actually take actions and use tools but still
mostly reset between sessions. The obvious next step is already showing up
as OpenClaw, Hermes, and others: a system that's always on, remembers
everything about you, and acts for you continuously, not just answering when
you ask but actually handling things on your behalf out in the world,
messaging people, researching, managing accounts, being present online the
way you would be yourself if you had the time. A digital counterpart, the
JARVIS-shaped assistant from Iron Man: less a tool you open and close, more
an extension of you that's always working.**

**Paredros is a call to standardize exactly these systems, so this becomes
something modular and interoperable, built from swappable pieces, instead of
every product welding its own closed stack shut. Right now I'm working on a
draft of exactly that. Its central idea: identity, a counterpart's actual
memory and character, gets broken out as its own portable layer, owned by
you, separate from whatever software is running it, so it can grow and
improve over time instead of starting over with every new piece. Still
early, still a plan, and this org is the space where that plan gets worked
out in the open.**

---

## The problem

Every serious personal-AI product being built right now is a monolith:
memory, permissions, and character welded to one vendor's stack. That's a
trap for individuals, a year of accumulated memory locked in one company's
private format is a year of switching cost no matter what the license says,
and it's a trap for companies too, procurement can't get portable context or
an audit trail out of a black box, so adoption stalls right when it starts to
matter.

Monoliths are also just slow. When one vendor owns every layer, every upgrade
is gated on that vendor's roadmap. Break the same system into pieces that
compete independently, memory providers against memory providers, runtimes
against runtimes, and each layer improves at its own pace instead of the
slowest one holding back the rest. It's the same reason Linux distros and
their package ecosystems keep getting better faster than any single vendor's
OS: competition at the piece level, not the whole-system level. Every
standard that's actually stuck (POSIX, TCP/IP, the web itself) made this
trade and the ecosystem got better for it.

Real efforts already exist and are making progress: MCP for tools, SKILL.md
for skills, A2A for agent-to-agent traffic, a W3C group working on memory
interoperability. But each is scoped to its own single piece in isolation,
nobody's attempting the whole system. This is probably not a one-document job
anyway, more likely a family of separate specs coordinated under one project.
Paredros is an attempt at exactly that: a standard at the scope of a full
digital counterpart system, not a claim that nobody else is working on
anything.

## What Paredros is

A standard is just a shared contract: an agreed shape that lets pieces built
by different people slot into each other, the way POSIX defines the
interface a Unix-like operating system has to provide so that software
written against it works across any of them, or the way HTTP lets any
browser talk to any server. Nobody has to trust the other builder, they only
have to agree on the interface between them.

Paredros draws that contract for a digital counterpart system: the pieces
it's made of, memory, identity, the enforcement layer, the agent runtime, and
the seams between them. It'll likely end up as a family of interfaces rather
than one document, plus eventually a conformance test suite that proves an
implementation actually complies, not just claims to.

That's the actual commitment right now: getting those seams right, not
building every piece myself. Once they're settled, anyone can build a real
implementation of any piece, and the people already building OpenClaw,
Hermes, and the rest end up helping the same fight just by competing against
each other on individual pieces, instead of each rebuilding a whole isolated
stack alone.

The whole draft, piece by piece and seam by seam, is written out in
[anatomy.md](https://github.com/mojo-labs-circus/paredros/blob/main/anatomy.md),
the most concrete map of what this is right now.

## Who's building this

I'm Clarke, second-year CS student. I've spent the last three months digging
into this: how personal AI actually works right now, what's already being
standardized (MCP, SKILL.md, A2A, the W3C memory work) and what isn't, and
why every serious product still ends up welding identity, memory, and
permissions into one closed stack anyway. That's what led here: the piece
missing isn't another product, it's a standard nobody's attempting at this
scope, and once it exists, everyone building OpenClaw, Hermes, and the rest
can actually build on shared ground instead of each solving the same problem
alone.

I can't build this by myself, and I'm not claiming to. What matters is the
standard existing, not Paredros being the one that wrote it, if a better
version of this comes from somewhere else, that's the goal working, not this
org losing.

Right now the most useful thing is looking at the actual design: read
anatomy.md, the piece list, and the seams between them, and say what's
missing, wrong, or drawn in the wrong place. If you've built or worked on
something like OpenClaw, Hermes, or similar, whatever you ran into is real
signal, bring it. Code contributors are needed too, soon, not to build one
reference implementation, but several independent ones. That's genuinely how
a standard gets proven: real standards require more than one working,
independent build before they count as settled, not a single official
example. Mostly, though, this is just an invitation to collaborate and help
build a community around getting this right.

If this is interesting to you, reach out:
[clarkehines@icloud.com](mailto:clarkehines@icloud.com)

---

## Repositories

| Repo | Purpose |
|---|---|
| [paredros](https://github.com/mojo-labs-circus/paredros) | The thinking and the draft standard: the anatomy, vision, philosophy, the pieces and seams |

More repos show up here as the interfaces get settled enough for real
implementations to start.

---

Docs: [CC BY-SA 4.0](https://github.com/mojo-labs-circus/paredros/blob/main/LICENSE)
