# Colin K Thomas

**Computer Science Student @ VIT Chennai | Software Engineering | Python | C++**

I build software systems and applications across APIs, data, AI, and infrastructure, with a focus on solving practical engineering problems, writing reliable software, and measuring the impact of technical decisions.

## Featured projects

### [FleetOps](https://github.com/colin-110/robot-fleet-platform)
**Real-time robot fleet monitoring and control platform**

FastAPI + Redis Streams + PostgreSQL + WebSockets

- Designed an asynchronous telemetry pipeline that decouples ingestion from database persistence
- Built real-time fleet state updates and command dispatch with bounded WebSocket fan-out
- Added idempotent command handling, RBAC, structured logging, correlation IDs, and operational metrics
- Reduced measured telemetry-ingest p99 from **1,271 ms to 158 ms**
- Load-tested to about **2,000 concurrent WebSocket clients** and **15K–18K messages/s** on a single node

### [Lumen](https://github.com/colin-110/lumen)
**Self-hosted document retrieval and RAG platform**

FastAPI + PostgreSQL + Redis + Qdrant + Celery + LLM APIs

- Built an end-to-end document retrieval and question-answering system with asynchronous ingestion
- Combined dense retrieval, BM25, Reciprocal Rank Fusion, and cross-encoder reranking
- Added semantic caching, SSE streaming, tenant isolation, and multi-provider LLM fallback
- Built retrieval evaluation around Recall@k, MRR, and NDCG
- Investigated a cache failure found through load testing and reduced repeat-query latency from **15.4 s to 44 ms**

### [Meeting Summarizer](https://github.com/colin-110/meeting-summarizer)
**Asynchronous meeting intelligence pipeline**

FastAPI + Whisper + LLMs + Pytest + GitHub Actions

- Built a processing pipeline for transcripts, summaries, decisions, action items, and open questions
- Added content-hash deduplication, layered file validation, structured-output validation, and retry handling
- Designed recovery for provider failures and interrupted processing
- Built a reproducible evaluation pipeline for transcription and extraction quality
- Documented results including **~1.8% WER**, **18/18** decision recall, and **21/21** action-item recall

## What I Work With

**Languages:** Python, C++, Java, SQL

**Software Engineering:** APIs, application architecture, testing, concurrency, Git

**Systems & Data:** FastAPI, REST, WebSockets, PostgreSQL, Redis, Qdrant, SQLite, async workers, queues, caching

**AI:** LLM APIs, RAG, hybrid retrieval, reranking

**Infrastructure:** Docker, AWS, GitHub Actions, Prometheus, Grafana

## Links

[LinkedIn](https://www.linkedin.com/in/colinkthomas) · [LeetCode](https://leetcode.com/u/OKTRBpaERN)
