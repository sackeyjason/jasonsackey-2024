---
title: "Love in the age of decentralised personal computing"
date: "2018-02-19"
categories: 
  - "holochain"
  - "network"
  - "urbit"
tags: 
  - "cryptography"
  - "dating"
  - "decentralisation"
  - "privacy"
  - "social-media"
layout: "./_layout.astro"
---

How will the distributed network revolution impact online dating?

Services like OKCupid, Tinder and Match.com operate on centralised, client-server models. Daters sign up to a service and give it some personal information: photos, biography text, age, sex, location, and preferences. The service stores the info, and gives the user an interface for checking out profiles of other, algorithmically-chosen, suitable daters and starting to chat with them. They typically run on revenue from advertising, and/or charge fees from users.

Commercial online dating services offer security, not through encryption, but being responsible for kicking out miscreants. They set and enforce rules for decent conduct, to tackle problems like fake profiles, inappropriate photos, scams, stalking, harassment, and catfishing. Bad offline behaviour, too, may be subject to their disciplinary measures: [Facebook bans all sex offenders](https://www.facebook.com/help/210081519032737/), and several dating apps (e.g Tinder and Bumble) require the use of a Facebook profile for identity verification. [OKCupid banned some dude for involvement in neo-Nazi/alt-right activities](https://theblog.okcupid.com/okcupid-has-zero-tolerance-for-racism-ffaae9f2d800).

The centralised structure of these services is not merely a technical implementation detail, but the basis for enforcing the social orderliness that makes these platforms worth using in the first place. That is, some degree of safety, through each of the platforms' benevolent dictatorial oversight.

What would a distributed, decentralised platform for online dating offer? Secure, end-to-end encrypted messaging is a plausible feature. Assuming we want an alternative that appeals to an audience wider than a bunch of crypto-nerds, this isn't enough to compete. How would it be made _safe_?

It's a challenge! I think a decentralised system can tackle it. Eventually, it'll even beat centralised ones.

I first started thinking about the shape of a possible solution in terms of Urbit. I more recently learned about Holochain, which also seems to have the right ingredients for a similar approach. Either of those platforms can straightforwardly support a peer-to-peer, free-for-all of unfiltered, encrypted communication. This is clearly insufficient as a protocol to support even dozens of strangers socialising. From [Urbit literature](https://medium.com/@urbit/design-of-a-digital-republic-f2b6b3109902):

> Bringing people together is an easy problem for any social network. The hard problem is keeping them apart. In other words, the hard problem is _filtering_. Society is filtering.

I propose this decentralised dating approach: daters _and matchmakers_ are peers on a network.

In a centralised dating platform, there's just one matchmaker. It owns and runs the platform. Its job is to virtually introduce potential matches to one another, and keep the platform safe (by setting and enforcing rules).

In a decentralised system, any peer on the network can set themselves up as a matchmaker. Daters on the network would pick and choose one or several matchmakers, entrusting them with the sorts of responsibilities that users of OKCupid, Tinder, etc. do with those platforms. Namely:

- Save a copy of my dating profile -- perhaps one conforming to a provided schema.
- Show me other profiles.
- Put me in contact with other suitable people connected to you (--suitability as determined by some rules of engagement: profile info matching our expressed preferences. But the personal touch added by a personal matchmaker opens the doors to possibilities beyond algorithmic box-checking...)

Who are these matchmakers? Some could be unpaid volunteers, just there to help get dates for their friend: matching them with friends, or friends-of-friends. Or fellow hobbyists, or fellow churchgoers, or fellow professionals in some field, or associates of any other sort.

(Matchmakers, crucially, would _not_ control the user interfaces. Users ultimately control their own UIs. They're modifiable programs that sits on the users' own machines.)

This system is also open to the possibility of commercial matchmaking operations. They'd compete on the basis of their respective reputations for offering a high-quality service, and differentiated target audiences. They could also co-operate, perhaps by merging together their respective pools of clients. One would expect commercial information-sharing of this sort to be regulated by [data-protection laws.](https://www.cennydd.com/writing/a-techies-rough-guide-to-gdpr) But what about when it's a non-commercial operator? It seems that non-legislative means will be needed: protocols, filtering, and reputation systems for encouraging trustworthy matchmaking standards.

But perhaps much of this will prove unnecessary when we've got robust distributed social networking, one key factor being an identity system. Holochain is building its own [distributed public key infrastructure](https://github.com/Holochain/dpki). When you join Urbit, you get a [new alien pseudonym](https://urbit.org/posts/address-space/). Probably a _planet_ like '`~mighex-forfem`', which is a 'permanent' personal identity (and eventually, an asset with a price tag).

These potentially can serve as the basis for a range of multi-purpose reputation systems. They would provide assurances that could relieve some of the burdens from matchmakers, and users choosing matchmakers. And, perhaps, sometimes make dedicated matchmakers redundant? I suspect decentralised networking will make many centralised dating sites obsolete, but perhaps I'm too conservative in my estimations. It could make 'online dating' as such obsolete: absorbed into general-purpose social networking.

The system of 'daters' and 'matchmakers' could also be applied to non-dating contexts, e.g. professional networking. This is what one would expect from general-purpose social networking. Bumble has already expanded its functionality to include networking for business  and friendship. It may well try to grow and subsume the functionality of Facebook, LinkedIn, and Meetup.com. There's no limit to the potential voraciousness of any of these platforms. For the as-yet most highly-evolved apex of this trend, [see WeChat (video)](https://www.nytimes.com/video/technology/100000004574648/china-internet-wechat.html). WeChat is centralised.

## Meanwhile in decentralised tech love

[LegalFling](https://legalfling.io/). An app that records sexual consent on a blockchain. Ridiculous, sounds like a joke, but here we are.

[Luna](https://www.meetluna.com/). A blockchain-based dating app. Seems more convoluted and centralised than the scheme I've outlined, but doesn't seem completely stupid. Maybe it'll work.

[Marriage recorded on blockchain](https://news.bitcoin.com/cross-border-love-on-the-blockchain/). This sounds like another joke, but it really makes sense. One can imagine a cryptocurrency that automatically reroutes funds sent to either of two wedded wallets into a couple's shared wallet. And then, that wallet's contents being split up according to a smart contract, when a divorce is marked on the chain. No lawyer required!

The [decentralised social protocol Scuttlebutt](https://www.scuttlebutt.nz/) explains itself with a [love story (video)](https://vimeo.com/236358264).
