---
title: "Hacking on Holochain: first impressions"
date: "2018-01-31"
categories: 
  - "cloud"
  - "holochain"
  - "javascript"
  - "network"
  - "programming"
  - "user"
tags: 
  - "cryptography"
  - "decentralisation"
  - "fedwiki"
  - "wiki"
layout: "./_layout.astro"
---

Here's an exciting player in the ascendant decentralised computing space: [Holochain](https://holochain.org/). It's a 'post-blockchain' platform for apps that communicate peer-to-peer, with secure user identities and cryptographically-validated shared data.

---

This week, key Holo people and creative collective [darVOZ](https://www.darvoz.org/) are running a sprint-athon in London. This is where I met them (people in both groups) for the first time, including Holo primary architect Art, and Connor, developer of Holo apps like Clutter (decentralised Twitter clone). And I got my own paws into developing in the system.

It's alpha software, open source (of course), with dev tools that are already suitable for tinkering. They provide testing tools and seem to encourage a test-driven approach. Holo apps have configuration in JSON and code in JavaScript. Running instances of the app run the JS code in their VM. They also can provide a web UI.

Holo development involves writing and reading from the app's DHT, which is a append-only data structure that's automatically shared among connected peer apps that have the same 'DNA', which is a hash of the app's code (Holo loves biological metaphors). Proper handling of this DHT seems to be the new core discipline that Holo demands from developers, and the key to unlocking its peculiar powers.

I've only scratched the surface, and I intend to contribute more to the effort of porting  Federated Wiki to Holochain, which is [in progress](https://github.com/Holochain/fed-wiki). Then I'll see how I can incorporate it into my little side project, the glorious Operating Space initiative (part of which is: this blog).
