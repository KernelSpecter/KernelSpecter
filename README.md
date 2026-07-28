## Specter

I build local-first tools: they run on your own machine, at a footprint you can
measure, and they don't phone home.

Mostly Rust and Python, on a CPU-only laptop — which turns out to be a useful
constraint. It forces you to find out what things actually cost instead of assuming
the hardware will cover for you.

### Projects

**[hidforge](https://github.com/KernelSpecter/hidforge)** · Rust

A macro engine for *any* mouse, not just the one whose vendor software you happened to
install. Holds an exact click rate from 10 to ~10,000 per second and costs 0% CPU
sitting idle. It learns whatever a button actually emits rather than assuming a button
number — because side buttons don't arrive on a predictable channel, and some never
reach the OS at all.

**[AirLock](https://github.com/KernelSpecter/AirLock)** · Python · and its
**[browser extension](https://github.com/KernelSpecter/AirLock-extension)** · JavaScript

Strips API keys, passwords and PII out of text before it reaches an LLM. A CLI you can
pipe or hang off a pre-commit hook, plus an extension that catches the paste itself.
Entirely local, zero network calls — which is rather the whole point of a tool for not
leaking things.

**[Alife](https://github.com/KernelSpecter/Alife)** · Python

Micro-organisms in a petri dish that learn to survive within their own lifetime, no
generational hand-waving. Runs on a single CPU core.

**[mochi](https://github.com/KernelSpecter/mochi)** · Python

A cat that lives on your desktop, watches you work, and expects to be fed.

**[Cadence](https://github.com/KernelSpecter/Cadence)**

A to-do app built around the more interesting question: why you stop opening to-do
apps.

### Currently

Learning cybersecurity properly, rather than by tutorial.

Reading an unreasonable amount of Win32 documentation as a side effect of hidforge —
Raw Input, HID report descriptors, and exactly how much a `QueryPerformanceCounter`
spin loop costs you.

---

Before hidforge there was
[autoclicker](https://github.com/KernelSpecter/autoclicker): 53 clicks per second,
non-adjustable, AutoHotkey. Most of what I've built since has been an argument with
that.
