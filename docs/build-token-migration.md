---
id: build-token-migration
title: Token Migrations
sidebar_label: Token Migrations
---

Token ecosystems that currently exist elsewhere would need to be migrated to new infrastructure if this community wanted to
upgrade to a parachain. This article documents some available options for migrating tokens to a new Substrate-based chain
in order to connect to Polkadot as a parachain.

## Why migrate a token?

 - The token ecosystem is already liquid with holders, traders, or users.
 - The developers want to optimize their protocol or application by building it using Substrate.
 - The community wants a trust-minimized way to initiate a new chain.

## Examples of Token Migrations

 - Polkadot is migrating a [Frozen Token][DOT Allocation Indicator] called the DOT Allocation Indicator from Ethereum
 to Polkadot mainnet. The token as it exists currently on Ethereum is a dummy token with transfers disabled as it
 always meant only as a placeholder.
 - Eth2.0 uses a [deposit contract][Deposit Contract] to migrate Eth1.x ether to the new Beacon Chain.
 - Binance [migrated their tokens from an ERC20 variant][Binance Migration] to a native token on Binance Chain,
 although this was done in a trusted method by depositing the ERC20 tokens to Binance.com to be burned and exchanged.
 - [Lockdrops][Lockdrop], although not a pure token migration since the token is returned to the locker after some
 duration of time, can still be considered a type of token migration and a smart alternative for some teams.

## Migrating an ERC20 token to a parachain

The most common use case of a team migrating a token to a parachain will likely be migrating an Ethereum-based token
that conforms to the ERC20 token standard to use the Substrate balances module. There's a few methods that can be
taken to do this, the most common of which would be to deploy a contract onto Ethereum which would lock the balances
of the old token and provide the necessary information for creation of claims on a Substrate chain.

snip snip snip

Another method to making an initial state of balances on a new chain would be scraping the entire balance history
of the ERC20 token in order to generate the balance mapping. Although this is cumbersome to do and likely requires
an archive of the transaction history for the token you want to clone, it has the benefit of being completely trustless
(outside of the trust assumptions already existing on Ethereum). Anyone can scrape the chain for the token balances
at the same block and generate the same initial state of balances.

## Bridge migration

On-going migration of tokens from one chain to another would generally require a bridge between the chains.
The advantage of this approach is that tokens can be continuously swapped over to a running parachain,
but there is added complexity in the design of this approach.


[DOT Allocation Indicator]: https://etherscan.io/token/0xb59f67a8bff5d8cd03f6ac17265c550ed8f33907
[Deposit Contract]: https://community.binance.org/topic/44/binance-chain-mainnet-swap
[Binance Migration]: https://community.binance.org/topic/44/binance-chain-mainnet-swap
[Lockdrop]: https://blog.edgewa.re/whats-a-lockdrop-an-explainer/