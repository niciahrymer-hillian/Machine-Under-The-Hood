# 📖 Lesson Plan — Machine-Under-The-Hood

> **Chain K — Hardware & Systems Foundations** | What a computer is really doing: CPU, memory hierarchy, storage, and buses — the mental model everything else sits on.

## What This Project Is

Build a working mental model of the physical machine — CPU, memory hierarchy, storage, buses — so performance behaviour stops being mysterious.

## Learning Objectives

By the end I can:

1. Describe what a CPU does per cycle and what cores and pipelines buy you.
2. Order the **memory hierarchy** by latency and explain the cost of each level.
3. Explain why sequential access beats random on both disk and RAM.
4. Compare HDD and SSD behaviour and failure characteristics.
5. Classify a workload as CPU-, memory-, or I/O-bound.
6. Predict how a data structure's layout affects cache behaviour.

## Software You Will Use

- A machine you can inspect (`lscpu`, `free`, `iostat`).
- Benchmark tools (`sysbench`, `fio`).
- A simple program to demonstrate cache effects.

## Build Order

1. Inventory your own machine's specifications.
2. Benchmark sequential vs random reads on disk.
3. Write a program that traverses an array in cache-friendly and cache-hostile order; measure the gap.
4. Observe memory pressure and swapping deliberately.
5. Profile a workload and classify its bottleneck.
6. Write up the latency numbers in your own words.

## Common Mistakes to Avoid

- Treating all memory as equally fast.
- Assuming more cores always means faster.
- Ignoring data locality in hot loops.
- Benchmarking with caches warm and calling it cold performance.
- Optimising code when the bottleneck is I/O.

## Check Your Understanding

The quiz covers the latency hierarchy, cache effects, sequential vs random access, and bottleneck classification.

## Why This Matters (Industry Application)

Understanding the machine is what turns performance work from guesswork into diagnosis. It's also the
substrate for systems programming, database internals, and distributed systems — every one of which assumes
you know why sequential access beats random and why memory is precious.

## Reflection Questions

- Which slow program you have written was actually memory-bound rather than CPU-bound?
- How does this change how you would size a cloud instance?
