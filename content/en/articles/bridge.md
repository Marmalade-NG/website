---
title: "Marmalade NG Bridge"
author: "Pascal"
description: "Bridging tokens between ledgers instances"
tags: []
date: "2024-01-01"
thumbnail: /bridge.png
weight: 140
---
Bridging tokens between ledgers instances.

<!--more-->

## Introduction
Marmalade-NG Bridge is a side project of Marmalade NG Core.

The objective is to bridge tokens between ledgers instances.

Bridging means:

- Burning the token on the source ledger
- Minting the token on the destination ledger

![Bridge diagram](https://raw.githubusercontent.com/Marmalade-NG/marmalade-ng-bridge/main/doc/source/diagrams/bridge.svg)

## Uses cases

- **Marmalade NG <-> another Marmalade NG instance (Bidirectional)**: Allow bridging between the public (official) Marmalade NG ledger and a private Marmalade ledger. token-id's must be equal.

- **Marmalade NG <-> same Marmalade NG (Bidirectional)**: Allow exchanging a token to another token on the same ledger. This is useful if a creator wants to upgrade his token (for example, to add a new policy).

- **X-chain Marmalade NG <-> same Marmalade NG (Bidirectional)**: Allow bridging tokens between chains. token-id's and ledgers fully qualified names must be equal.

- **Marmalade V1 -> Marmalade NG (Unidirectional)**: Allow to upgrade a Marmalade V1 token to a Marmalade NG token.

- **Generic ledger -> Marmalade NG (Unidirectional)**: Allow upgrading a token from a third party ledger to Marmalade NG token. Only non-fungible tokens are supported.


## Components

The Marmalade NG bridge is composed of several components:

- A main module: which acts as a manager.
- Several Marmalade NG policies.
- Some helper modules to glue to Marmalade V1 or Generic Ledgers.

## Documentation

The technical documentation is available:
https://marmalade-ng-bridge.readthedocs.io
