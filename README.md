# Aravinth Kaneshalingam

Final-year Computer Science student at King's College London (Predicted First Class). I gravitate towards systems programming, low-latency infrastructure, and understanding how things work close to the metal.

Currently fuzzing compiler runtimes in C and exploring what comes next - the kind of work where correctness and performance aren't optional.

## Projects

**[DCache](https://github.com/aravinth-kanesh/distributed-cache)** - High-performance distributed in-memory cache in Go
- 256-shard concurrent map achieving 50M+ ops/sec with sub-25ns GET latency; 80+ Redis-compatible commands
- AOF persistence (buffered-channel writer, configurable fsync) + CRC-32C binary snapshots for crash recovery
- Async master-slave replication via PSYNC with bounded ring-buffer backlog and TCP connection hijacking
- Prometheus observability with per-command latency histograms; Docker Compose stack with Grafana

**[Real-Time Market Data Simulator](https://github.com/aravinth-kanesh/market-data-simulator)** - Python, asyncio, NumPy
- 1.3M+ ticks/second throughput with sub-100µs p99 latency
- Geometric Brownian Motion price dynamics with per-subscriber queue isolation and backpressure handling

## Currently Building

**Poly/ML Compiler Fuzzing Framework** - C, Standard ML, AFL++, LLVM, ASan/UBSan
- First systematic fuzzing framework targeting Poly/ML (Isabelle/HOL's trusted computing base) on ARM64
- Persistent-mode AFL++ harness with LLVM LTO instrumentation and sanitiser integration

## Experience

**Software Engineer Intern - The Kusp Hub** (Summer 2025)
- Built an AI-powered career matching platform; reduced pipeline latency by 95% (75s → 2s) through offline vector pre-computation and cached sentence-transformer embeddings
- Engineered two-stage semantic matching: bi-encoder retrieval + category-weighted reranking with 97%+ accuracy in CV skill/experience extraction

## Technical Skills

**Languages:** Python, C/C++, Java, Go, Scala, JavaScript, SQL, Standard ML

**Systems & Tools:** Docker, Git, AFL++, LLVM, ASan/UBSan, asyncio, NumPy, Redis, Prometheus

**Frameworks:** Flask, Django, React

## Contact

[LinkedIn](https://www.linkedin.com/in/aravinth-kaneshalingam) · [Email](mailto:aravinth_kanesh@hotmail.com)
