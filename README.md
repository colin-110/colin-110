## Colin K Thomas

Third-year Computer Science student at VIT Chennai, focused on backend and
distributed systems engineering.

### What I'm building

**[Distributed Fleet Telemetry Platform](https://github.com/colin-110/robot-fleet-platform)**

A real-time telemetry ingestion and monitoring platform. Redis Streams consumer
groups handle asynchronous ingestion so HTTP latency stays independent of
database I/O; a WebSocket fan-out layer with bounded per-client queues and
drop-oldest backpressure delivers live updates; command dispatch is idempotent
via an explicit state machine and atomic row-level claims.

Load-tested to roughly 2,000 concurrent clients at up to 18,000 messages per
second with over 99% delivery. Deployed on AWS behind CloudFront, with GitHub
Actions running 24 tests against a live PostgreSQL service.

[Live demo](https://d14zlr0p01xdp8.cloudfront.net) &middot;
[Source](https://github.com/colin-110/robot-fleet-platform)

### Tech

Python &middot; FastAPI &middot; PostgreSQL &middot; Redis &middot; WebSockets
&middot; React &middot; Docker &middot; AWS &middot; GitHub Actions

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/colinkthomas) &middot;
colinkthomas110@gmail.com
