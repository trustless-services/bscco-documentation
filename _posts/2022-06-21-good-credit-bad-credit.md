---
layout: post
title: Good Credit, Bad Credit
categories: [Discussion]
excerpt: Credit is the ultimate scaling mechaism. How do we take advantage of it while minimizing systemic risk?
---

## Credit risks in Bitcoin

Bitcoin is trading at 2020 prices again, and credit risk has everything to do with it.
Everyone and their dog has written about the details regarding Luna Terra, Celsius, and
Three Arrows Capital, so I will not bore you with the details. However, it is important
to note that the "cryptocurrency" industry tends to go through these cyclical boom-and-bust
cycles every few years, due to the buildup of leverage and credit in the system.

As is apparent today, bad credit can lead to industry-wide contraction. Even if your
defi protocol is over-collateralized, bad credit that exists externally can cause cascading
liquidations that threaten even the more cautious investors. This is a phenomenon that
appears to be impossible to prevent, and perhaps should even be embraced as a natural
process inherent to free markets.

Indeed, Bitcoin was created in part as a response to fiat bailing out irresponsible
creditors, as evidenced by the message embedded in the genesis block. But sure, while
there is no 'Bitcoin Central Bank' to bail out bad debt, you cannot _prevent_ the
creation of debt in the first place, as debt is also an uncensorable peer-to-peer
concept.

It is understandable that many in the Bitcoin community are reluctant to accept the
existence of credit in a Bitcoin economy, but it is inevitable. And I would like to
add that credit itself also has many benefits - for example, if properly managed and
allocated, it can accelerate good businesses or eradicate bad ones. Thus, the focus
should not be on _preventing_ credit, but on mitigating systemic risks.


## Credit and Lightning

Recently Alex Bosworth commented on the zero-conf channels feature bit to be implemented
soon in Lightning. Zero-conf channels allow consenting peers to consider a channel 'open'
before the transaction has confirmed a sufficient number of times on-chain, and for
other nodes to route transactions over such credit-based channels.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">An interesting aspect to the upcoming LN protocol change to support channels without block confirmations is that you could start spending sats on LN that you don&#39;t really have from the perspective of the Blockchain<br><br>This could drive a UX where you onboard instantly but on credit</p>&mdash; Alex Bosworth (@alexbosworth) <a href="https://twitter.com/alexbosworth/status/1538951444920823810?ref_src=twsrc%5Etfw">June 20, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

For what it's worth, I don't agree with all of Alex's opinions, but I was taken aback by
the amount of pushback he received for welcoming credit on Lightning. The majority of
replies seem to be wary of systemic risk; however, in the case of zero-conf channels,
the only parties at risk are the nodes who share this channel. (i.e., you are not a
direct counterpart of zero-conf channels unless you explicitly consent to it, and your
funds in traditional channels will not be affected by failure of zero-conf channels.)

There is massive room for credit in the Lightning Network, due to its P2P nature being
very complementary to credit, and I believe this is one of the directions Lightning will
take to provide better UX, more functionality, and cheaper fees.

In principle, a good question to ask when evaluating projects that introduce credit
might be: _What is the worst that can happen?_ In Lightning channels, the worst that
can happen is _theft of channel funds_ or more generally _closure in incorrect state_,
but since your Lightning channel is a fully-collateralized affair between just you and
your counterpart, these issues themselves do not have contagious effects (with the 
exception offorced closures due to stuck HTLCs going on-chain, but this is an LN-wide
problem regardless of introducing credit or other features).

As financial use cases of Lightning are explored, there will inevitably be products
that introduce some systemic risk to other such products, but I struggle to think of
examples where regular lightning channels go bust for this reason. Perhaps a rush for
liquidity will cause channel closures _en masse_? I'd love to hear any examples where
the introduction of credit and a subsequent stress event can cause issues with 
Lightning's ability to facilitate payments.