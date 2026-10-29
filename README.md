# Axiom

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Axiom is a log management, event data, and observability platform that ingests, stores, and queries large volumes of logs, traces, and events at low cost. Data is loaded into datasets and queried with the Axiom Processing Language (APL). The REST API (base https://api.axiom.co, US region; https://api.eu.axiom.co for EU) exposes ingest, APL query, datasets, fields, annotations, monitors, notifiers, dashboards, virtual fields, starred queries, API tokens, users, and organizations, with v1 and v2 endpoint families and Bearer token authentication.

**Areas:** Observability · Log Management · Event Data · Logs · Tracing · Analytics · APL

## Axiom on APIs.io

Everything profiled for Axiom is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/axiom-co/](https://apis.io/providers/axiom-co/)** — or go straight to one of the APIs or properties below.

### APIs (19)

- [Axiom Annotations API](https://apis.io/apis/axiom-co/axiom-co-annotations-api/) — Mark deployments, incidents, and events on charts.
- [Axiom Dashboards API](https://apis.io/apis/axiom-co/axiom-co-dashboards-api/) — Collections of charts and visualizations.
- [Axiom Datasets API](https://apis.io/apis/axiom-co/axiom-co-datasets-api/) — Manage the datasets that store ingested event data.
- [Axiom Fields API](https://apis.io/apis/axiom-co/axiom-co-fields-api/) — Inspect and annotate dataset fields.
- [Axiom Ingest API](https://apis.io/apis/axiom-co/axiom-co-ingest-api/) — Send logs, traces, and events into a dataset.
- [Axiom Monitors API](https://apis.io/apis/axiom-co/axiom-co-monitors-api/) — APL-backed alert monitors.
- [Axiom Notifiers API](https://apis.io/apis/axiom-co/axiom-co-notifiers-api/) — Notification channels monitors dispatch through.
- [Axiom Organizations API](https://apis.io/apis/axiom-co/axiom-co-organizations-api/) — Organization-level settings.
- [Axiom Query API](https://apis.io/apis/axiom-co/axiom-co-query-api/) — Run APL queries across datasets.
- [Axiom Starred Queries API](https://apis.io/apis/axiom-co/axiom-co-starred-queries-api/) — Saved, shareable APL queries.
- [Axiom Tokens API](https://apis.io/apis/axiom-co/axiom-co-tokens-api/) — Scoped API tokens used to authenticate requests.
- [Axiom Users API](https://apis.io/apis/axiom-co/axiom-co-users-api/) — Current user and organization members.
- [Axiom Virtual Fields API](https://apis.io/apis/axiom-co/axiom-co-virtual-fields-api/) — Derived fields computed from an APL expression at query time.
- [Axiom Edge API](https://apis.io/apis/axiom-co/axiom-co-edge-api/) — The Edge API from Axiom — 3 operation(s) for edge.
- [Axiom Groups API](https://apis.io/apis/axiom-co/axiom-co-groups-api/) — The Groups API from Axiom — 2 operation(s) for groups.
- [Axiom Mapfields API](https://apis.io/apis/axiom-co/axiom-co-mapfields-api/) — The Mapfields API from Axiom — 1 operation(s) for mapfields.
- [Axiom Roles API](https://apis.io/apis/axiom-co/axiom-co-roles-api/) — The Roles API from Axiom — 2 operation(s) for roles.
- [Axiom Views API](https://apis.io/apis/axiom-co/axiom-co-views-api/) — The Views API from Axiom — 2 operation(s) for views.
- [Axiom MCP Server](https://apis.io/apis/axiom-co/axiom-co-mcp-server/) — Axiom's hosted remote Model Context Protocol server (HTTP transport) at mcp.axiom.co, OAuth-protected per RFC 9728, for querying datasets with APL from agents.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Axiom Custom Webhook Notifier](https://apis.io/asyncapis/axiom-co/axiom-co-custom-webhook-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/webhook](https://apis.io/channels/axiom-co/webhook/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Moved to axiom-co](https://apis.io/servers/axiom-co/axiom/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Axiom Co Agentic Access](https://apis.io/agentic-access/axiom-co/axiom-co-agentic-access/)

#### JSON Schema (18)

The data models the API reads and writes.

- [Annotation](https://apis.io/schemas/axiom-co/axiom-co-annotation/)
- [AplQueryRequest](https://apis.io/schemas/axiom-co/axiom-co-apl-query-request/)
- [Dashboard](https://apis.io/schemas/axiom-co/axiom-co-dashboard/)
- [Dataset](https://apis.io/schemas/axiom-co/axiom-co-dataset/)
- [DatasetCreateRequest](https://apis.io/schemas/axiom-co/axiom-co-dataset-create-request/)
- [DatasetUpdateRequest](https://apis.io/schemas/axiom-co/axiom-co-dataset-update-request/)
- [Field](https://apis.io/schemas/axiom-co/axiom-co-field/)
- [IngestStatus](https://apis.io/schemas/axiom-co/axiom-co-ingest-status/)
- [Monitor](https://apis.io/schemas/axiom-co/axiom-co-monitor/)
- [Notifier](https://apis.io/schemas/axiom-co/axiom-co-notifier/)
- [Organization](https://apis.io/schemas/axiom-co/axiom-co-organization/)
- [QueryResult](https://apis.io/schemas/axiom-co/axiom-co-query-result/)
- [StarredQuery](https://apis.io/schemas/axiom-co/axiom-co-starred-query/)
- [Token](https://apis.io/schemas/axiom-co/axiom-co-token/)
- [TokenCreateRequest](https://apis.io/schemas/axiom-co/axiom-co-token-create-request/)
- [TokenCreated](https://apis.io/schemas/axiom-co/axiom-co-token-created/)
- [User](https://apis.io/schemas/axiom-co/axiom-co-user/)
- [VirtualField](https://apis.io/schemas/axiom-co/axiom-co-virtual-field/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Axiom Co Context](https://apis.io/jsonld/axiom-co/axiom-co-context/)

#### Collections (14)

Postman and Open Collection request collections.

- [Axiom API](https://apis.io/collections/axiom-co/open-axiom-co/)
- [Axiom Annotations API](https://apis.io/collections/axiom-co/open-axiom-co-annotations-api/)
- [Axiom Annotations Dashboards API](https://apis.io/collections/axiom-co/open-axiom-co-dashboards-api/)
- [Axiom Annotations Datasets API](https://apis.io/collections/axiom-co/open-axiom-co-datasets-api/)
- [Axiom Annotations Fields API](https://apis.io/collections/axiom-co/open-axiom-co-fields-api/)
- [Axiom Annotations Ingest API](https://apis.io/collections/axiom-co/open-axiom-co-ingest-api/)
- [Axiom Annotations Monitors API](https://apis.io/collections/axiom-co/open-axiom-co-monitors-api/)
- [Axiom Annotations Notifiers API](https://apis.io/collections/axiom-co/open-axiom-co-notifiers-api/)
- [Axiom Annotations Organizations API](https://apis.io/collections/axiom-co/open-axiom-co-organizations-api/)
- [Axiom Annotations Query API](https://apis.io/collections/axiom-co/open-axiom-co-query-api/)
- [Axiom Annotations Starred Queries API](https://apis.io/collections/axiom-co/open-axiom-co-starred-queries-api/)
- [Axiom Annotations Tokens API](https://apis.io/collections/axiom-co/open-axiom-co-tokens-api/)
- [Axiom Annotations Users API](https://apis.io/collections/axiom-co/open-axiom-co-users-api/)
- [Axiom Annotations Virtual Fields API](https://apis.io/collections/axiom-co/open-axiom-co-virtual-fields-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Axiom API Rules](https://apis.io/rules/axiom-co/axiom-co-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Axiom Co Authentication](https://apis.io/security/axiom-co/axiom-co-authentication/)
- [Axiom Co Domain Security](https://apis.io/security/axiom-co/axiom-co-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Axiom Co Plans Pricing](https://apis.io/plans/axiom-co/axiom-co-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Axiom Co Rate Limits](https://apis.io/rate-limits/axiom-co/axiom-co-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Axiom Co Finops](https://apis.io/finops/axiom-co/axiom-co-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://axiom.co/)
- [Documentation](https://axiom.co/docs)
- [Blog](https://axiom.co/blog/feed.xml)
- [GitHub](https://github.com/axiomhq)

## API Evangelist rating

**Kin Score 37.7** — thin · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 68.3 |
| Contract quality | 69.3 |
| Contract governance | 19.7 |
| Operational transparency | 18.4 |
| Developer ergonomics | 38.6 |
| Access clarity | 7.9 |

**Agent readiness 41.8** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | verified |
| Event Surface Described | derived (partial credit) |
| Agent Skills | unknown |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 16.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/axiom-co/](https://apis.io/providers/axiom-co/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Axiom: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/axiom-co/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
