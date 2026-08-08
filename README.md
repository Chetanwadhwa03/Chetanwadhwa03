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


### GEO Auditor — Generative Engine Optimization Engine
A diagnostic web application that evaluates and scores websites for Generative Engine Optimization (GEO). It bridges the gap between traditional SEO and AI search engines by auditing on-page semantic structures, AI crawler permissions, client-rendering dependencies, and LLM brand visibility.

- Engineered a 100-point scoring algorithm evaluating 4 core technical pillars: Content Structure (30 pts), Crawlability (35 pts), LLM Access & Citation Visibility (20 pts), and Rendering/SSR (15 pts).
- Built live DOM & crawler parsers in Node.js/Express to fetch and inspect live `robots.txt` AI agent directives (`GPTBot`, `ClaudeBot`, `CCBot`), `sitemap.xml` availability, H1–H6 heading hierarchies, and `JSON-LD` Schema.org entity markup.


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
