---
title: "KdaFS (KIP 025)"
author: "Pascal"
description: "Proposal for a standardized Metadata On-chain Storage"
date: "2024-01-01"
toc: false
thumbnail: /kdafs.png
weight: 130
---
## Context

On Marmalade NG (and Marmalade V2), the ledger doesn't manage metadata (expect pure technical data needed to manage sales/transfers ...).
Metadata (and eventually images) must be stored by a third party protocol with the following properties:
  - long term storage guarantee
  - immutability

Storing an NFTs on a centralized server, or only accessible using a dedicated provider via `http` or `https` (eg https://immutablerecord.com/ ) is out of question and too risky for holders:

https://cointelegraph.com/news/nfts-minted-on-ftx-break-highlighting-web2-hosting-flaws


IPFS provides a good option for storing NFTs metadata but suffers from 2 issues:
  - Pinning issue. Holders must rely on creator's pinning severs. (A perfectly acceptable workaround is to recommend the holders to pin themselves their own NFTs. But this not very user friendly)
  - Slowness and reachability: Sometimes the network is relatively slow to retrieve the data, especially in case of low pin counts.

## KdaFS and KIP 025

KdaFS is a proposed as an alternative to ipfs:// for storing durably NFTs metadata.

Depending on the contract implementation, metadata are:
  - perfectly immutable
  - storage term will be the duration of the Kadena blockchain: same lifetime as Marmalade


KdaFS is not linked to Marmalade NG, but **is a perfect companion**.

More specifically:
   - KdaFS is not mandatory for Marmade NG (*ipfs* is a definitively an acceptable and good option)
   - KdaFS can be used for other ledgers or others unrelated projects like Marmalade V2.


Currently the KIP025 in "proposal state": https://github.com/kadena-io/KIPs/pull/54

Standard proposal: https://github.com/kadena-io/KIPs/blob/75099f2e112c87ad4669f1a643cbd7bf49cfce66/kip-0025.md

It should be accepted as standard before being used safely (with a guarantee of durability), and make *mandatory* for wallets and marketplaces to implement it.

**Any help for pushing an approval by the Kadena's a team is appreciated.**

## Images and KdaFS

Since Marmalade NG metadata's standard allows embedding images as a dataURI, it's possible to store images directly in the metadata object on KdaFS.
But because of the block size limitation on Kadena, the image size is roughly limited to 100kb, preventing High resolution images from being used.

For HD images, either:
- Store the metadata on KdaFS and the image on ipfs.
- Don't use KdaFS at all.

However for low res images, KdaFS is ideal.

## Reference implementation

https://github.com/Marmalade-NG/kdafs

## On-chain Contracts

Kdafs requires a special contract to be deployed. Example are given in the repository

This contract can be private, or public. Soon, a public "*official*" (= can be trusted) contract will be deployed on chain 8 on Mainnet.

## Gateways

Wallets, marketplace or other Dapp for simplicity can use a gateway as described in the standard.

Currently a gateway is deployed at:
  https://gw.marmalade-ng.xyz

Soon a swarm of gateways will be deployed on the Flux network.


## Access directly through a node

Anyone can access directly a Kdafs library. Soon a library will be released based on:
https://github.com/Marmalade-NG/kdafs/blob/main/gateway/Kda_fs.js
