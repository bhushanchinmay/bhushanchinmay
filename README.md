# Chinmay Bhushan

I build backend services with Java and Spring Boot. My work covers APIs, subscription workflows, service integrations, asynchronous processing, and data consistency.

In my personal projects, I focus on concurrent updates, partial failures, reliable message delivery, and database design.

## Selected projects

🤖 Built with AI assistance from Codex or Claude.

### [Workflow State Tracker](https://github.com/bhushanchinmay/workflow-state-tracker) 🤖

A Spring Boot service that tracks workflow events and acknowledgements from downstream services.

- Uses transactional row locks to coordinate acknowledgements and overdue failure handling.
- Records terminal state changes and outbox events in the same PostgreSQL transaction.
- Publishes events to Kafka with retries, database leases, and dead-letter handling.
- Includes Flyway migrations, Testcontainers integration tests, request IDs, and application metrics.

**Design focus:** State transitions, concurrent updates, and recovery from partial failures. Delivery is at least once, so consumers must handle duplicate events.

### [Book Search](https://github.com/bhushanchinmay/book-search) 🤖

A Java and Spring Boot API for searching a book catalogue with PostgreSQL.

- Uses full-text search, GIN indexes, and relevance ranking.
- Keeps book data and its search index in one database.
- Imports data through a Java batch importer.
- Includes input validation, bounded results, and PostgreSQL integration tests.

**Design focus:** Search relevance, relational modelling, and data ingestion without a separate search service.

### [ClipSync](https://github.com/bhushanchinmay/clipsync) 🤖

A local tool that transfers clipboard text from macOS to Android over Wi-Fi.

- Uses mDNS to discover devices and TCP to transfer text.
- Defines message boundaries with length-prefixed framing.
- Sends to connected clients concurrently and disconnects stalled clients after a timeout.
- Combines a Python background service with a Kotlin Android application.

**Design focus:** Network protocols, slow-client handling, and platform constraints.

### [RouteSpec](https://github.com/bhushanchinmay/routespec)

A NestJS toolkit for API versioning, response formatting, and route metadata.

- Resolves API versions from URL paths or request headers.
- Separates version-specific responses from controller logic.
- Discovers route metadata through decorators and runtime inspection.
- Includes OpenAPI documentation, unit tests, and end-to-end tests.

**Design focus:** API compatibility, separation of responsibilities, and testable request handling.

## Technical focus

Java · Spring Boot · PostgreSQL · Kafka · Redis · REST APIs · Docker · Kubernetes

I am interested in backend roles where I can own service design, implementation, testing, and operational reliability.
