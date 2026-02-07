# Aravinth Kaneshalingam

Final-year Computer Science student at King's College London (Predicted First Class). I gravitate towards systems programming, low-latency infrastructure, and understanding how things work close to the metal.

Currently building distributed systems in Go and fuzzing compiler runtimes in C — the kind of work where correctness and performance aren't optional.

## What I'm Working On

**[DCache](https://github.com/aravinth-kanesh/distributed-cache)** — High-performance distributed in-memory cache in Go
- Sharded concurrent map (256 shards, per-shard RWMutex) achieving 50M+ ops/sec on Apple M2
- Redis-compatible RESP protocol layer — works with redis-cli out of the box
- Sub-25ns p99 GET latency, lock-free atomic metrics, sync.Pool buffer recycling
- 60+ commands across strings, lists, hash tables, and sets

**Poly/ML Compiler Fuzzing Framework** — C, Standard ML, AFL++, LLVM, ASan/UBSan
- First systematic fuzzing framework targeting Poly/ML (Isabelle/HOL's trusted computing base) on ARM64
- Persistent-mode AFL++ harness with LLVM LTO instrumentation and sanitiser integration

**Real-Time Market Data Simulator** — Python, asyncio, NumPy
- 1.3M+ ticks/second throughput with sub-100µs p99 latency
- Geometric Brownian Motion price dynamics with per-subscriber queue isolation and backpressure handling

## Experience

**Software Engineer Intern — The Kusp Hub** (Summer 2025)
- Built an AI-powered career matching platform; reduced pipeline latency by 95% (75s → 2s) through offline vector pre-computation and cached sentence-transformer embeddings
- Engineered two-stage semantic matching: bi-encoder retrieval + category-weighted reranking with 97%+ accuracy in CV skill/experience extraction

## Technical Skills

**Languages:** Python, C/C++, Java, Go, Scala, JavaScript, SQL, Standard ML

**Systems & Tools:** Docker, Git, AFL++, LLVM, ASan/UBSan, asyncio, NumPy

**Frameworks:** Flask, Django, React

## Contact

[LinkedIn](https://www.linkedin.com/in/aravinth-kaneshalingam) · [Email](mailto:aravinth_kanesh@hotmail.com)
