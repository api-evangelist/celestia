# Celestia (celestia)

Celestia is the first production modular data availability blockchain. It separates consensus and data availability from execution and settlement, letting rollups, sovereign chains, and other execution layers post their transaction data as blobs to Celestia under namespaces while running their own state machines. Light nodes use Data Availability Sampling (DAS) and Namespaced Merkle Trees (NMT) to verify availability without downloading full blocks, and the Blobstream / Blobstream X bridge attests Celestia data commitments on Ethereum and other EVM chains.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/celestia/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=opensource-api-evangelist&utm_content=repo)

## Tags

Blob, Blobstream, Bridge, Celestia, DAS, DataAvailability, DataAvailabilitySampling, EVM, FraudProof, Header, JSONRPC, LibP2P, P2P, PayForBlobs, Rollup, Share, State

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## Networks

| Network | Chain ID | Status | Faucet |
|---|---|---|---|
| Mainnet Beta | `celestia` | Live since Oct 2023 | n/a |
| Mocha-4 testnet | `mocha-4` | Live | Public faucet |
| Arabica devnet | `arabica-11` | Live (frequently reset) | Public faucet |

## APIs

| API | Module | Spec |
|---|---|---|
| Celestia Node Blob API | `blob.*` | [openapi](openapi/celestia-blob-api-openapi.yml) |
| Celestia Node Header API | `header.*` | [openapi](openapi/celestia-header-api-openapi.yml) |
| Celestia Node DA API | `da.*` | [openapi](openapi/celestia-da-api-openapi.yml) |
| Celestia Node Share API | `share.*` | [openapi](openapi/celestia-share-api-openapi.yml) |
| Celestia Node State API | `state.*` | [openapi](openapi/celestia-state-api-openapi.yml) |
| Celestia Node DAS API | `das.*` | [openapi](openapi/celestia-das-api-openapi.yml) |
| Celestia Node Fraud API | `fraud.*` | [openapi](openapi/celestia-fraud-api-openapi.yml) |
| Celestia Node P2P API | `p2p.*` | [openapi](openapi/celestia-p2p-api-openapi.yml) |
| Celestia Node Admin API | `node.*` | [openapi](openapi/celestia-node-api-openapi.yml) |
| Celestia Node Blobstream API | `blobstream.*` | [openapi](openapi/celestia-blobstream-api-openapi.yml) |

All ten modules are exposed via a single JSON-RPC endpoint on celestia-node (default `http://localhost:26658`) using bearer-token auth scoped to one of four permission tiers: `public`, `read`, `write`, `admin`. Tokens are minted via `celestia <node-type> auth <permissions>` or `node.AuthNew`.

## Reference Implementations

| Repo | Description | Language |
|---|---|---|
| [celestia-node](https://github.com/celestiaorg/celestia-node) | DA bridge/full/light nodes; JSON-RPC server | Go |
| [celestia-app](https://github.com/celestiaorg/celestia-app) | Consensus node (Cosmos SDK + CometBFT) | Go |
| [celestia-core](https://github.com/celestiaorg/celestia-core) | Fork of CometBFT used by celestia-app | Go |
| [lumina](https://github.com/celestiaorg/lumina) | Wasm-friendly Rust light node | Rust |
| [celestia-openrpc](https://github.com/celestiaorg/celestia-openrpc) | Go client w/o celestia-node deps (archived 2025-04) | Go |
| [celestia-ts](https://github.com/celestiaorg/celestia-ts) | TypeScript client | TypeScript |
| [celestia-rpc](https://docs.rs/celestia-rpc) | Rust RPC client crate | Rust |

## Core Tooling Libraries

- [nmt](https://github.com/celestiaorg/nmt) — Namespaced Merkle Tree
- [rsmt2d](https://github.com/celestiaorg/rsmt2d) — 2D Reed-Solomon Merkle Tree erasure code
- [go-square](https://github.com/celestiaorg/go-square) — Blob encoding into 2D EDS
- [go-fraud](https://github.com/celestiaorg/go-fraud) — Generic p2p fraud proof library
- [go-header](https://github.com/celestiaorg/go-header) — Header sync, gossip, and storage

## Bridges and Rollup Integrations

- [blobstream-contracts](https://github.com/celestiaorg/blobstream-contracts) — Celestia → EVM bridge
- [orchestrator-relayer](https://github.com/celestiaorg/orchestrator-relayer) — Blobstream orchestrator/relayer
- [op-alt-da](https://github.com/celestiaorg/op-alt-da) — Optimism Alt-DA provider backed by Celestia
- [nitro-das-celestia](https://github.com/celestiaorg/nitro-das-celestia) — Arbitrum Nitro DAS provider
- [hana](https://github.com/celestiaorg/hana) — Kona-based derivation pipeline for Celestia DA
- [celestia-da (Rollkit)](https://github.com/rollkit/celestia-da) — Modular DA interface implementation

## Specifications and Governance

- [celestia-specs](https://github.com/celestiaorg/celestia-specs) — Protocol specifications
- [CIPs](https://github.com/celestiaorg/CIPs) — Celestia Improvement Proposals
- [networks](https://github.com/celestiaorg/networks) — Public network configs and genesis files
- [docs](https://github.com/celestiaorg/docs) — Documentation source (MDX)

## License

All core repositories are licensed under [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0).

## Maintainer

- **Kin Lane** — <info@apievangelist.com> — <https://apievangelist.com>
