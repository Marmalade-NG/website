---
title: "Introduction to Marmalade NG"
author: "Pascal"
description: "A short introduction to Marmalade NG"
tags: []
date: "2024-01-01"
toc: false
thumbnail: /marm_code.png
weight: 200
---
A short introduction to Marmalade NG

<!--more-->

---

## What is Marmalade NG

Marmalade NG is a set of Smart contracts for the Kadena Blockchain. Marmalade NG is a successor to Marmalade V1.

Marmalade V1 introduced the concept of decentralized NFTs management and sales on Kadena. But had many limitations.
Kadena team started to create a new standard called Marmalade V2. While Marmalade V2 introduced interesting new ideas, it appears that Marmalade V2 was not developed as it should:

- Bad development practices
- Many issues and security flaws
- Don't fit user's and creator's needs.

That's why Marmalade-NG has been created. Initially, it was intended to be a fork of Marmalade V2, but quickly led to a major rewrite.

The smart contracts have been written according to the following recipes:

- Maximum security:
   * strict separation between tokens, policies, policies hooks.
   * strict validation of all data and user inputs.
   * All modrefs calls and re-entrancy attacks vectors have been verified and evaluated.
   * No circular dependencies
   * All recommendations from the Pact developers have been evaluated.

- Fairness and trustability:
  * Requirements and allowances are balanced between creators / marketplaces / and users.
  * Game theory: all **cheating** and **involved bad actors** scenarios have been taken into account to verify that nobody could obtain any advantage from trying to cheat.

These Medium articles were "the launchpad" of Marmalade NG:
https://medium.com/@crypto-pac/whats-wrong-with-marmalade-v2-part-1-2-2180d2c6afd

https://medium.com/@crypto-pac/what-can-we-do-with-marmaladev2-2-2-introducing-marmalade-ng-cceb7715c56d



## Architecture: Ledger and Policies

The architecture of Marmalade NG is very simple:

- A central ledger contract that only handles: accounts balances, basic, tokens registration and policy calls. Since, the ledger is the ultimate *Guardian* of Marmalade, its functionalities have been reduced to the less common denominator.

- A set of standard policies (currently 17): No policy is mandatory. Each policy works independently and manages one aspect of Marmalade. Possible combinations of policies are infinite, allowing most creators to issue token with a high degree of customization with 0 Pact code.

- User provided policies, allowing creators / developers create tokens with even more customization, tweaking and special features.


![Marmalade NG](/marmalade_ng_drawing_opt.svg)



## A common decentralized trusted platform

Marmalade NG acts as a common "central" but "decentralized" platform. It covers all steps of the lifetime of an NFT:
   - Creation / Minting
   - Transfers
   - Sales (with or without the help of Marketplace)
   - Holding and user's balances management.
   - X-chain transfers and X-ledgers transfers.

Each actor directly interacts with the set of smart-contracts which take care of the fairness of all the operations.

**Examples:**

From a creator / issuer point of view:
   - The creator can choose what are the allowed sales mechanisms
   - The creator can impose a royalty on each sale
   - The creator can limit or prevent centralized platforms from handling the NFT
   - The creator can decide whether marketplaces are allowed to add their own fees.
   - ... and many more via custom policies

From a marketplace point of view:
  - The Marketplace can impose a fee when a sale has been initiated (even if the NFT is finally bought on another Marketplace)
  - The Marketplace can define whether it allows a buying marketplace to share the fee.

From a user/holder point of view:
  - The holder can be sure that the rules of its NFT won't change in the future.
  - He can be sure that even without trusting the Marketplace, sales will be conducted fairly without any possibility of being rugged.

**HOWEVER** there are exceptions, where trustability can't 100% assured. But Marmalade NG in these limited cases provide all the transparency to evaluate what are the risks involved with a given NFT.



## An NFT building framework

For building an NFT, creators have the following possibilities:
- Choose a set of policies, matching their needs (should satisfy most basic cases)
- And optionally use Marmalade NG as a framework to write their own policies. This allows infinite possibilities for NFTs. And moreover, since sales are managed by policies, it's even possible to personalize how sales are conducted.

Most standard policies can be combined. And if properly written, custom policies will work together with standard policies. For example, a custom sale mechanism will work together with the standard marketplace and royalty policies.

During development, we already prototyped the following:
- Lottery sales
- Stacked NFTs directly managed by Marmalade
- Lended NFTs with restricted possibilities for the beneficiary.

## A private ledger for hosting NFTs.

Anybody is able to deploy its own instance of Marmalade NG, if special rules are needed at the ledger level, or if someone  prefers to have their own ledger and doesn't want to share with the public one.

However, most marketplaces will only be connected to the "`official`" ledger.

## The explorer

An explorer dApp is available: https://explorer.marmalade-ng.xyz

The explorer only uses on-chain data obtained directly from a node via local pact calls. The explorer should be considered as a reference, since it doesn't use third party indexers.

The explorer can be set-up to explore any ledgers, on any chains, or any networks.

## Support from the community / high valuable projects

Many projects already support Marmalade NG, and will migrate (partially or fully) to NG.

![Supporting projects](/support.png)
