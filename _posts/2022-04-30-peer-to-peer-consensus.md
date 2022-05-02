---
layout: post
title: Peer to Peer Consensus
categories: [Discussion]
excerpt: BSCCO enables individual Lightning channels, with their respective nodes' consent, to use mechanisms other than the Bitcoin blockchain as their settlement layer.
---

## BIP-119 and the difficulty of updating global consensus rules

A new constroversy in the Bitcoin ecosystem is an attempt to introduce BIP-119 (OP_CTV) using the Speedy Trial mechanism, which was used to activate Taproot just one year ago.

Personally, I am a fan of covenants and I support OP_CTV, although I agree that Speedy Trial leaves much to be desired in terms of a coordination mechanism.
The fact that we glossed over Speedy Trial's shortcomings when activating Taproot, which most did not and still do not understand, is painfully obvious today.

Introducing new consensus rules globally is quite difficult in Bitcoin, where many will be opposed form risk aversion or simple apathy.

## Lightning and 'local consensus'

The Lightning Network, comprised of payment channels between two nodes, offers an interesting comparison in terms of applying new consensus rules.
While in practice we use Bitcoin's consensus rules so we can enforce Layer 2 transactions on the base layer, one can imagine other ways of agreeing
with your peer regarding payment channel state.

For instance, we can have channels backed by WBTC on Ethereum, stablecoins issued on Bitcoin, other blockchains, credit, or even databases.
These may lack the robust trustlessness that BTC on Bitcoin offers, but can potentially make up for that in other ways.
This is particularly true if the nodes sharing the channel share some trust, or an external enforcement mechanism (e.g. legal contracts).

The best thing is that Lightning allows such experiments without placing the rest of the network at risk.
And if any liquidity benefits are to be had, those can apply globally.
