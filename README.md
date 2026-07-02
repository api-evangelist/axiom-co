# Axiom (axiom-co)

Axiom is a log management, event data, and observability platform that ingests, stores, and queries large volumes of logs, traces, and events at low cost. Data is loaded into datasets and queried with the Axiom Processing Language (APL). The REST API (base `https://api.axiom.co` for the US region, `https://api.eu.axiom.co` for the EU region) exposes ingest, APL query, datasets, fields, annotations, monitors, notifiers, dashboards, virtual fields, starred queries, API tokens, users, and organizations, with v1 and v2 endpoint families and Bearer token authentication.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/axiom-co/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/axiom-co/refs/heads/main/apis.yml)

## Tags

- Observability
- Log Management
- Event Data
- Logs
- Tracing
- Analytics
- APL

## Timestamps

- **Created:** 2026-07-02
- **Modified:** 2026-07-02

## APIs

### Axiom Ingest API

Send logs, traces, and events into an Axiom dataset. POST JSON, NDJSON, or CSV payloads to a dataset ingest endpoint, with optional content encoding and timestamp field configuration. A lower-latency edge ingest endpoint is also available.

- **Human URL:** [https://axiom.co/docs/restapi/ingest](https://axiom.co/docs/restapi/ingest)
- **Base URL:** `https://api.axiom.co/v1`

#### Tags

- Ingest
- Logs
- Events

#### Properties

- [Documentation](https://axiom.co/docs/restapi/ingest)
- [API Reference](https://axiom.co/docs/restapi/endpoints/ingestIntoDataset)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Query API (APL)

Run Axiom Processing Language (APL) queries across one or more datasets. POST an APL query with optional start/end times and receive tabular or legacy results. A legacy per-dataset structured query endpoint is also supported.

- **Human URL:** [https://axiom.co/docs/restapi/query](https://axiom.co/docs/restapi/query)
- **Base URL:** `https://api.axiom.co/v1`

#### Tags

- Query
- APL
- Analytics

#### Properties

- [Documentation](https://axiom.co/docs/restapi/query)
- [API Reference](https://axiom.co/docs/restapi/endpoints/queryApl)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Datasets API

Create, list, retrieve, update, and delete datasets - the containers that store ingested event data - plus trim and vacuum operations to manage retention and reclaim storage.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getDatasets](https://axiom.co/docs/restapi/endpoints/getDatasets)
- **Base URL:** `https://api.axiom.co/v1`

#### Tags

- Datasets
- Storage
- Management

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getDatasets)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Fields API

Inspect and annotate the fields of a dataset - list the discovered schema for a dataset and read or update per-field metadata such as description, unit, and hidden state.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getFieldsForDataset](https://axiom.co/docs/restapi/endpoints/getFieldsForDataset)
- **Base URL:** `https://api.axiom.co/v1`

#### Tags

- Fields
- Schema
- Datasets

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getFieldsForDataset)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Annotations API

Create, list, retrieve, update, and delete annotations that mark deployments, incidents, and other events on your dashboards and charts, scoped to datasets and time ranges.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getAnnotations](https://axiom.co/docs/restapi/endpoints/getAnnotations)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Annotations
- Events
- Context

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getAnnotations)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Monitors API

Manage monitors - threshold and match alerts backed by APL queries that watch your data and fire notifications. Create, list, retrieve, update, and delete monitors and read monitor run history.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getMonitors](https://axiom.co/docs/restapi/endpoints/getMonitors)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Monitors
- Alerts
- Alerting

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getMonitors)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Notifiers API

Manage notifiers - the notification channels (email, Slack, PagerDuty, webhooks, and more) that monitors dispatch alerts through. Create, list, retrieve, update, and delete notifier configurations.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getNotifiers](https://axiom.co/docs/restapi/endpoints/getNotifiers)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Notifiers
- Notifications
- Alerting

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getNotifiers)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Dashboards API

Create, list, retrieve, update, patch, and delete dashboards - the collections of charts and APL-backed visualizations that present your event data, with pagination support.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getDashboards](https://axiom.co/docs/restapi/endpoints/getDashboards)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Dashboards
- Visualization
- Analytics

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getDashboards)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Virtual Fields API

Define virtual fields - derived fields computed from an APL expression at query time for a dataset. Create, list, retrieve, update, and delete virtual fields scoped to a dataset.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getVirtualFields](https://axiom.co/docs/restapi/endpoints/getVirtualFields)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Virtual Fields
- Derived Fields
- Schema

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getVirtualFields)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Starred Queries API

Manage starred (saved) queries - reusable APL queries saved for a dataset and shared across a team. Create, list, retrieve, update, and delete starred queries.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints](https://axiom.co/docs/restapi/endpoints)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Starred Queries
- Saved Queries
- APL

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom API Tokens API

Manage API tokens - scoped credentials (basic ingest-only or advanced query/manage) used to authenticate API requests. Create, list, retrieve, regenerate, and delete tokens. Personal Access Tokens require an `x-axiom-org-id` header.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getTokens](https://axiom.co/docs/restapi/endpoints/getTokens)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Tokens
- Authentication
- Security

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getTokens)
- [Documentation](https://axiom.co/docs/reference/tokens)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Users API

Retrieve the currently authenticated user, list organization members, update roles, and remove members. The current-user lookup is also available on the v1 endpoint family.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints/getCurrentUser](https://axiom.co/docs/restapi/endpoints/getCurrentUser)
- **Base URL:** `https://api.axiom.co/v2`

#### Tags

- Users
- Members
- Administration

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints/getCurrentUser)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Axiom Organizations API

Read and manage organization settings - retrieve the organizations a caller belongs to, get an organization by ID, and update organization-level configuration.

- **Human URL:** [https://axiom.co/docs/restapi/endpoints](https://axiom.co/docs/restapi/endpoints)
- **Base URL:** `https://api.axiom.co/v1`

#### Tags

- Organizations
- Account
- Administration

#### Properties

- [API Reference](https://axiom.co/docs/restapi/endpoints)
- [OpenAPI](openapi/axiom-co-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/axiom-co.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/axiom-co.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/axiomhq)
- [LinkedIn](https://www.linkedin.com/company/axiomhq)
- [Website](https://axiom.co/)
- [Documentation](https://axiom.co/docs)
- [Plans](plans/axiom-co-plans-pricing.yml)
- [Rate Limits](rate-limits/axiom-co-rate-limits.yml)
- [Fin Ops](finops/axiom-co-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
