# Colin K Thomas

**Backend / Systems Engineering | Python | FastAPI | PostgreSQL | Redis**

Computer Science student at VIT Chennai building backend systems, data-intensive services, and real-time applications.

I care about:
- asynchronous processing and concurrency
- reliable APIs and background workers
- database correctness and caching
- observability, testing, and measurable performance

## Featured projects

### [FleetOps](https://github.com/colin-110/robot-fleet-platform)
**Real-time robot fleet monitoring and control**

FastAPI + Redis Streams + PostgreSQL + WebSockets

- Decoupled telemetry ingestion from database persistence with asynchronous workers
- Added bounded WebSocket fan-out so slow clients do not block the fleet
- Implemented idempotent command handling, RBAC, structured logging, and correlation IDs
- Measured telemetry ingest p99 from **1,271 ms to 158 ms**
- Load-tested to about **2,000 concurrent WebSocket clients** and **15K–18K messages/s** on a single node

### [Lumen](https://github.com/colin-110/lumen)
**Self-hosted document retrieval and RAG platform**

FastAPI + PostgreSQL + Redis + Qdrant + Celery + LLM APIs

- Hybrid dense + BM25 retrieval with Reciprocal Rank Fusion and cross-encoder reranking
- Semantic caching and SSE streaming for lower latency
- Asynchronous document ingestion with OCR fallback
- Organization-level document isolation and multi-provider LLM fallback
- Retrieval evaluation with Recall@k, MRR, and NDCG

### [Meeting Summarizer](https://github.com/colin-110/meeting-summarizer)
**Asynchronous meeting intelligence pipeline**

FastAPI + Whisper + LLMs + Pytest + GitHub Actions

- Background processing for transcription and structured extraction
- Content-hash deduplication and layered file validation
- Explicit handling of provider failures, retries, malformed outputs, and restarts
- Reproducible evaluation pipeline for transcription and extraction quality
- Documented evaluation results including **~1.8% WER**, **18/18** decision recall, and **21/21** action-item recall

## Technical focus

**Languages:** Python, C++, Java, SQL

**Backend:** FastAPI, REST APIs, WebSockets, SQLAlchemy

**Data:** PostgreSQL, Redis, Qdrant, SQLite

**Systems:** async workers, queues/streams, caching, concurrency

**Infrastructure:** Docker, AWS, GitHub Actions, Prometheus, Grafana

**AI:** LLM APIs, RAG, hybrid retrieval, reranking

## Links

[LinkedIn](https://www.linkedin.com/in/colinkthomas) · [LeetCode](https://leetcode.com/u/OKTRBpaERN)
