# Bee Intelligence

Bee Intelligence is an AI intelligence and future robotics platform for agriculture, starting with beekeeping.

This public showcase is intentionally sanitized. It is designed for investors, accelerators, technical founders, and Project Europe-style reviewers who need to understand that the project is real and technically substantial without receiving proprietary source code, prompts, schemas, credentials, private data, or Git history.

## Short Description

Bee Intelligence is building the intelligence layer for agricultural operations. Beekeeping is the first proving ground because hives are biologically complex, economically important, sensor-friendly, and operationally constrained: good decisions depend on weather, colony condition, disease risk, hive history, expert knowledge, and local observations.

The long-term progression is:

```text
knowledge -> sensing -> understanding -> decisions -> physical action
```

The current system focuses on knowledge, sensing, understanding, and evidence-grounded decision support. Robotics and actuation are future layers, not current validated functionality.

## Problem

Agricultural operators often have fragmented information:

- scientific and practical knowledge in documents
- field observations in notes or inspections
- sensor telemetry in separate dashboards
- operational history in spreadsheets or memory
- AI tools that can answer generally but cannot reliably ground answers in local evidence

For beekeeping, this fragmentation matters. A hive-specific recommendation should not be invented from generic beekeeping knowledge. It should be tied to the user's hive records, readings, inspections, alerts, and evidence sources.

## Why Beekeeping First

Beekeeping is a strong first vertical because it combines:

- high biological complexity in a compact physical system
- measurable signals such as temperature, humidity, and acoustic features
- repeated operational workflows such as inspections, treatments, feeding, and equipment changes
- meaningful expert knowledge and historical documentation
- a natural path from decision support toward carefully bounded physical assistance

The goal is not to stop at a beekeeping chatbot. The goal is to prove an agriculture intelligence layer that can later generalize to other crops, livestock, and controlled-environment systems.

## What Currently Works

The private repository contains implemented and tested foundations for:

- document ingestion, parsing, chunking, validation, reprocessing, repair, and replay
- vector retrieval using Chroma as a derived index
- PostgreSQL-backed source-of-truth storage for documents, chunks, jobs, operational data, sessions, traces, and knowledge graph provenance
- knowledge graph extraction/enrichment with evidence linked back to source material
- deterministic retrieval-augmented answer generation with citations, grounding checks, fallback behavior, session handling, and trace persistence
- apiary and hive records
- logical sensors, physical devices, device assignment history, normalized readings, raw payload preservation, and alert evaluation
- inspections, treatments, feeding, equipment events, hive timelines, alert rules, and alert lifecycle state
- authentication, sessions, explicit permissions, same-origin checks, audit logging, and production safety validators
- a React product shell for apiaries, devices/readings, inspections/alerts, the grounded assistant, knowledge tools, and operator administration
- local Docker Compose runtime with API, worker, application PostgreSQL, identity PostgreSQL, and Chroma
- production-oriented Docker and migration scaffolding
- automated backend, frontend, architecture, migration, security, retrieval, sensor, and release-readiness tests

## Real-World Sensor Integration

The project includes a physical telemetry path for Raspberry Pi Pico-based apiary hardware using temperature, humidity, and acoustic measurements. The checked-in firmware documents tested DHT22 and analog microphone wiring, sampling behavior, buffering, clock synchronization, and upload retry behavior.

The backend supports physical-device telemetry by separating raw payload receipt, parsed payloads, normalized readings, stored readings, and alert evaluation. Device credentials are hashed, physical devices can move between hives over time, and readings preserve both device observation time and backend receipt time.

The public examples in this package use synthetic values only. The project has not yet been validated with sensors installed inside a live beehive.

## Evidence-Grounded Reasoning

The assistant is designed to separate general agricultural education from operational hive claims.

For general beekeeping education, it can use retrieved knowledge sources and clearly cite supporting evidence. For concrete claims about a user's hive, it must rely on user-owned data such as readings, hive records, inspections, alerts, and traceable evidence. If that evidence is insufficient, the correct behavior is to say so instead of inventing a diagnosis.

## Current Validation Status

Implemented/tested in the repository:

- ingestion, chunk validation, KG persistence, vector retrieval, and replay/repair paths
- deterministic RAG behavior, citations, grounding filters, abstention behavior, and trace persistence
- sensor normalization, raw payload preservation, duplicate handling, device assignment history, tenant isolation, invalid payload handling, and time filtering
- alert rules, alert deduplication, alert evidence, acknowledgement, resolution, and backend-owned threshold evaluation
- frontend product shell and workflows for workspace, devices/readings, operations/alerts, assistant, knowledge, and administration
- production-safety defaults such as secure-cookie requirements, origin controls, secret redaction, and hardcoded-secret scanning support

Tested with physical telemetry support:

- firmware and receiver support exist for real sensor hardware and physical telemetry signals
- public sample data is synthetic and intentionally does not disclose private raw measurements
- no repository evidence supports a claim of live in-hive sensor deployment yet

Not yet proven:

- long-duration monitoring inside live hives
- scientific or peer-reviewed validation of predictions or recommendations
- robotic actuation
- autonomous physical intervention
- large-scale commercial deployment

## Long-Term Vision

The long-term vision is an agricultural intelligence and robotics platform:

1. ingest trusted agricultural knowledge
2. connect real-world telemetry and field observations
3. understand local state through evidence-grounded reasoning
4. support human decisions with traceable recommendations
5. validate decision support with domain experts and field trials
6. introduce robotic components for narrow, safe tasks
7. eventually close the loop from sensing to reasoning to supervised physical action

Beekeeping is the first system where this loop can be built and validated carefully.

## Technology Overview

Verified technologies and components in the private repository include:

- Python and FastAPI for the backend API
- PostgreSQL for durable operational, document, agent, and provenance state
- a separate PostgreSQL identity database for users and sessions
- Chroma for derived vector retrieval
- a worker/offline plane for ingestion, reindexing, KG work, replay, and maintenance
- Docker and Docker Compose for local runtime and production-oriented scaffolding
- React and Vite for the authenticated product shell
- firmware support for Pico-based telemetry hardware
- pytest, Node tests, Playwright tests, migration verification, Chroma rebuild checks, and secret scanning scripts

## Current Stage

Bee Intelligence is a private, technically functional prototype and platform foundation. It is not presented here as a public SaaS deployment, a certified agricultural diagnostic system, or a validated robotics product.

The current value is the implemented intelligence backbone: ingestion, retrieval, graph-backed evidence, operational data modeling, sensor integration, and a product UI foundation. The next major proof points are live in-hive deployment, longer field validation, richer sensing, expert evaluation, and eventually narrowly scoped robotic assistance.
