# Awesome-Multi-Model-Database

# Top Multi-Model Database Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Unified Data Models, ACID Transactions & Hybrid Query Languages*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Multi-Model Databases**. These tools support multiple data models — document, graph, key-value, vector, time-series, and relational — within a single engine and query language, eliminating the need to stitch together separate databases for different workloads.

**Examples** include SurrealDB, ArangoDB, OrientDB, Couchbase, MarkLogic, MongoDB, Azure Cosmos DB, and Amazon DynamoDB (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, unified query languages, and transparent multi-model architecture — ideal for teams wanting to consolidate their data stack without losing the flexibility to model data the way each application needs.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **MongoDB Atlas** — Managed version of the leading document database. **MongoDB tops the document store ranking on DB-Engines** but is primarily a document model — multi-model capabilities are limited compared to true multi-model engines. **Best for teams wanting the largest document ecosystem** rather than unified multi-model access.

- **Amazon DynamoDB** — Fully managed key-value and document store with single-digit millisecond latency. **Best for AWS-native teams** with simple, stable access patterns.

- **Couchbase Capella** — Managed Couchbase with **multi-model data access** including key-value, JSON document, SQL++, full-text search, vector search, and eventing services [citation:4]. **Best for enterprises wanting multi-model access** with a mature, memory-first architecture.

- **Azure Cosmos DB** — Globally distributed multi-model database with document, key-value, graph, and wide-column APIs. **Best for Azure-native applications** needing multi-region distribution and multiple data models.

## Open-Source GitHub Projects

- **[SurrealDB](https://github.com/surrealdb/surrealdb)**  
  **The scalable document-graph database that unifies six data models in one ACID engine** — **supports document, graph, vector, time-series, relational, and geospatial data** natively, not as bolt-on layers [citation:1][citation:7]. **SurrealQL** is a single SQL-style query language handling graph traversals (`RELATE`, `->`), vector KNN search, `LIVE SELECT` real-time subscriptions, and hybrid queries combining document, graph, and relational patterns in one statement [citation:1]. **Built-in authentication and row-level security** live in the database rather than a sidecar service [citation:7]. **Single binary deploys anywhere** — in-memory, embedded, edge, WASM, or cloud [citation:7]. **Proven in production**: Saks Fifth Avenue uses it for 1.5 million AI-driven product recommendations weekly; Tencent processes millions of events per second [citation:13]. **Best for teams wanting true multi-model consolidation** with one engine, one query language, and one transaction across all data models.

- **[ArangoDB](https://github.com/arangodb/arangodb)**  
  **The graph-native multi-model foundation for enterprise applications** — **unifies graph, document, key-value, vector, and full-text search in one engine** with **AQL (ArangoDB Query Language)** for querying all models [citation:2][citation:8]. **AQL supports graph traversals, joins, geo-spatial queries, full-text search with BM25/TF-IDF ranking, and vector similarity in a single query** [citation:2]. **ACID transactions** for single-server deployments; cluster deployments support fully ACID single-document operations [citation:2]. **SmartGraphs** use value-based sharding to co-locate connected data for efficient deep traversals; **SatelliteCollections** replicate reference data to every node [citation:8]. **Enterprise features** include RBAC, provenance/lineage, GraphML service (GraphSAGE), and in-engine analytics (PageRank, centrality, community detection) [citation:8]. **Deploys as fully managed (AMP), on-premises, air-gapped, or hybrid** with feature parity [citation:8]. **Best for enterprises needing graph-native multi-model** with strong governance and AI-ready retrieval capabilities.

- **[OrientDB](https://github.com/orientechnologies/orientdb)**  
  **The original true multi-model database** — **supports graph, document, key-value, and object models** with the engine built from the ground up for all four, not an API layer over a single model [citation:3]. **Documents have native `LINK` relationships** that are automatically resolved on fetch — unlike MongoDB or CouchDB where the developer handles relationships [citation:3]. **Graph model uses property graph** with vertices and edges supporting custom properties [citation:3]. **SQL-like query language extended for graph traversal**, plus Gremlin support [citation:15]. **Schema-less, schema-full, and schema-mixed modes** [citation:15]. **Note**: OrientDB's community edition development has slowed — evaluate maintenance activity before new adoption. **Best for teams wanting a proven multi-model engine** with document and graph integration.

- **[Couchbase Server](https://github.com/couchbase/couchbase)**  
  **The original multi-model NoSQL database** — **combines key-value speed with JSON document flexibility**, with additional access methods including SQL++ (formerly N1QL), Full-Text Search, Vector Search, Eventing, and Analytics [citation:4]. **Memory-first architecture** caches most-used data and indexes in memory for low-latency reads [citation:4]. **Workload isolation** via independent services (Data, Query, Index, Search, Analytics, Eventing) that can scale separately [citation:4]. **Community Edition** source is available under **BSL 1.1** (converts to Apache 2.0 after four years) [citation:4]. **Best for enterprises wanting multi-model access** with a mature, memory-first architecture and workload isolation.

- **[MarkLogic](https://github.com/marklogic/marklogic-server)**  
  **The enterprise multi-model database with built-in search** — **native storage for documents (JSON/XML), text, graph (RDF), relational views, geospatial, and binary formats** [citation:5]. **Universal Index** provides search-engine capabilities built into the database core — data is indexed at ingest for immediate querying [citation:11]. **ACID transactions, bitemporal, HA/DR, and petabyte scalability** [citation:5]. **Query interfaces include JavaScript, XQuery, SPARQL, SQL, REST API, Java API, Node.js API, and Optic API** [citation:11]. **Best for enterprises needing multi-model with built-in search** across complex, heterogeneous data.

### Additional Strong Open-Source Options

- **Fauna** — Web-native multi-model database with document, graph, relational, and time-series support. **DB-Engines lists it as a document store and graph DBMS** [citation:6][citation:12]. Commercial cloud-only service. Best for serverless applications wanting multi-model access without infrastructure.
- **OrientDB (Object Model)** — In addition to graph/document/key-value, OrientDB also supports the object model, making it a four-model engine [citation:3][citation:15].

**Frameworks for building custom systems**: Combine **SurrealDB** for the most complete single-engine multi-model consolidation with unified SurrealQL and ACID transactions across all models, **ArangoDB** for graph-native enterprise multi-model with strong governance and AI-ready retrieval, **OrientDB** for a proven document-plus-graph engine, **Couchbase** for memory-first multi-model with workload isolation, and **MarkLogic** for enterprise multi-model with built-in search — to build a data layer tailored to your model mix, governance requirements, and query complexity.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Multi-model databases differ significantly in model coverage, query language unification, and licensing. **SurrealDB unifies six models in one ACID engine** with a single query language [citation:7], but its ecosystem is younger than established alternatives. **ArangoDB is graph-native** with AQL spanning all models [citation:2], but cluster multi-document ACID requires OneShard [citation:2]. **OrientDB's community development has slowed** — evaluate before new adoption. **Couchbase Community is BSL 1.1** (not OSI-approved, converts to Apache 2.0 after four years) [citation:4]. **MarkLogic is enterprise-focused** with built-in search [citation:5]. **"Multi-model" varies** — some databases support multiple models natively in the engine, while others layer APIs over a single storage model [citation:3].
- Self-hosted open-source solutions require proper cluster sizing, replication configuration, and awareness that ACID guarantees may differ between single-server and cluster deployments.

---

**Made for backend engineers and architects consolidating data stacks with multi-model databases.**
Let's make multi-model databases more open, unified, and workload-appropriate.
