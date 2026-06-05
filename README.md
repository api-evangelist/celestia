# celestia (celestia)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/celestia/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/celestia/refs/heads/main/apis.yml)

## Scope

- **Position:** Producing

## Timestamps

- **Created:** 2026-05-24T00:00:00.000Z
- **Modified:** 2026-05-30

## APIs

### Celestia Node Blob API

JSON-RPC methods in the blob module of celestia-node. Submit blobs to one or more namespaces with blob.Submit, retrieve them by height with blob.Get and blob.GetAll, generate inclusion proofs with blob.GetProof, check inclusion with blob.Included, and subscribe to namespace blobs with blob.Subscribe. The canonical surface for rollups and applications publishing data to Celestia.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Blob
- Celestia
- DataAvailability
- JSONRPC

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-blob-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-blob-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-blob-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](openapi/celestia-subscriptions-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](json-schema/celestia-blob-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/celestia-namespace-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/celestia-blob-structure.json)
- [JSON-LD](json-ld/celestia-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/celestia-blob-submit-example.json)
- [Example](examples/celestia-blob-get-example.json)

### Celestia Node Header API

JSON-RPC methods in the header module of celestia-node. Query ExtendedHeaders with header.LocalHead, header.NetworkHead, header.GetByHeight, header.GetByHash, and header.GetRangeByHeight; track sync state with header.SyncState and header.SyncWait; and subscribe to new headers with header.Subscribe.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Celestia
- Header
- JSONRPC

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-header-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-header-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-header-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](openapi/celestia-subscriptions-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](json-schema/celestia-extended-header-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/celestia-header-getbyheight-example.json)

### Celestia Node DA API

JSON-RPC methods in the da module of celestia-node implementing the modular Data Availability interface used by Rollkit, Optimism Alt-DA, Arbitrum Nitro DAS, and other rollup frameworks. Exposes da.Submit, da.Get, da.GetIDs, da.GetProofs, da.Commit, da.Validate, and da.MaxBlobSize.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Celestia
- DataAvailability
- JSONRPC
- Rollup

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-da-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-da-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-da-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/celestia-da-submit-example.json)

### Celestia Node Share API

JSON-RPC methods in the share module of celestia-node. Provides direct access to Celestia's share-level data, the extended data square (EDS), namespaced shares, and share proofs via share.SharesAvailable, share.GetShare, share.GetEDS, share.GetNamespaceData, share.GetRange, and share.GetSamples.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Celestia
- DataAvailability
- JSONRPC
- Share

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-share-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-share-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-share-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/celestia-share-getnamespacedata-example.json)

### Celestia Node State API

JSON-RPC methods in the state module of celestia-node. Exposes state-level operations including account balances, transfers, delegations, and most importantly state.SubmitPayForBlob, the canonical entrypoint for submitting PayForBlobs transactions to the celestia-app state machine.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Celestia
- JSONRPC
- PayForBlobs
- State

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-state-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-state-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-state-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/celestia-state-submitpayforblob-example.json)

### Celestia Node DAS API

JSON-RPC methods in the das module of celestia-node. Operational introspection over the Data Availability Sampling subsystem that light nodes run to probabilistically verify block data availability. Exposes das.SamplingStats and das.WaitCatchUp.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Celestia
- DAS
- DataAvailabilitySampling
- JSONRPC

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-das-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-das-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-das-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](openapi/celestia-subscriptions-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Celestia Node Fraud API

JSON-RPC methods in the fraud module of celestia-node. Exposes fraud proof retrieval and subscription for the BadEncoding fraud proof type used to slash bridge nodes that propagate incorrectly erasure-coded blocks. Methods include fraud.Get and fraud.Subscribe.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Celestia
- FraudProof
- JSONRPC

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-fraud-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-fraud-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-fraud-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](openapi/celestia-subscriptions-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Celestia Node P2P API

JSON-RPC methods in the p2p module of celestia-node. libp2p-level introspection and control over the Celestia DA network including peer info, NAT status, connection management, bandwidth stats, pubsub topics, and the private/protected peer lists.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Celestia
- JSONRPC
- LibP2P
- P2P

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-p2p-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-p2p-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-p2p-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Celestia Node Admin API

JSON-RPC methods in the node module of celestia-node. Provides administrative introspection over the running node including node.Info, node.Ready, node.LogLevelSet, and the auth-token issuance methods node.AuthNew and node.AuthVerify used to delegate capability-scoped access to other API modules (public, read, write, admin).

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Administrative
- Auth
- Celestia
- JSONRPC

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-node-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-node-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-node-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Celestia Node Blobstream API

JSON-RPC methods in the blobstream module of celestia-node. Generates inclusion proofs against Blobstream data commitments so EVM chains can verify, via the Blobstream(X) bridge contracts, that a given blob was published to Celestia at a specific height. Methods include blobstream.GetDataRootTupleRoot, blobstream.GetDataRootTupleInclusionProof, and blobstream.GetShareProof.

- **Human URL:** [https://node-rpc-docs.celestia.org/](https://node-rpc-docs.celestia.org/)

#### Tags

- Blobstream
- Bridge
- Celestia
- EVM
- JSONRPC

#### Properties

- [Documentation](https://node-rpc-docs.celestia.org/)
- [OpenAPI](openapi/celestia-blobstream-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/celestia-blobstream-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/celestia-blobstream-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://celestia.org)
- [Documentation](https://docs.celestia.org)
- [Documentation](https://node-rpc-docs.celestia.org/)
- [Getting Started](https://docs.celestia.org/learn/celestia-101/data-availability/)
- [Getting Started](https://docs.celestia.org/build/quick-start)
- [Blog](https://blog.celestia.org)
- [Forum](https://forum.celestia.org)
- [Forum](https://discord.com/invite/YsnTPcSfWQ)
- [Twitter](https://x.com/CelestiaOrg)
- [GitHub Organization](https://github.com/celestiaorg)
- [SDK](https://github.com/celestiaorg/celestia-node)
- [SDK](https://github.com/celestiaorg/celestia-app)
- [SDK](https://github.com/celestiaorg/celestia-core)
- [SDK](https://github.com/celestiaorg/celestia-openrpc)
- [SDK](https://github.com/celestiaorg/celestia-ts)
- [SDK](https://github.com/celestiaorg/celestia-node-client-rs)
- [SDK](https://docs.rs/celestia-rpc)
- [SDK](https://github.com/celestiaorg/lumina)
- [Tool](https://github.com/celestiaorg/nmt)
- [Tool](https://github.com/celestiaorg/rsmt2d)
- [Tool](https://github.com/celestiaorg/go-square)
- [Tool](https://github.com/celestiaorg/blobstream-contracts)
- [Tool](https://github.com/celestiaorg/orchestrator-relayer)
- [Integration](https://github.com/celestiaorg/op-alt-da)
- [Integration](https://github.com/celestiaorg/nitro-das-celestia)
- [Integration](https://github.com/rollkit/celestia-da)
- [Specification](https://github.com/celestiaorg/celestia-specs)
- [Specification](https://github.com/celestiaorg/CIPs)
- [Documentation](https://github.com/celestiaorg/docs)
- [Code Examples](https://github.com/celestiaorg/awesome-celestia)
- [Documentation](https://github.com/celestiaorg/networks)
- [Tool](https://github.com/celestiaorg/helm-charts)
- [License](https://www.apache.org/licenses/LICENSE-2.0)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
