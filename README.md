# Polygon Node DAppNode package

> **2026 compatibility warning — historical DAppNode package only.** This repository still packages Bor `v0.2.14-tmp-span-hotfix`, Heimdall v1 `v0.2.8`, March 2022 snapshots and wildcard RPC bindings. **Do not deploy these files as a current Polygon PoS mainnet node.** The canonical, actively modernized OMEGA node deployment is [POL-mainnet-full-node/modern](https://github.com/House-Of-Drip-Online/POL-mainnet-full-node/tree/main/modern), using Bor v2.11.0 and Heimdall-v2 v0.13.2. This notice does not delete historical source, merge independent repositories or authorize replacement of the currently restoring node. The [comparison and disposition](https://github.com/House-Of-Drip-Online/POL-mainnet-full-node/blob/main/modern/docs/POLYGON_NODE_DAPPNODE_GAP_CLOSURE_20261108.md) identifies reusable concepts but **no compatible legacy binary or snapshot**.


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
