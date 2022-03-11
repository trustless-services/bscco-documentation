---
layout: post
title: The Birth of BSCCO
categories: [Discussion]
excerpt: BSCCO enables individual Lightning channels, with their respective nodes' consent, to use mechanisms other than the Bitcoin blockchain as their settlement layer.
---

## Virtual Channels as a scaling mechanism for LN

The Lightning Network is often touted as a cheap payment method that enables micropayments on Bitcoin
without sacrificing on-chain decentralization.

While the latter half is true, whether LN remains cheap indefinitely remains a question.
Routing each payment comes with a risk of channel closure due to technical difficulties or malice.

The following equation must hold for LN to be viable:

(sum of LN fees) > (sum of on-chain fees for LN channels)

And for each HTLC routed, there exists an equation that node operators should consider:

(expected value gained from HTLC) = P(success)\*fee - P(channel close)\*cost > 0

*(Note that this equation ignores the time & resource cost of handling canceled HTLCs,
which account for the vast majority of payment attempts on the network.)*

The problem lies herein; in order to route payments from potential bad actors, what would
the breakeven fee be, and what use cases does that price out? This unfortunate reality stems
from Lightning Channels necessarily using the blockchain as a settlement mechanism to
resolve potential disputes. 

But what if we didn't need to go on-chain? Could we reduce costs & improve LN's efficiency?

## Introducing BSCCO: Trust and the Lightning Network

BSCCO enables individual Lightning channels, with their respective nodes' consent, to use
mechanisms other than the Bitcoin blockchain as their settlement layer. In other words,
you no longer have to use HTLCs, and can instead settle in various ways.

While the Bitcoin blockchain replaces courts and central planners as the final arbiters of
financial records, there are certainly cases where that level of power is not needed.
Maybe you trust your counterparty to honor a contract. Maybe your counterpary is a different
node of yours. In such cases, why use the inflexible Bitcoin blockchain when you could use
credit, stablecoins, custodial solutions, and more?

The idea behind BSCCO is to provide a generalized tool which can be combined with custom
logic to enable different types of record keeping for individual channels.

Check the [roadmap](https://bscco.xyz/roadmap) for planned release dates.