# Colin K Thomas

**Computer Science @ VIT Chennai · Backend & Software Engineering**

I build backend services in Python and FastAPI, deploy them on AWS, and test how they behave under load and failure. Every project below has a working deployment or a reproducible local setup, plus documented measurements.

[LinkedIn](https://www.linkedin.com/in/colinkthomas) · [LeetCode](https://leetcode.com/u/OKTRBpaERN)

---

## Projects

### [FleetOps](https://github.com/colin-110/robot-fleet-platform) · [Live demo](https://robot-fleet-platform.vercel.app)
Real-time robot fleet monitoring and control platform.
`FastAPI` `MQTT` `TimescaleDB` `WebSockets` `React` `Docker` `AWS Lightsail`

- Telemetry is acknowledged only after it is committed, and each robot keeps an on-disk outbox. In chaos tests, killing the robots, the API or the broker mid-stream still stored every reading exactly once.
- Robots and server run the same predictor, so robots send data only when values drift past a set tolerance. This cut message volume by 55%. Compact CBOR encoding uses 20–35 bytes per reading, compared with about 450 bytes as JSON.
- Handles 1,000 simulated robots at about 40% of one CPU core. The project has about 925 tests across the backend, the robot agent and the dashboard.

### [Lumen](https://github.com/colin-110/lumen) · [Live demo](https://lumen-three-nu.vercel.app)
Self-hosted document assistant with hybrid retrieval and cited, streamed answers.
`FastAPI` `PostgreSQL` `Redis` `Qdrant` `Celery` `Next.js` `CloudFormation`

- Hybrid retrieval combines dense search and BM25 using Reciprocal Rank Fusion, followed by ColBERT late-interaction reranking.
- On a fixed evaluation set, it reaches 98% Recall@5 and 0.98 MRR with reranking in 25 ms. A cross-encoder took 1,222 ms.
- Includes asynchronous idempotent ingestion, semantic caching, tenant isolation, multi-provider LLM fallback and checks that verify the numbers in each answer against the cited sources.

### [Meeting Summarizer](https://github.com/colin-110/meeting-summarizer) · [Live app](https://meeting-summarizer-recorder.vercel.app)
Produces transcripts, summaries, decisions and action items from recorded or uploaded meetings.
`FastAPI` `SQLite` `Whisper` `ffmpeg` `GitHub Actions` `AWS Lightsail`

- Uses a durable job queue on SQLite with leases and heartbeats. In tests with concurrent worker processes, every job ran exactly once.
- Live recordings are transcribed and summarized during the meeting, so notes are ready 14.8 s after stopping instead of 65.7 s.
- Trimming silence reduced the audio sent for transcription by 33% and kept timestamps within about 1 s. A shared token budget with model fallback keeps the app working within free-tier API limits. Runs on a $5/month server.

### [Fact Knowledge Layer](https://github.com/colin-110/fact-knowledge-layer)
Extracts facts from PDFs, links each one to its source and checks documents against each other for contradictions.
`FastAPI` `SQLite FTS5` `Chroma` `PyMuPDF` `LLM APIs`

- Every fact links to its page, quote and position in the source document. Deterministic code normalizes currencies, periods and units so that comparisons are reproducible.
- Matching relationships between documents are resolved by rules first. Only ambiguous pairs are sent to an LLM.
- A free text-layout pass handled 17 of 20 chart-heavy pages without paid vision calls. The project has 120 tests that run in CI on every push.

### Other work
- [Papercut](https://github.com/colin-110/papercut): converts between images and PDFs entirely in the browser, without uploading files (TypeScript)
- [PID-free stabilization robot](https://github.com/colin-110/custom-pid-free-stabilization-robot): an ESP32 robot with adaptive control and dual-core FreeRTOS tasks (C++)
- [Robot kinematics simulator](https://github.com/colin-110/robot-kinematics-ik-simulator): forward and inverse kinematics for a 6-DOF robot arm, with a 3D visualization (Python)
- [Algal bloom forecasting](https://github.com/colin-110/hab_project_ml): an XGBoost model that predicts harmful algal blooms from satellite and climate data (Python)

---

## Skills

**Languages:** Python, C++, Java, SQL, TypeScript/JavaScript

**Backend:** FastAPI, REST, WebSockets, SSE, MQTT, Celery, job queues, caching, rate limiting

**Databases:** PostgreSQL, TimescaleDB, SQLite, Redis, Qdrant, Chroma

**Retrieval & LLMs:** RAG, hybrid search (dense + BM25), reranking, retrieval evaluation

**Infrastructure:** Docker, AWS (EC2, Lightsail, CloudFormation, SSM), GitHub Actions, Prometheus, Grafana, Vercel

**Frontend & Embedded:** React, Next.js, ESP32, FreeRTOS
