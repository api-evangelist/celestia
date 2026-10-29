# Celestia

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

Celestia is the first production modular data availability blockchain. It separates
consensus and data availability from execution and settlement, letting rollups,
sovereign chains, and other execution layers post their transaction data as blobs
to Celestia under namespaces while running their own state machines. Light nodes
use Data Availability Sampling and Namespaced Merkle Trees to verify availability
without downloading full blocks, and the Blobstream / Blobstream X bridge attests
Celestia data commitments on Ethereum and other EVM chains. The reference stack —
celestia-app (consensus, Cosmos SDK + CometBFT) and celestia-node (DA bridge/full/
light nodes) — exposes a JSON-RPC API with nine modules (blob, header, share,
state, das, fraud, p2p, node, da, blobstream), plus a modular DA interface used
by Rollkit, Optimism Alt-DA, Arbitrum Nitro DAS, and other rollup frameworks.

**Areas:** Blockchain · Data Availability · Web3 · Infrastructure · Open Source · JSON-RPC · Modular Blockchain · Rollup · Cryptography · Developer Tools

## Celestia on APIs.io

Everything profiled for Celestia is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/celestia/](https://apis.io/providers/celestia/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Celestia Node Blob API](https://apis.io/apis/celestia/celestia-blob-api/) — JSON-RPC methods in the blob module of celestia-node. Submit blobs to one or more namespaces with blob.Submit, retrieve them by height with blob.Get and…
- [Celestia Node Header API](https://apis.io/apis/celestia/celestia-header-api/) — JSON-RPC methods in the header module of celestia-node. Query ExtendedHeaders with header.LocalHead, header.NetworkHead, header.GetByHeight,…
- [Celestia Node DA API](https://apis.io/apis/celestia/celestia-da-api/) — JSON-RPC methods in the da module of celestia-node implementing the modular Data Availability interface used by Rollkit, Optimism Alt-DA, Arbitrum Nitro…
- [Celestia Node Share API](https://apis.io/apis/celestia/celestia-share-api/) — JSON-RPC methods in the share module of celestia-node. Provides direct access to Celestia's share-level data, the extended data square (EDS), namespaced…
- [Celestia Node State API](https://apis.io/apis/celestia/celestia-state-api/) — JSON-RPC methods in the state module of celestia-node. Exposes state-level operations including account balances, transfers, delegations, and most…
- [Celestia Node DAS API](https://apis.io/apis/celestia/celestia-das-api/) — JSON-RPC methods in the das module of celestia-node. Operational introspection over the Data Availability Sampling subsystem that light nodes run to…
- [Celestia Node Fraud API](https://apis.io/apis/celestia/celestia-fraud-api/) — JSON-RPC methods in the fraud module of celestia-node. Exposes fraud proof retrieval and subscription for the BadEncoding fraud proof type used to slash…
- [Celestia Node Admin API](https://apis.io/apis/celestia/celestia-node-api/) — JSON-RPC methods in the node module of celestia-node. Provides administrative introspection over the running node including node.Info, node.Ready,…
- [Celestia Node Blobstream API](https://apis.io/apis/celestia/celestia-blobstream-api/) — JSON-RPC methods in the blobstream module of celestia-node. Generates inclusion proofs against Blobstream data commitments so EVM chains can verify, via the…
- [Celestia P2P API](https://apis.io/apis/celestia/celestia-p2p-api/) — libp2p peer, connection, NAT, and pubsub control.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Derived candidate only — Celestia publishes no MCP server](https://apis.io/servers/celestia/derived-candidate-only-celestia-publishes-no-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Celestia Agentic Access](https://apis.io/agentic-access/celestia/celestia-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Celestia Blob](https://apis.io/schemas/celestia/celestia-blob/)
- [Celestia Extended Header](https://apis.io/schemas/celestia/celestia-extended-header/)
- [Celestia Namespace](https://apis.io/schemas/celestia/celestia-namespace/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Celestia Blob Structure](https://apis.io/json-structure/celestia/celestia-blob-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Celestia Context](https://apis.io/jsonld/celestia/celestia-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Celestia Vocabulary](https://apis.io/vocabularies/celestia/celestia-vocabulary/)

#### Examples (6)

Example requests and responses.

- [Celestia Blob Get Example](https://apis.io/examples/celestia/celestia-blob-get-example/)
- [Celestia Blob Submit Example](https://apis.io/examples/celestia/celestia-blob-submit-example/)
- [Celestia Da Submit Example](https://apis.io/examples/celestia/celestia-da-submit-example/)
- [Celestia Header Getbyheight Example](https://apis.io/examples/celestia/celestia-header-getbyheight-example/)
- [Celestia Share Getnamespacedata Example](https://apis.io/examples/celestia/celestia-share-getnamespacedata-example/)
- [Celestia State Submitpayforblob Example](https://apis.io/examples/celestia/celestia-state-submitpayforblob-example/)

#### Collections (11)

Postman and Open Collection request collections.

- [Celestia Node Blob API](https://apis.io/collections/celestia/open-celestia-blob-api/)
- [Celestia Node Blob Blobstream API](https://apis.io/collections/celestia/open-celestia-blobstream-api/)
- [Celestia Node Blob DA API](https://apis.io/collections/celestia/open-celestia-da-api/)
- [Celestia Node Blob DAS API](https://apis.io/collections/celestia/open-celestia-das-api/)
- [Celestia Node Blob Fraud API](https://apis.io/collections/celestia/open-celestia-fraud-api/)
- [Celestia Node Blob Header API](https://apis.io/collections/celestia/open-celestia-header-api/)
- [Celestia Blob Node API](https://apis.io/collections/celestia/open-celestia-node-api/)
- [Celestia Node Blob P2P API](https://apis.io/collections/celestia/open-celestia-p2p-api/)
- [Celestia Node Blob Share API](https://apis.io/collections/celestia/open-celestia-share-api/)
- [Celestia Node Blob State API](https://apis.io/collections/celestia/open-celestia-state-api/)
- [Celestia Node Subscriptions](https://apis.io/collections/celestia/open-celestia-subscriptions-asyncapi/)

#### Overlays (10)

OpenAPI overlays, including conversational phrasing for each operation.

- [Celestia Blob Api Overlay](https://apis.io/overlays/celestia/celestia-blob-api-overlay/)
- [Celestia Blobstream Api Overlay](https://apis.io/overlays/celestia/celestia-blobstream-api-overlay/)
- [Celestia Da Api Overlay](https://apis.io/overlays/celestia/celestia-da-api-overlay/)
- [Celestia Das Api Overlay](https://apis.io/overlays/celestia/celestia-das-api-overlay/)
- [Celestia Fraud Api Overlay](https://apis.io/overlays/celestia/celestia-fraud-api-overlay/)
- [Celestia Header Api Overlay](https://apis.io/overlays/celestia/celestia-header-api-overlay/)
- [Celestia Node Api Overlay](https://apis.io/overlays/celestia/celestia-node-api-overlay/)
- [Celestia P2 P Api Overlay](https://apis.io/overlays/celestia/celestia-p2-p-api-overlay/)
- [Celestia Share Api Overlay](https://apis.io/overlays/celestia/celestia-share-api-overlay/)
- [Celestia State Api Overlay](https://apis.io/overlays/celestia/celestia-state-api-overlay/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Celestia — jsonschema rules](https://apis.io/rules/celestia/celestia-jsonschema-spectral-rules/)
- [Celestia API Rules](https://apis.io/rules/celestia/celestia-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Celestia Authentication](https://apis.io/security/celestia/celestia-authentication/)
- [Celestia Domain Security](https://apis.io/security/celestia/celestia-domain-security/)
- [Celestia Trust Center](https://apis.io/security/celestia/celestia-trust-center/)
- [Celestia Vulnerability Disclosure](https://apis.io/security/celestia/celestia-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Celestia Plans Pricing](https://apis.io/plans/celestia/celestia-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Celestia Rate Limits](https://apis.io/rate-limits/celestia/celestia-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.celestia.org/)
- [Documentation](https://docs.celestia.org)
- [Getting started](https://docs.celestia.org/learn/celestia-101/data-availability/)
- [API reference](https://docs.celestia.org/build/rpc/node-api/)
- [Support](https://forum.celestia.org)
- [Blog](https://blog.celestia.org)
- [Terms of service](https://celestia.org/tos/)
- [Privacy policy](https://celestia.org/privacy/)
- [GitHub](https://github.com/celestiaorg)
- [Status](https://status.celestia.org)

## API Evangelist rating

**Kin Score 63.8** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 60.6 |
| Contract governance | 31.8 |
| Operational transparency | 86.8 |
| Developer ergonomics | 95.2 |
| Access clarity | 28.9 |

**Agent readiness 35.6** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | verified |
| Event Surface Described | — |
| Agent Skills | yes |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 35.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/celestia/](https://apis.io/providers/celestia/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Celestia: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/celestia/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
