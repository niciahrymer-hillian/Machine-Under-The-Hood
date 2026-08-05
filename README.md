# Machine-Under-The-Hood

### What a computer is really doing: CPU, memory hierarchy, storage, and buses — the mental model everything else sits on.

![Chain K](https://img.shields.io/badge/Chain%20K-64748B?style=for-the-badge) [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge)](LICENSE-GPL) [![License: AGPL v3](https://img.shields.io/badge/License-AGPLv3-blue?style=for-the-badge)](LICENSE-AGPL)

[📖 Lesson Plan](docs/LESSON_PLAN.md)

<!-- SCREENSHOT PLACEHOLDER: docs/screenshots/overview.png -->

> ⬜ **Scaffold pending.** Directory created to portfolio standard; full content (README, lesson plan, tour + quiz, skeleton code) still to be built. Part of **Chain K — Hardware & Systems Foundations**.

## Why This Was Built

I write software that runs on hardware I couldn't describe in detail, and that bothers me. When code is
slow, the explanation is often physical — a cache miss, a disk seek, memory pressure — and without a model
of the machine those explanations are just words.

This is the foundation for the rest of Chain K: what the CPU actually does per cycle, why memory is a
hierarchy rather than one pool, and why the gap between an L1 hit and a disk read is measured in factors of
a million.

## Why This Matters (Industry Application)

Understanding the machine is what turns performance work from guesswork into diagnosis. It's also the
substrate for systems programming, database internals, and distributed systems — every one of which assumes
you know why sequential access beats random and why memory is precious.

## Topics Covered

| Area | What this project covers |
|------|--------------------------|
| CPU | Cores, clock cycles, pipelines, and instruction execution |
| Memory hierarchy | Registers → L1/L2/L3 → RAM → disk, and the cost of each |
| Storage | HDD vs SSD, sequential vs random access |
| Buses | How components actually talk to each other |
| Bottlenecks | Recognizing CPU-bound vs memory-bound vs I/O-bound |
| Implications | Why data locality and access patterns dominate performance |

## How This Connects

Chain K (Hardware & Tinkering). The foundation for **Build-A-PC** and **Linux-On-Old-Hardware**; explains performance behavior in **Chain O**.

---
Dual licensed — [GPL v3](LICENSE-GPL) and [AGPL v3](LICENSE-AGPL).
