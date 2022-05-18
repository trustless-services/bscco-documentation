---
layout: post
title: Blockspace as a Commodity
categories: [Discussion]
excerpt: Blockspace as a commodity clarifies what is necessary for long-term Bitcoin security - arbitrage.
---

## The Two Bitcoin Commodities

Yesterday, I read Mario Gibney's fresh conceptualization of Bitcoin as a producer of two separate goods: BTC and blockspace.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">I believe more and more that to reason effectively about future bitcoin security requires recognizing there are two separate goods produced by the bitcoin network:<br><br>- the asset (BTC): 21 million units ever, hard cap, non-consumable<br>- blockspace: 4 MWU every ~10m, consumable</p>&mdash; Mario Gibney 🇺🇦 (@Mario_Gibney) <a href="https://twitter.com/Mario_Gibney/status/1526361206885388288?ref_src=twsrc%5Etfw">May 17, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

The value proposition of BTC has been clear for years: scarce, uncensorable, predictable money, with a sprinkle of demand as payment for blockspace.

Rather, it is the framing of blockspace as a commodity that is interesting, as Mario puts it: "it has its own value independent of the asset BTC."

## How to value blockspace

Bitcoin miners produce blockspace for a subsidy of newly issued BTC and transaction fees paid by users.
Since the subsidy is paid regardless of the amount of transactions filling the block, the fees are the only payment made for blockspace.

It is also trivial that if a transaction gets included for 1 sat/vbyte, 1 vbyte of blockspace is valued at 1 sat or less at that time.

Blockspace as a commodity has some interesting characteristics. One is its inelastic supply; production cannot respond to changes in demand.
Additionally, it cannot be preserved, and must be used when purchased. You cannot include new transactions in old blocks, no matter how empty they were!

Therefore, the price of blockspace is fundamentally volatile, and lack of demand can cause the it to remain at near-zero levels, as we have seen lately.
Even during bull markets, we see long periods of low prices occasionally broken by spikes to 100+ sats/vbyte.

## Can we profit from this volatility?

This volatility raises a question: could we purchase blockspace when it is cheap and use it when it is expensive?

Intuitively, this seems impossible. Payment for some blockspace and its use (inclusion of a transaction) have an atomic relationship.
However, with a little creativity, there is a way. If the UTXO created by a transaction represents a future opportunity, you could preserve its
utility for later.

In the current Lightning Network, channels must provide proof of a funding UTXO on-chain as a spam filter when announcing their existence
or updating their fee. Nothing prevents you from creating funding UTXOs in advance and announcing the channel at a later time. 

Of course, there is little point in doing this. If you are locking up your funds in the first place, why not just announce the
channel? In order for the UTXO to represent future opportunity, we need to be able to open a channel with _whomever we want_ at a later time.

We can achieve this by separating the concepts of funding UTXO owner and channel operator, something made possible by BSCCO and channels that
do not rely on HTLCs on Bitcoin to function. High on-chain fees keeping you from opening a channel? No problem, just lease a UTXO and set up a
BSCCO channel with a willing peer, no on-chain interaction needed.

## Long-term implications

In recent conversations regarding Bitcoin's long-term security, a repeated concern raised by critics is if demand for blockspace will be sufficient.
Low miner compensation can result in malicious miners attempting double spends, either for their own gain or for bribes.

While I believe that we will simply learn to wait for as many confirmations as necessary based on the situation, just as we should be doing now,
UTXO leasing schemes can potentially provide some baseline demand for "cheap" blockspace that can be reused in the future. This should also help
ease spikes as some demand for current blockspace can instead be directed towards leasing old blockspace.

While I am unsure what percentage of low-priced blockspace demand will be added by such schemes in the distant future, I believe there are many unexplored
use cases this concept can enable. I hope that such schemes will further ease the concerns some may have regarding Bitcoin's sustainability decades in the future.
