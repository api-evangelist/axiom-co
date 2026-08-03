# Axiom (axiom-co)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
