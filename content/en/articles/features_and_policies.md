---
title: "Features and standard policies list"
author: "Pascal"
description: "List of features provided by Marmamalade"
date: "2024-01-01"
toc: false
thumbnail: /policies.png
weight: 180
---
Marmalade standard Features and policies

---

<style>
.bi {
  display: inline-block;
  height: 3.0rem;
  width: 3.0rem;
  top: -0.25rem;
  position: relative;
}
</style>


## Standard

### Collection

{{% icon collection %}} Create collections of tokens

### Blacklist

{{% icon dash-circle %}}  Create blacklistable tokens

### Guards

{{% icon shield-lock %}} Protect a token by a set of guards

### Extra policies

{{% icon diagram-3 %}} Extends tokens features by a set of team proposed policies.

### Instant mint

{{% icon database-add %}} Mint the tokens in the same transaction as they are created

### Non fungible

{{% icon database-add %}} Enforce non fungible tokens

### Fixed issuance

{{% icon database-add %}}Control the issuance of poly-fungible tokens

### Trusted custody

{{% icon house-lock %}} Transfer tokens to custodials (lending/farming platforms, centralized marketplaces, ... )

### Fixed sale

{{% icon cart4 %}} Sell tokens at a fixed price


### Auction sale

{{% icon cart4 %}} Sell tokens in standard auction

### Dutch auction sale

{{% icon cart4 %}} Sell tokens in dutch auctions (time decreasing price, with geometric progression).

### Royalty

{{% icon piggy-bank %}} Charge royalty for each sale

### Adjustable Royalty

{{% icon piggy-bank %}} Charge royalty for each sale. The royalty rate can be be further adjusted by the creator.


### Marketplace

{{% icon shop %}}  Allows marketplaces to charge a fee. Fee can be shared between the "*buying*" marketplace, and the "*selling*" marketplace.

### Disable sales

{{% icon lock %}} Prevent a token for being sold

### Disable transfers

{{% icon lock %}} Prevent a token for being transferred

### Disable burn

{{% icon lock %}} Prevent a token for being burned

---

## Extended policies

### Currency whitelist

{{% icon currency-exchange %}} Whitelist some currencies authorized for a token sale

*Not currently released on Mainnet*

### Donation

{{% icon piggy-bank %}} Donate 0.1 KDA on each sale for solidarity.

*Not currently released on Mainnet*

### Multi Sellers

{{% icon diagram-2 %}} Divide the sell price between a list of sellers

*Not currently released on Mainnet*

### Lottery

{{% icon cart4 %}} Create a lottery to win the NFT. Each potential buyer bids a certain amount. The winner of the NFT is randomly drawn.

*Not currently released on Mainnet*

*Unsafe*
