# Aravinth Kaneshalingam

Final-year Computer Science student at King's College London (Predicted First 
Class). I work close to the metal - systems programming, low-latency 
infrastructure, and understanding exactly why things break.

My interests sit at the intersection of systems and security: compilers, memory 
safety, and how low-level vulnerabilities actually manifest. Currently building 
a coverage-guided fuzzing framework targeting Poly/ML (the runtime at the core 
of Isabelle/HOL's trusted computing base) and an optimal Rubik's cube solver 
in C++.

## Projects

**[DCache](https://github.com/aravinth-kanesh/distributed-cache)** - 
High-performance distributed in-memory cache in Go

- 256-shard concurrent map achieving 50M+ ops/sec with sub-25ns GET latency; 
  80+ Redis-compatible commands
- AOF persistence (buffered-channel writer, configurable fsync) + CRC-32C binary 
  snapshots for crash recovery
- Async master-slave replication via PSYNC with bounded ring-buffer backlog and 
  TCP connection hijacking
- Prometheus observability with per-command latency histograms; Docker Compose 
  stack with Grafana

**[Real-Time Market Data Simulator](https://github.com/aravinth-kanesh/
market-data-simulator)** - Python, asyncio, NumPy

- 1.4M+ ticks/second raw generation throughput; 127k+ msg/s end-to-end delivery 
  across 10 concurrent subscribers with zero message loss
- Geometric Brownian Motion price simulation with asyncio fan-out, 
  per-subscriber queue isolation, and sub-200µs p99 latency

## Currently Building

**Poly/ML Compiler Fuzzing Framework** - C, Standard ML, AFL++, LLVM, 
ASan/UBSan

- First systematic fuzzing framework targeting Poly/ML (Isabelle/HOL's trusted 
  computing base) on ARM64 - finding memory safety violations and undefined 
  behaviour in a runtime that formal verification tools depend on
- Persistent-mode AFL++ harness with LLVM LTO instrumentation and 
  ASan/UBSan integration for crash triage

**[Optimal Rubik's Cube Solver](https://github.com/aravinth-kanesh/
optimal-cube)** - C++17, CMake

- Guarantees minimum-move solutions (≤20 moves, God's Number) via IDA* with 
  pattern databases
- 88M-state corner pattern database stored as 4-bit nibbles (~42 MB); built once 
  via BFS, loaded at runtime
- O(1) heuristic evaluation via coordinate move tables - no arithmetic on the 
  search hot path, just table lookups
- 15-move scrambles < 1s, 18-move < 60s; 36-test suite validates optimality

## Experience

**Software Engineer Intern - The Kusp Hub** (Summer 2025)

- Built an AI-powered career matching platform; reduced pipeline latency by 95% 
  (75s → 2s) through offline vector pre-computation and cached 
  sentence-transformer embeddings
- Engineered two-stage semantic matching: bi-encoder retrieval + 
  category-weighted reranking with 97%+ accuracy in CV skill/experience 
  extraction

## Technical Skills

**Languages:** Python, C/C++, Java, Go, Scala, JavaScript, SQL, Standard ML  
**Systems & Tools:** Docker, Git, AFL++, LLVM, ASan/UBSan, asyncio, NumPy, 
Redis, Prometheus, CMake  
**Frameworks:** Flask, Django, React

## Contact

[LinkedIn](https://www.linkedin.com/in/aravinth-kaneshalingam) · 
[Email](mailto:aravinth_kanesh@hotmail.com)
