# Colin K Thomas

**Backend / Systems Engineering | Python | FastAPI | PostgreSQL | Redis**

Computer Science student at VIT Chennai focused on backend systems, APIs, data-intensive services, concurrency, and distributed systems.

I build backend software with an emphasis on clear service boundaries, asynchronous processing, database correctness, observability, testing, and measurable performance.

## Selected projects

### [FleetOps](https://github.com/colin-110/robot-fleet-platform)
Real-time robot fleet monitoring and control platform using FastAPI, PostgreSQL, Redis Streams, and WebSockets.

- Decoupled telemetry ingestion from PostgreSQL persistence with Redis Streams and worker-based batching
- Built bounded WebSocket fan-out so slow clients do not block the fleet
- Implemented idempotent command handling with atomic compare-and-set updates
- Added JWT roles, short-lived WebSocket console tickets, structured logging, and Prometheus/Grafana
- Measured telemetry ingest p99 from **1,271 ms to 158 ms**

### [Lumen](https://github.com/colin-110/lumen)
Self-hosted document assistant focused on retrieval quality and backend infrastructure.

- Hybrid dense + BM25 retrieval with Reciprocal Rank Fusion and cross-encoder reranking
- Redis/Qdrant semantic caching and SSE response streaming
- Celery-based asynchronous document ingestion with OCR fallback
- JWT authentication and organization-level document isolation
- Retrieval evaluation with Recall@k, MRR, and NDCG

### [Meeting Summarizer](https://github.com/colin-110/meeting-summarizer)
FastAPI service for asynchronous meeting transcription and structured analysis.

- Background audio processing with FastAPI
- Content-hash deduplication and input validation
- Explicit handling of provider failures, retries, malformed output, and server restarts
- Golden-dataset evaluation for transcription and extraction quality
- Automated testing with GitHub Actions

## What I work with

**Backend:** Python, FastAPI, SQLAlchemy, REST APIs  
**Data:** PostgreSQL, SQLite, Redis  
**Systems:** asynchronous workers, queues/streams, WebSockets, caching, concurrency  
**Infrastructure:** Docker, GitHub Actions, Prometheus, Grafana, AWS  
**Other:** C++, Java, React

## Links

[LinkedIn](https://www.linkedin.com/in/colinkthomas) · [LeetCode](https://leetcode.com/u/OKTRBpaERN) · [Email](mailto:colinkthomas110@gmail.com)
