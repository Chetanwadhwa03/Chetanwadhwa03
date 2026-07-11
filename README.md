# Chetan Wadhwa

Software Engineer focused on backend architecture and real-time systems. I work primarily with Node.js, Redis, and WebSockets — designing decoupled, event-driven services that stay responsive under concurrent load, and RAG pipelines that handle asynchronous, resource-heavy workloads without blocking the main thread.

BASED IN INDIA

[LinkedIn](https://www.linkedin.com/in/chetan-wadhwa-9174051a3/) · [chetanwadhwa03@gmail.com](mailto:chetanwadhwa03@gmail.com)

---

## Projects

### [CoreWire](https://corewire.vercel.app/) — Real-Time Collaborative Code Workspace
A browser-based IDE built on native WebSockets, supporting live multi-user code editing, persistent rooms, and in-editor chat.

- Engineered zero-latency code synchronization across concurrent clients using native WebSockets rather than a managed real-time layer, giving direct control over connection state and message routing.
- Diagnosed and fixed a recurring infinite broadcast loop (the "ping-pong" bug) by redesigning update propagation around a `useRef`-based interception layer between the Monaco Editor and the socket connection.
- Locked socket sessions to authenticated user IDs to prevent chat spoofing and correctly handle late-joiner state syncing.
- Integrated the JDoodle Compiler API for secure, sandboxed code execution, and reduced redundant database writes significantly with a custom debounce-based autosave.

### C-Flux — AI-Powered Document Assistant *(in progress)*
An event-driven RAG backend built to separate request handling from long-running AI workloads.

- Architected a decoupled backend that keeps stateless REST APIs separate from a stateful WebSocket layer, routing long-running LLM work through a background worker to avoid blocking request handling.
- Built a Redis-queue-backed ingestion pipeline for PDF parsing and embedding generation, using Google Gemini for 3072-dimensional embeddings and Pinecone for semantic retrieval.
- Designed the ingestion worker to handle upstream API rate limits gracefully rather than failing on burst load.
- Implemented Redis Pub/Sub to broadcast streaming AI responses to the correct concurrent user, enabling the architecture to scale horizontally across workers.

### [Tunesta](https://tunesta.netlify.app/) — Cloud-Native Personal Music Library
A media vault for personal audio storage with JWT-based identity management ensuring complete data isolation between users, backed by Cloudinary for persistent cloud storage.

---

## Technical Skills

**Languages** — C++, JavaScript (ES6+), TypeScript, SQL

**Backend & Architecture** — Node.js, Express.js, WebSockets, REST APIs, JWT, Event-Driven Systems, Microservices

**Data & AI Infra** — Redis, MongoDB, Pinecone, MySQL, Google Gemini

**Frontend** — React (Vite), TypeScript, Tailwind CSS

**Infra & Tooling** — Railway, Render, Vercel, Git, Postman

---

*Currently deepening my understanding of distributed systems design — queueing, backpressure, and horizontal scaling patterns for real-time workloads.*
