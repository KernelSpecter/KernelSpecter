<h1 align="center">Specter</h1>

<p align="center">
  <b>I build local-first tools</b><br>
  <sub>They run on your own machine, at a footprint you can measure, and they don't phone home.</sub>
</p>

<p align="center">
  <img alt="Rust" src="https://img.shields.io/badge/Rust-B7410E?style=flat-square&logo=rust&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3B6E8F?style=flat-square&logo=python&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-8A7B2F?style=flat-square&logo=javascript&logoColor=white">
  <img alt="Win32" src="https://img.shields.io/badge/Win32-2A5D8F?style=flat-square&logo=windows&logoColor=white">
  <img alt="Linux" src="https://img.shields.io/badge/Linux-4A4F55?style=flat-square&logo=linux&logoColor=white">
</p>

Mostly Rust and Python on a CPU-only laptop, which turns out to be a useful
constraint. It forces you to find out what things actually cost instead of assuming
the hardware will cover for you.

### Projects

<table>
<tr>
<td width="50%">
<a href="https://github.com/KernelSpecter/nowwatching"><img alt="nowwatching" src="https://opengraph.githubassets.com/1/KernelSpecter/nowwatching"></a>
</td>
<td width="50%">
<a href="https://github.com/KernelSpecter/hidforge"><img alt="hidforge" src="https://opengraph.githubassets.com/1/KernelSpecter/hidforge"></a>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/KernelSpecter/AirLock"><img alt="AirLock" src="https://opengraph.githubassets.com/1/KernelSpecter/AirLock"></a>
</td>
<td width="50%">
<a href="https://github.com/KernelSpecter/anicli-rpc"><img alt="anicli-rpc" src="https://opengraph.githubassets.com/1/KernelSpecter/anicli-rpc"></a>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/KernelSpecter/quorum"><img alt="quorum" src="https://opengraph.githubassets.com/1/KernelSpecter/quorum"></a>
</td>
<td width="50%">
<a href="https://github.com/KernelSpecter/Alife"><img alt="Alife" src="https://opengraph.githubassets.com/1/KernelSpecter/Alife"></a>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/KernelSpecter/mochi"><img alt="mochi" src="https://opengraph.githubassets.com/1/KernelSpecter/mochi"></a>
</td>
<td width="50%">
<a href="https://github.com/KernelSpecter/Cadence"><img alt="Cadence" src="https://opengraph.githubassets.com/1/KernelSpecter/Cadence"></a>
</td>
</tr>
</table>

**[nowwatching](https://github.com/KernelSpecter/nowwatching)** is Rich Presence for
films and series: the show's own name in the header, poster art, and a live
countdown. It reads the Windows media session, so there is nothing to enable per site
and no extension needed, and the extension that ships with it is only there for the
sites a title string alone cannot describe. Discord animates a card's progress bar
client-side and has no field that means stopped, so a paused bar cannot be frozen at
all. It can only be put back where it belongs, which it now is every ten seconds.

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

**[anicli-rpc](https://github.com/KernelSpecter/anicli-rpc)** does the same job for
anime from a terminal, by sitting between ani-cli and mpv without patching either of
them. Sub or dub is deduced from the audio track's language tag, because ani-cli
picks one and then never tells the player which. nowwatching ignores mpv on purpose
so the two never publish the same episode twice.

**[quorum](https://github.com/KernelSpecter/quorum)** takes attendance from a signed
token the room hears at 19 kHz, with no GPS, no camera and no box on the wall. It
does not claim to stop one student carrying five friends' phones, because no audio
scheme ever has. It claims to notice: the same devices in the same room every day for
three weeks is a signature, and that goes in a report.

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

Local IPC, lately. Discord frames its messages with an 8-byte header, mpv speaks
line-delimited JSON, and underneath both it is named pipes on Windows or Unix sockets
on Linux, which are far less interchangeable than they look.

The Windows media session too, which hands you a title, a duration and a timeline for
anything playing on the machine, and then quietly stops updating that timeline the
moment the tab goes to the background. Two bugs traced back to reading that silence
as a pause.

---

Before hidforge there was
[autoclicker](https://github.com/KernelSpecter/autoclicker): 53 clicks per second,
non-adjustable, AutoHotkey. Most of what I've built since has been an argument with
that.
