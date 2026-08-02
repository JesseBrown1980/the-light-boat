# The light boat

> **Part of it all:** [the bridge](https://jessebrown1980.github.io/the-bridge-to-all-of-it/) — every public thing in one place, so none of it gets lost.

**One button:** → **https://jessebrown1980.github.io/the-light-boat/**

Two people, one exchange, then a direct line with **nothing in the middle** — and
the block you have to carry is **61% smaller** than the raw one.

---

## Reduction for headroom

A raw WebRTC offer runs about a thousand characters, and nearly all of it is
boilerplate that is **byte-identical every single time**. Only four things are
actually yours:

```
the ufrag        the password        the fingerprint        the candidates
```

Everything else is rebuilt from a template on arrival.

**MEASURED:**

```
raw            1,060 characters
what you carry   414 characters      61% less
round trip     expands back with every field intact
```

Nothing was approximated. **The parts that were dropped were the parts that are
constant** — which is the difference between reduction and loss.

---

## What is free, and the one thing that isn't

**No server of ours touches your words.** Once the line opens it is browser to
browser. Nothing is stored, logged or relayed — there is nothing in the middle to
do it with. No account, no install, no host, no registry.

The one thing that isn't free, stated rather than hidden: to find a route across
the internet, browsers ask a public **STUN** server for their own outside address.
Free ones. They see that two addresses asked; **they never see a word of what you
say.** On the same wifi it doesn't need them at all.

---

## The address is the content

The colour bar is the **sha-256 of your own block** — two brown stops, banded
`16…240`, luminance-clamped `32…224`. Same addressing as every leaf, every zebra,
and the kernel itself.

**Nobody hands out names here, so nobody can take one away.**

---

## What is not here yet, and why

The plan was to show the block as a **coloured QR** so the handshake itself would
be light — photons off one screen into another camera, no network in the meeting at
all. Three channels instead of one, so three times the data in the same square.

**The idea is verified:** 414 characters fits a single version-13 code and OpenCV
decodes it back exactly.

**The encoder written for it does not yet produce a valid code.** Checked against a
reference implementation at all eight mask patterns — no match at any of them. Two
bugs were found and fixed along the way (a format-info cell placed into the timing
row, and a data module wrongly reserved), and it still does not agree.

So it is not in this page.

> **A code that half-reads is worse than none**, because you find out while
> holding a phone up in front of somebody.

It goes in when it passes, and not before.

---

## Proven on real hardware

```
phone     192.168.15.4
browser   192.168.15.9
between   nothing

first message out    delivered
reply back           delivered
```

---

**Jesse Daniel Brown (OP-JESSE).**

*One meeting point, then free forever.*
