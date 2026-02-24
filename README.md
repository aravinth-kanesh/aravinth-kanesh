# Aravinth Kaneshalingam

Final-year Computer Science student at King's College London (Predicted First Class). I gravitate towards systems programming, low-latency infrastructure, and understanding how things work close to the metal.

Currently fuzzing compiler runtimes in C and building an optimal Rubik's cube solver in C++ - the kind of work where correctness and performance aren't optional.

## Key Projects

**[DCache](https://github.com/aravinth-kanesh/distributed-cache)** - High-performance distributed in-memory cache in Go
- 256-shard concurrent map achieving 50M+ ops/sec with sub-25ns GET latency; 80+ Redis-compatible commands
- AOF persistence (buffered-channel writer, configurable fsync) + CRC-32C binary snapshots for crash recovery
- Async master-slave replication via PSYNC with bounded ring-buffer backlog and TCP connection hijacking
- Prometheus observability with per-command latency histograms; Docker Compose stack with Grafana

**[Real-Time Market Data Simulator](https://github.com/aravinth-kanesh/market-data-simulator)** - Python, asyncio, NumPy
- 1.4M+ ticks/second raw generation throughput; 127k+ msg/s end-to-end delivery across 10 concurrent subscribers with zero message loss
- Geometric Brownian Motion price simulation with asyncio fan-out, per-subscriber queue isolation, and sub-200µs p99 latency at normal trading rates

## Currently Building

**Poly/ML Compiler Fuzzing Framework** - C, Standard ML, AFL++, LLVM, ASan/UBSan
- First systematic fuzzing framework targeting Poly/ML (Isabelle/HOL's trusted computing base) on ARM64
- Persistent-mode AFL++ harness with LLVM LTO instrumentation and sanitiser integration

**[Optimal Rubik's Cube Solver](https://github.com/aravinth-kanesh/optimal-cube)** - C++17, CMake

- Guarantees minimum-move solutions (≤20 moves, per God's Number) via IDA* with pattern databases
- 88M-state corner pattern database stored as 4-bit nibbles (~42 MB); built once via BFS, loaded at runtime
- Eliminated all encoding from the search hot path: coordinate move tables give O(1) heuristic evaluation - no arithmetic, just table lookups per node
- Targets: 15-move scrambles < 1s, 18-move < 60s; 36-test suite validates optimality and solution correctness

## Experience

**Software Engineer Intern - The Kusp Hub** (Summer 2025)
- Built an AI-powered career matching platform; reduced pipeline latency by 95% (75s → 2s) through offline vector pre-computation and cached sentence-transformer embeddings
- Engineered two-stage semantic matching: bi-encoder retrieval + category-weighted reranking with 97%+ accuracy in CV skill/experience extraction

## Technical Skills

**Languages:** Python, C/C++, Java, Go, Scala, JavaScript, SQL, Standard ML

**Systems & Tools:** Docker, Git, AFL++, LLVM, ASan/UBSan, asyncio, NumPy, Redis, Prometheus, CMake

**Frameworks:** Flask, Django, React

## Contact

[LinkedIn](https://www.linkedin.com/in/aravinth-kaneshalingam) · [Email](mailto:aravinth_kanesh@hotmail.com)
