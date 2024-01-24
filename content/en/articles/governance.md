---
title: "Governance"
author: "Pascal"
description: "Governance of Marmalade NG"
date: "2024-01-01"
toc: false
thumbnail: /governance.jpg
weight: 190
---
Marmalade NG Governance

<!--more-->
## Marmalade NG Governance

Marmalade NG is a community project. Marmalade NG is not based on a DAO.

But the "official ledger" governance is shared by several projects that have a direct interest in the integrity of the contracts.

The governance is done through a Multi-Sig defined keyset.

n_4e470a97222514a8662dd1219000a0431451b0ee.admin-multi-sig (chains 0 to 20)

[MultiSig chain 8](https://kadenakode.marmalade-ng.xyz/?network=https%3A%2F%2Fapi.chainweb.com&networkId=mainnet01&chainIds=%5B%228%22%5D&gasLimit=15000&gasPrice=0.00001&code=(describe-keyset%20%22n_4e470a97222514a8662dd1219000a0431451b0ee.admin-multi-sig%22) )

[MultiSig chain 1](
https://kadenakode.marmalade-ng.xyz/?network=https%3A%2F%2Fapi.chainweb.com&networkId=mainnet01&chainIds=%5B%221%22%5D&gasLimit=15000&gasPrice=0.00001&code=(describe-keyset%20%22n_4e470a97222514a8662dd1219000a0431451b0ee.admin-multi-sig%22) )

The governance will mainly consist of fixing bugs and deploying new features. Don't expect from the governance to manipulate balances and tables data.

### Signees

Multi-Sig: Keys 3 of 6

|              |    PubKey                                                        |
|--------------|------------------------------------------------------------------|
| CryptoPascal | 4e70958bc74b248cfe373e41aaa7bd0ad72b9bf002dc7d6fa27ce2de215ccdd4 |
| KadenAI      | f186668ac03b8b152dc87eac29909f58e58453e2485a6d44046c3413cd77f789 |
| Arkade       | d9724a2521377d915ef6e47b43f5f7e90c506aa00495acafb7b5be416f051a66 |
| MoK          | f5a13cd22f267008481b60035e2d6ec19d1bf92c1054021f1240994d1b7f1e86 |
| Hypercent    | 775a6918e17d2f424f026b294af1d70bf6afadbae85327d05dd3e55fe9c0f954 |
| KadenaBet    | 4a13e13d143161edfb96e2f2a9aef80f020f3337ea29e58fc8689ab230c32412 |


---

## In the future

### Transition to multi-sig smart-wallets

Once multi-sigs Smart-wallets will gain maturity, the governance will transition to them. Allowing more flexibility:

- Easier signature process
- Allowing some awesome features like multi-sigs of multis-sigs.

### Transition to a non-governed module

1 - The ledger module will be made non-upgradable and non-manageable (expected 2024-Q4 / 2025-Q1)

2 - All the standard policies will be made non-upgradable and non-manageable  (no expected date)

---

## If you don't trust the current governance

There is nothing that prevents deploying a private ledger on the blockchain.

All deployment instructions are present in the Github repository. And with *Marmalade-NG Bridge*, you can even create a link for your "privately hosted tokens" between the "official" ledger and your private one.
