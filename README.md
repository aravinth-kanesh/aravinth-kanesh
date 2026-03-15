# Aravinth Kaneshalingam

Final-year Computer Science student at King's College London (Predicted First Class). I work close to the metal - systems programming, low-latency infrastructure, and understanding exactly why things break.

My interests sit at the intersection of systems and security: compilers, memory safety, and how low-level vulnerabilities actually manifest. Currently building a coverage-guided fuzzing framework targeting Poly/ML (the runtime at the core of Isabelle/HOL's trusted computing base).

## Projects

**[Crux](https://github.com/aravinth-kanesh/crux)** - Optimal Rubik's Cube Solver · C++17, CMake

- Guarantees minimum-move solutions (≤20 moves, God's Number) via IDA* with pattern databases
- 88M-state corner pattern database stored as 4-bit nibbles (~42 MB); three 6-edge partial DBs built via BFS
- O(1) heuristic evaluation via coordinate move tables - no per-node arithmetic on the search hot path
- Parallel search across 18 root moves with atomic abort; 12-move scrambles under 30ms, 32-test suite validates optimality

**[DCache](https://github.com/aravinth-kanesh/distributed-cache)** - 
High-performance distributed in-memory cache · Go, Docker, Prometheus

- 256-shard concurrent map achieving 50M+ ops/sec with sub-25ns GET latency; 
  80+ Redis-compatible commands
- AOF persistence (buffered-channel writer, configurable fsync) + CRC-32C binary 
  snapshots for crash recovery
- Async master-slave replication via PSYNC with bounded ring-buffer backlog and 
  TCP connection hijacking
- Prometheus observability with per-command latency histograms; Docker Compose 
  stack with Grafana

**[Real-Time Market Data Simulator](https://github.com/aravinth-kanesh/market-data-simulator)** - Low-latency market data streaming engine · Python, asyncio, NumPy

- 1.4M+ ticks/s raw generation; 127k+ msg/s end-to-end across 10 subscribers with sub-200µs p99 latency and zero loss
- GBM price dynamics; asyncio fan-out with per-subscriber queue isolation and backpressure handling
- p50/p95/p99/p99.9 percentile tracking via NumPy vectorised operations, decoupled from the generation hot path
- 53-test suite covering GBM statistical properties, backpressure behaviour, and high-load end-to-end scenarios

## Currently Building

**Trust Me, I am a Verifier! (Or should you?) - Fuzzing the Poly/ML Compiler** · C, Standard ML, AFL++, LLVM, ASan/UBSan

- First systematic coverage-guided fuzzing framework for Poly/ML (Isabelle/HOL's trusted computing base) on ARM64
- Direct AFL++ binary fuzzing with LLVM LTO PCGUARD instrumentation; ASan/UBSan layered at runtime to avoid bootstrap failures
- 72 curated SML seeds; two-phase lexer/parser campaign strategy with evolved corpus handoff between phases
- Pre-campaign UBSan overflow in arm64.cpp:246; EC2 Graviton: 1,698 edges, 25.24% libpolyml/ coverage, 1,178 exec/sec

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
