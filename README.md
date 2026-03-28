# Aravinth Kaneshalingam

Final-year Computer Science student at King's College London (Predicted First Class). I work close to the metal - systems programming, low-latency infrastructure, and understanding exactly why things break.

My interests sit at the intersection of systems and security: compilers, memory safety, and how low-level vulnerabilities actually manifest. I built a coverage-guided fuzzing framework targeting Poly/ML (the runtime at the core of Isabelle/HOL's trusted computing base), finding UBSan and memory safety bugs in ARM64-specific compiler code.

## Projects

**Trust Me, I am a Verifier! (Or should you?) - Fuzzing the Poly/ML Compiler** · C, Standard ML, AFL++, LLVM, ASan/UBSan

- First systematic coverage-guided fuzzing framework for Poly/ML (Isabelle/HOL's trusted computing base) on ARM64
- Direct AFL++ binary fuzzing with LLVM LTO PCGUARD instrumentation; ASan/UBSan layered at runtime to avoid bootstrap failures; CMPLOG and rare power schedule added for Phase 2
- 72 curated SML seeds + Isabelle/HOL corpus; two-phase lexer/parser strategy with afl-cmin minimisation and evolved corpus handoff between phases
- Pre-campaign UBSan overflow in `arm64.cpp:246`; SIGSEGV crashes in module elaboration; EC2 Graviton: 2,017 edges, 28.57% `libpolyml/` coverage, ~24.9 exec/sec (Phase 1)

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

**[Auteur](https://github.com/aravinth-kanesh/auteur)** - Personal cinema intelligence engine · Python, FastAPI, React, ChromaDB, SQLite

- Local RAG pipeline: sentence-transformers embeddings over watch history stored in ChromaDB; semantic retrieval drives a streaming conversational AI (Ollama / Anthropic)
- Progressive taste profiling — fast DB-only stats endpoint + async LLM endpoint for cinematic identity summary and hidden pattern detection
- Full-stack: FastAPI backend with SQLite persistence, React + Tailwind frontend with real-time streaming chat and filter/sort history browser

## Experience

**Software Engineer Intern - The Kusp Hub** (June - September 2025)

- Architected AI-powered career discovery platform with 97%+ CV skill extraction 
  accuracy using LLM structured outputs (Groq API) and coordinate-based 
  multi-column PDF reconstruction with PyMuPDF
- Engineered two-stage semantic job matcher combining sentence-transformer 
  bi-encoder retrieval with category-weighted reranking; reduced pipeline latency 
  by 95% (75s → 2s) through offline vector pre-computation
- Built full-stack Flask application with async processing, confidence scoring and 
  semantic match explanations; deployed to production on Render with Gunicorn
- Developed work credits generator using custom LLM prompts to categorise and 
  surface candidates' creative industry experience as a portfolio PDF

## Technical Skills

**Languages:** Python, C/C++, Java, Go, Scala, JavaScript, SQL, Standard ML  

**Systems & Tools:** Docker, Bash, AFL++, LLVM, ASan/UBSan, asyncio, NumPy, Redis, Prometheus, CMake

**Frameworks:** Flask, Django, React, FastAPI

## Contact

[LinkedIn](https://www.linkedin.com/in/aravinth-kaneshalingam) · 
[Email](mailto:aravinth_kanesh@hotmail.com)
