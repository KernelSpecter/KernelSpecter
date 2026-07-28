## Specter

I build local-first tools. They run on your own machine, at a footprint you can
measure, and they don't phone home.

Mostly Rust and Python on a CPU-only laptop, which turns out to be a useful
constraint. It forces you to find out what things actually cost instead of assuming
the hardware will cover for you.

<p>
  <img alt="Rust" src="https://img.shields.io/badge/Rust-B7410E?style=flat-square&logo=rust&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3B6E8F?style=flat-square&logo=python&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-8A7B2F?style=flat-square&logo=javascript&logoColor=white">
  <img alt="Win32" src="https://img.shields.io/badge/Win32-2A5D8F?style=flat-square&logo=windows&logoColor=white">
  <img alt="Linux" src="https://img.shields.io/badge/Linux-4A4F55?style=flat-square&logo=linux&logoColor=white">
</p>

### Projects

<table>
<tr>
<td width="50%">
<a href="https://github.com/KernelSpecter/hidforge"><img alt="hidforge" src="https://opengraph.githubassets.com/1/KernelSpecter/hidforge"></a>
</td>
<td width="50%">
<a href="https://github.com/KernelSpecter/AirLock"><img alt="AirLock" src="https://opengraph.githubassets.com/1/KernelSpecter/AirLock"></a>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/KernelSpecter/Alife"><img alt="Alife" src="https://opengraph.githubassets.com/1/KernelSpecter/Alife"></a>
</td>
<td width="50%">
<a href="https://github.com/KernelSpecter/mochi"><img alt="mochi" src="https://opengraph.githubassets.com/1/KernelSpecter/mochi"></a>
</td>
</tr>
</table>

**[hidforge](https://github.com/KernelSpecter/hidforge)** holds an exact click rate
from 10 to roughly 10,000 per second and idles at 0% CPU. It learns whatever a button
actually emits rather than assuming a button number, because side buttons don't
arrive on a predictable channel and some never reach the OS at all.

**[AirLock](https://github.com/KernelSpecter/AirLock)** strips API keys, passwords
and PII out of text before it reaches an LLM. A CLI you can pipe or hang off a
pre-commit hook, plus a
[browser extension](https://github.com/KernelSpecter/AirLock-extension) that catches
the paste itself. Entirely local, zero network calls, which is rather the whole point
of a tool for not leaking things.

**[Alife](https://github.com/KernelSpecter/Alife)** grows micro-organisms that learn
to survive within their own lifetime, no generational hand-waving, on a single CPU
core.

**[mochi](https://github.com/KernelSpecter/mochi)** is a cat that lives on your
desktop, watches you work, and expects to be fed.

**[Cadence](https://github.com/KernelSpecter/Cadence)** is a to-do app built around
the more interesting question: why you stop opening to-do apps.

### Currently

Learning cybersecurity properly, rather than by tutorial.

Reading an unreasonable amount of Win32 documentation as a side effect of hidforge:
Raw Input, HID report descriptors, and exactly how much a `QueryPerformanceCounter`
spin loop costs you.

---

Before hidforge there was
[autoclicker](https://github.com/KernelSpecter/autoclicker): 53 clicks per second,
non-adjustable, AutoHotkey. Most of what I've built since has been an argument with
that.
