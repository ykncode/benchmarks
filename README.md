# 🏎️ Yukinary (YKN) Performance & Benchmark Arena

Comprehensive systems benchmarks and industrial workload comparisons for the **Yukinary Programming Language**.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE-MIT)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE-APACHE)
[![Compiler: Yukinary](https://img.shields.io/badge/Main_Repository-ykncode/yukinary-brightgreen)](https://github.com/ykncode/yukinary)

---

## 📊 Overview

This repository hosts the official benchmark suite, competitor implementations, and test harnesses comparing Yukinary against industry-standard systems languages:

* **C** (GCC -O3 / Clang -O3)
* **Rust** (rustc / cargo --release)
* **Go** (go build)
* **Python** (CPython 3.12+)

---

## 🧪 Benchmark Suites

### 1. Cold-Start Startup Latency
Measures time-to-first-instruction and binary process initialization overhead. Yukinary's zero-runtime direct machine code boots in **sub-millisecond (< 1.2 ms)** time on both Windows PE32+ and Linux ELF64.

### 2. Micro-Workloads (`rivals/`)
* **SHA-256 Throughput:** 10,000,000 hashing rounds on 4 KB blocks.
* **JSON Serialization / Parsing:** Heavy nested object trees and dictionary key extraction.
* **HTTP Processing:** Memory-mapped socket parsing and response generation.
* **Matrix Multiplication & Arithmetic:** Loop variable register allocation (`RBX`, `R12`..`R15`) verification.
* **BitNet 1.58b Inference:** Ternary Transformer matrix-free integer dot products.

---

## 🛠️ Running the Benchmarks

```powershell
# Run the full industrial comparison suite
python industrial/run_systems_compare.ps1

# Run BitNet 1.58b comparison
python industrial/run_bitnet_compare.ps1

# Generate summary report
python report.py
```

Detailed measurement data and methodology are documented in [`industrial/YUKINARY_ENDUSTRIYEL_BENCHMARK_RAPORU.md`](industrial/YUKINARY_ENDUSTRIYEL_BENCHMARK_RAPORU.md).

---

## 📜 License

Dual-licensed under either of:
* Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE))
* MIT license ([LICENSE-MIT](LICENSE-MIT))

at your option.
