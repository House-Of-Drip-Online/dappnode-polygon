# Polygon Node DAppNode package

> **CURRENTNESS WARNING — 2026-10-11:** This repository is a historical Polygon node deployment source, **not an operating, synchronized, production-certified Polygon RPC node**. DAppNode Bor/Heimdall images, snapshot and dependency versions are not independently verified against current Polygon PoS Heimdall-v2/Bor releases. Do not deploy its commands without the compatibility review in [NODE_READINESS_2026-10-11.md](docs/NODE_READINESS_2026-10-11.md). The original instructions below are retained for audit/history.


[![DAppNodeStore Available](https://img.shields.io/badge/DAppNodeStore-Available-brightgreen.svg)](http://my.dappnode/#/installer/polygon.public.dappnode.eth)

[![Polygon github](https://img.shields.io/badge/GithubRepo-blue.svg)](https://github.com/maticnetwork/launch) (Official)

Polygon (aka Matic) is a PoS EVM network. This package deploys a Polygon Full Node (Pruned) that will, by default, download the latest snapshot (at the time of publishing) the package and then sync to the tip of the chain.

The primary container in this package is `bor` which provides the RPC endpoint on `8545/tcp` - you can map this to a host port if you wish to access it without the VPN or expose it via HTTPS.

There is also the PoS container `heimdalld` which has an API at `26657/tcp` - you generally don't need to expose this at all, but if you want to query the status of heimdall remotely without the VPN you can map this port as well. e.g. `http://heimdalld:26657/status`

By default this package maps ports 40303 (tcp & udp) and 26656/tcp to the DAppNode Host for peering of bor and heimdall respectively.

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details


## Sovereign admission alignment

This repository remains an independent infrastructure/build boundary. Shared trust and interoperability semantics are documented in [`docs/SOVEREIGN_ADMISSION_ALIGNMENT.md`](docs/SOVEREIGN_ADMISSION_ALIGNMENT.md). Sovereign alignment does not merge repositories, builds, deployments, security domains, or runtime authority.


## Source authority matrix

Source ownership, active versus archival loci, external authority boundaries, and known divergences are documented in [`docs/SOURCE_AUTHORITY_MATRIX.md`](docs/SOURCE_AUTHORITY_MATRIX.md), governed portfolio-wide by `House-Of-Drip-Online/-MAEVN-HOLDINGS/topology/APEX_SOURCE_AUTHORITY_MATRIX.md` (APEX-SOURCE-001). File presence alone does not establish runtime, deployment, registry, execution, or certification authority.
