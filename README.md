# Cell

## Introduction

Cell is a new NFT protocol that lets you build NFT collections with an extreme level of flexibility, simplicity, efficiency, reusability, scalability, and cross-platform portability.

**It achieves this by adopting a new paradigm:**

> Virtual Machine as a Smart Contract

Instead of deploying a predetermined smart contract logic onto the blockchain, you deploy a Cell virtual machine, and do all the programming logic OUTSIDE the blockchain.

![vm.png](vm.png)

While a traditional NFT contract requires you to **program hardcoded logic BEFORE deployment**, the Cell virtual machine smart contract lets you **program all the token minting logic AFTER deployment.**

This has the exact same benefits of the traditional NFTs but with much more flexibility, extreme efficiency, and ultimate portability.

---


## News & Community

> - **Twitter:** https://twitter.com/skogard
> - **Discord:** https://discord.gg/BZtp5F6QQM
> - **Medium:** https://medium.com/@skogard

---

## Demo

With Cell, all you need to know is JavaScript. With just a couple of lines of JavaScript you can:

1. Programmatically print your own NFT collection
2. Build web apps that let others print NFTs
3. Build agents that print NFTs automatically
4. Build your own NFT platform
5. And many more

Let's try a simple demo. The following web app lets you mint any image on your machine as NFTs, with **just 48 lines of code**:

<iframe width="100%" height="1000" src="//jsfiddle.net/skogard/qf7rvc8L/18/embedded/html,result/dark/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

Here's what it looks like:

![nurondemo.gif](nurondemo.gif)

---

## Quickstart

You can build your own NFT collection in minutes by following the tutorial:

<blockquote><a class='btn' href="https://tutorial.cell.computer">Visit Tutorial</a></blockquote>

<br>

![nuronpreview.gif](nuronpreview.gif)


---

# Problem

Here are some of the limitations of the NFT technology today:

## Inflexible

NFT Smart contracts are like hardware. Once you ship them, the logic is fixed, you can't change them.

![hardware.png](hardware.png)

Just like how a **refrigerator company cannot sell a refrigerator and then somehow remotely morph it to an oven AFTER it's been sold,** the behavior of smart contracts are decided BEFORE they are deployed, and it is difficult to try out different ways tokens can be minted once a contract has been deployed.

Also, the traditional smart contract approach is equivalent to buying a hypothetical refrigerator that ONLY lets you store pre-determined products, like eggs, milk, butter, and so on, but **does NOT allow you to store unexpected items like leftover pizza, flour dough, energy drinks, or cold brew coffee,** because the allowed items are hardcoded into the refrigerator.

Imagine you wanted to run a business with NFT, where you sell NFTs as access tokens to your business.

1. Sometimes you may want to raise the mint price of tokens
2. Sometimes you may want to raise (or lower) the mint price of only one specific token
3. Sometimes you may want to give away the tokens for free, but only the ones you want to give away
4. Sometimes you may want to do a flash sale, but only for a limited time only
5. Sometimes you may want to let people claim tokens only if they fit certain conditions

Trying to hard-code all of this into a contract is not only **inefficient**, but also **infeasible** because **you cannot predict every way you will want to distribute each of your tokens.**

---

## Complicated

![goldberg.png](goldberg.png)

To deploy your own NFT collection with customizable features, there's a lot of things to learn, such as Solidity, IPFS, Web3, and so on.

![tech.png](tech.png)

These technologies collectively have a fairly high learning curve and risk factors, which makes it difficult for anyone to just build their own NFT collection in minutes like they publish a blog post.

There do exist several **service providers** that let you mint NFTs through their platforms, but there are many drawbacks:

1. cannot easily extend your NFT community to include features not provided by the service providers
2. can't build a completely open community around your NFT collections
3. risk censorship 
4. have to rely on a 3rd party infrastructure
5. give up flexibility and customizability

---

## Platform Dependent

There are many blockchains out there. While it is not difficult to write one contract and deploy to many blockchains since many blockchains share the same codebase (EVM or Bitcoin), it is still near impossible to easily port NFTs from one blockchain to another.

![chains.png](chains.png)

The main issue is the **unique resource identifier**. NFTs traditionally have been identified by their location, not their content. 

When we talk about NFTs, we identify them by asking the following questions:

1. **host blockchain:** Which blockchain is it on?
2. **contract address:** Which contract is it on?
3. **tokenId:** What is the tokenId within the contract?

You may have a single image you want to turn into NFT. The `tokenId` for the image will be different depending on where you host the NFT.

Because the **tokenIds are blockchain dependent**, the NFTs using this scheme are naturally blockchain dependent and not easily portable. It is not easy for NFTs to cross over from one blockchain to another.

Practically speaking, this is a very real risk factor for anyone thinking about issuing some valuable asset as an NFT.

- **Uncertainty:** There are a lot of blockchains, and you don't know which one will stick around in the future. Your NFT's value may go to zero if the host blockchain's value goes to zero, regardless of the content stored in the NFT.
- **Switching costs:** Furthermore, if you suddenly need to switch to using another blockchain, you need to re-learn all the tech around the new blockchain. You have to do this for every new blockchain you need to use, which is very inefficient.

---

## Everything Costs Money

With a typical NFT contract, because all the token related logic is stored inside an NFT smart contract on the blockchain, everything costs money:

1. Configuring costs money
2. Adding or updating invites (if you implemented an invite scheme) costs money
3. Creating a token costs money for the creators

![money.png](money.png)

These things add up, and it becomes too expensive to do experiments.

- Doing experiments is expensive
- Creating lots of tokens is expensive
- Trying multiple minting/pricing strategy for the same NFTs is not feasible

The barrier to experimentation is simply too high for NFTs. Even the people who think they are doing fine publishing NFTs are not really taking full advantage of what NFTs can do for them. For example, nobody even imagines making millions of NFTs because of the cost.

---

## Protocol Tax

Most blockchain protocols try to capture value on the protocol level by taking a cut for each usage. Even if they do not do it today, that's often the future goal, which may they implement through a governance vote.

While this makes sense for various protocol types (such as marketplace protocols) and there's nothing wrong with this kind of **"protocol fee tax"**, this does add a layer of psychological barrier and uncertainty if you're thinking about building out your whole universe powered by NFTs, made up of millions and billions of tokens.

---

## No Automation

We take for granted that NFTs are something that can only be created manually by humans, and cannot be automated..

All existing NFT frameworks are focused on creating static NFT collections where humans always need to be involved from the beginning till the end. Even the so-called "generative art" NFT projects require a human being to run a generative art program first, and manually publish the result afterwards.

For example, you cannot have a "robot generative artist" automatically print out NFTs perpetually and make money from the art.

![human.png](human.png)

This is a huge limitation. This means it is not possible for a machine to automatically print out NFTs perpetually without human intervention.

- Imagine you wanted to incorporate NFT into your entire supply chain, where every product produced gets assigned a unique NFT automatically.
- Imagine you wanted to automatically tokenize in-game items as they are generated, either by NPCs or by the user.

Such things are not possible with the existing state of the NFT technology.

---

# Solution

Cell takes a Virtual Machine approach to NFTs.

Instead of building NFT collections that rely on a single blockchain, Cell provides a "virtual machine" that lets you create **universally unique** NFTs that can transcend blockchains.

---

## Dynamic Programmability

Once you deploy a smart contract, you can't change the logic. This is analogous to a calculator being able to do only one thing: calculation.

![calculator.png](calculator.png)

On the other hand, the Cell contract does NOT include any collection specific logic, but includes an interpreter which makes dynamic programmability possible. This is analogous to owning a smart phone. Because each token can be individually programmed AFTER the contract deployment, we have much more flexibility working with NFTs.

We can describe the difference as **Fat Contract vs. Lean Contract**:

![leancontract.png](leancontract.png)

### Fat contract

Traditionally, NFT contracts have been all about **writing as much collection-specific logic into the contract as possible**.


### Lean contract

With Cell, instead of writing all the collection specific logic into the contract, you initially deploy only a minimal **virtual machine**.

Then going forward, this virtual machine contract can interpret and execute signed messages (Offchain token scripts) created by humans or machines to mint them onto the blockchain.

---

## Simple

The Cell virtual machine abstracts out all the messy and complicated details you need to deal with, so you can focus on the real thing that matters: The NFT logic.

![api.png](api.png)

How simple?

### 1. No blockchain connection needed

For starters, **creating tokens DOES NOT even involve connecting to the blockchain network.** You can create tokens completely offline even without an Internet connection.

This means **You do not even need to deal with the blockchain at all!**

This removes all the friction (**learning curve, maintenance, cost, 3rd party dependency etc.**) from the picture, letting you fully control experience around your NFTs, not to mention you can **get started instantly without having to set up some blockchain development environment.**

> **How does this work?**
> 
> Cell unbundles the minting process into two separate steps:
>
> 1. Print tokens
> 2. Mint tokens
>
> The NFT creator just needs to "print" tokens by signing them with keys, and then publish them to the web. It is the "minters" who then mint the printed tokens later, through their browser wallet. Therefore the NFT creator does not need to be connected to the blockchain at all.

### 2. Simple cross platform API

Thanks to the virtual machine, you can create NFTs without needing to understand all the blockchain stuff or other decentralized tech stuff like IPFS.

**All you need to know is JavaScript.**

![code.png](code.png)

### 3. Simple cross language RPC

Or, if you prefer to use any other programming language, you can use your favorite language to make HTTP RPC requests to create tokens locally.

> RPC Specification: https://nuron.cell.computer/#/

---


## Platform Independent

![everywhere.png](everywhere.png)

Cell is a minimal virtual machine in a smart contract. Instead of deploying a fully hard-coded smart contract onto the blockchain, you deploy a virtual machine which can interpret incoming signed messages (called "offchain token script") and mint them into **onchain tokens**.

Also it implements a universal URI to reference each token, which makes every token ever printed with Cell universally unique and platform independent.

Traditionally, NFTs have been uniquely identified by arbitrarily assigning tokenIds such as 1, 2, 3, etc. This works for one chain but does not scale outside of a single chain because you can have different tokenIds for the same token, depending on the blockchain. 

Cell solves this problem with a universally unique tokenId system powered by IPFS (More on this in the "universal token ID" section)

> **NOTE**
>
> Currently Cell is deployed on Ethereum and Ethereum Testnet only, but it has plans to support all EVM compatible blockchains out of the box, and may support non EVM chains in the future.

---

## Unlimited Tokens for Free

Cell was designed to completely get rid of all maintenance costs and minting costs.

- **BEFORE:** With the traditional NFT architecture, everything costs money and you can't easily experiment with different ideas.
- **AFTER:** With Cell, EVERYTHING is free (except for a one time gas fee for when you deploy the contract at the beginning).

![cost.png](cost.png)

1. **One time spend:** The ONLY time you need to spend any money is for paying for gas at the beginning when you deploy the contract. From that point on, everything is completely FREE for the creators because the creators can create tokens, configure them, and do many other things completely outside of the blockchain, thanks to the virtual machine architecture.
2. **Create millions and billions of tokens for FREE:** With the virtual machine approach, the process of "creating" and "minting" of tokens are unbundled, which means the creator can create as many tokens as they want without spending any money, and allow the "minters" to mint the created tokens. The creator can also be the minter, or they can be different parties.
3. **Minters pay:** The creators simply create tokens, as many as they want. It is the minters who pay for the gas for minting the created tokens onto the blockchain, and even this gas fee has been optimized with Cell.
4. **No platform fee:** There is no "platform", and there is no fee charged by anyone. Cell is a 100% open and ownerless system.

---

## Ownerless Public Utility

**With Cell, there is no organization that "owns" and directly makes money from the protocol.**

Cell is a public utility protocol, just like the Internet. No owner, and anyone can innovate on it, and anyone can permissionlessly build on top of Cell to build their own overlay protocols WITHOUT paying some protocol tax to the original inventor.

The mental model here is to build a completely open and fair protocol that everyone can build on top of together collaboratively.

> See the [License & Philosophy](#license-amp-philosophy) section to learn more.

---

## Automation

Most NFTs until now have been **manually created by humans**. This includes even the "generative art" NFTs, because the actual creation of each token is always triggered by human interactions.

On the other hand, Cell is built not only for manual tokenization, but also automated tokenization. It is optimized for automation.

For example, you can build an autonomous tokenization bot that keeps printing tokens algorithmically, based on its interaction with humans, or based on its interaction with other bots.

These tokens then can be minted onto the blockchain.

![automation.png](automation.png)

1. **Automatic tokenization:** Because you do not have to manually approve a signature every time you need to create a token, this can be used to seamlessly tokenize anything on your computer without your intervention.
2. **Embeddable token printer:** Through its abstraction, you can create NFTs without ever directly touching all the complicated technologies like solidity, IPFS, and wallets. This also means it's effortless to embed Cell into ANY program to automatically tokenize anything that happens inside those apps.
3. **Natural resources in a virtual world:** imagine you want to create a virtual world made up of NFTs as natural resources. You can't just create a single "10K item drop" and call it a day. You want the items to constantly be created or morphed, and the minting difficulty increase or decrease based on market conditions. This is only possible when you can automatically tokenize things.


---

# Technology

> Build once, deploy anywhere.

Let's use a Java analogy to explain the "virtual machine" concept for NFT contracts.

![java.png](java.png)

With Java virtual machine, the Java compiler creates a bytecode, which then can run on various virtual machines installed on different platforms like Windows, Linux, Mac, etc.

With Cell virtual machine, the Cell printer module (called [Nuron](https://nuron.cell.computer)) creates offchain token "scripts", which then can be fed to various Cell virtual machines installed on different blockchains like Ethereum, Polygon, etc.

The virtual machine contract is implemented using:

1. Offchain signed tokens (the "bytecode")
2. Onchain smart contract that accepts the offchain signed tokens as input and authorizes minting.

Instead of directly minting onchain tokens, you go through two steps:

1. **CREATE:** you first create the above "offchain token", which is a signed message that describes a token's behavior once minted.
2. **MINT:** then the created JSON object can be submitted to the blockchain to mint the described token.

## Offchain Token Script

If Java has bytecode, Cell has offchain token script.

![offchaintoken.png](offchaintoken.png)

Each token is a JSON object that contains:

1. Token information
2. Minting condition
3. Cryptographic signature

Here's the schema for a token:

```json
{
  body: {
    cid: cid,                           // IPFS CID of the NFT metadata => The NFT information
    id: id,                             // The tokenId of the NFT => can be derived from the cid
    raw: raw,                           // IPFS encoding (true if raw, false if dag-pb)
    minter: minter,                     // who is allowed to mint this token?
    minters: minters,                   // which group of addresses can mint this token? (merkle tree)
    price: price,                       // how much needed for minting this token?
    start: start,                       // when does the minting start? (unix timestamp in seconds)
    end: end,                           // when does the minting end? (unix timestamp in seconds)
    royaltyReceiver: royaltyReceiver    // royalty receiver for this token
    royaltyAmount: royaltyAmount        // royalty amount for this token (out of 1,000,000)
  },
  domain: {
    name: contract_name,
    chainId: chainId,
    verifyingContract: contract_address,
    version: "1"
  }
}
```

Each token (a signed JSON object) is effectively a command you can submit to the "onchain virtual machine", described below.


## Onchain Virtual Machine

![vmcheck.png](vmcheck.png)

The "virtual machine" is essentially an [ERC721 NFT contract](https://eips.ethereum.org/EIPS/eip-721) that executes the **token script** submitted from outside of the blockchain.

It has the following properties:

1. **Clean Slate ERC721:** No collection specific logic (the logic is not hardcoded to the contract, it's embedded in the token scripts that get submited to the VM). Only the ERC721 NFT standard + virtual machine interpreter implementation.
2. **Auth Engine:** Implements the logic that authenticates and authorizes whether to allow an offchain to be minted or not
3. **Minter:** Once the auth check passes, the offchain token can be minted onto the blockchain as an "onchain token". And from this point the token behaves exactly the same as any other ERC721 tokens.

---


## Universal Token ID

One of Cell's main innovations is the **"universal token Id"**, which is a [content addressable](https://en.wikipedia.org/wiki/Content-addressable_storage) tokenId system that **natively** leverages the [IPFS CID](https://proto.school/content-addressing) scheme **on-chain**. So how does this work?

> **In short, the universal tokenId system takes the same IPFS-based `tokenURI` approach adopted by most NFT collections, and applies it even to the `tokenId`s, on-chain.**

### Old way: Location based tokenIds

Most existing NFT contracts use **location based tokenIds**, which means you can only uniquely identify each token location-wise, using the combination of the following "location" attributes:

1. The blockchain it's hosted on
2. The contract address of the collection
3. The tokenId of the token within the collection

We can formulate this **"location based token addressing** in the following form:

```
<chainId>.<contractAddress>.<tokenId>
```

Let's look at an example. The following NFT has a tokenId of **2087** https://opensea.io/assets/0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d/2087

![tokenid.png](tokenid.png)

In this case, we can express this token's location as:

```
1.0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d.2087
```

Where the `1` represents Ethereum ([Ethereum's chainId is 1](https://chainlist.org/))

As we can see, the tokenId **2087** is just an arbitrary number and has nothing to do with the uniqueness of the content itself.

For example, there is no one stopping you from:

1. Using the same image but give it a tokenId of 3000
2. Using a different image to create the token 2087
3. Create a new contract and use the same image to create a "different" token

Basically, the tokenIds are arbitrary and have nothing to do with the uniqueness of the tokens they represent.

Therefore this kind of tokenId system does not uniquely identify digital objects and is not portable across blockchains.

You may be able to make it work on one blockchain, but if you need to migrate to another blockchain in the future (or if you want to use multiple blockchains simultaneously), this tokenId system is the biggest bottleneck to your NFT portability.

### Cell way: Content addressable tokenIds

Cell implements a **Universal tokenId** system with the following properties:

1. **Content-addressable:** tokenIds are deterministically calculated from the token's metadata using the same [multiformats](https://multiformats.io/) algorithm used by the [IPFS CID v1 scheme](https://docs.ipfs.io/concepts/content-addressing/#identifier-formats). 
2. **Universally unique:** Just like how all the files stored on IPFS have universally unique identifiers (CIDs) regardless of where (which machine) they are stored, Cell's tokenIds--regardless of where (which blockchain) they are stored--have universally unique identifiers (tokenIds). The same bored ape NFT will have exactly the same tokenId on Ethereum, Polygon, and any other blockchain, because the tokenIds are not arbitrarily decided but pre-determined based on what each token represents.
3. **The tokenId is the tokenURI:** Typically tokenIds and tokenURIs have nothing to do with each other in NFT collections. You can have a tokenId of 1 and a tokenURI of `ipfs://bafybeicaivkonz2sofegu2thshbeod3723ye2i5c5ivsyhv7gyuyunyyoq`, and they are completely unrelated. But with Cell, the `tokenId` is deterministically derived from the `tokenURI`.
4. **Onchain IPFS resolution:** To implement this, the Cell smart contract has implemented a native on-chain IPFS resolution function that **calculates the tokenURI** instead of storing it, which lowers the gas cost and makes the contract super efficient.
5. **100% ERC721 compliant:** Even while implementing all these schemes, Cell keeps the tokenIds 100% compliant to the [ERC721 standard](https://eips.ethereum.org/EIPS/eip-721). More specifically, every tokenId is a unique `uint256` type identifier derived from the NFT metadata.

Here's a quick overview of how it works:

1. **[offchain]** When creating a token, you supply the IPFS CID of the token metadata
2. **[offchain]** The offchain token printer ([Nuron](https://nuron.cell.computer)) creates a JSON token script object with 2 attributes: `id` and `raw`, which are deterministically derived from the original CID. The `id` is the `uint256` tokenId, and the `raw` is used to store the encoding ("raw" or "dag-pb") of the original IPFS CID supplied.
3. **[onchain]** The created token script is submitted to the onchain virtual machine
4. **[onchain]** The onchain virtual machine runs the authorization logic and if everything is valid, it mints the token with the `id` as the tokenId (as well as storing the `raw` (encoding) attribute internally). Note that we do not need to store a separate `tokenURI`.
5. **[onchain]** Whenever the token is queried, the `tokenURI` attribute is calculated on the fly from the `tokenId` and the `raw` attributes later) through an onchain IPFS CID encoder engine.


---

## NFT Containerization

The Cell framework lets you store and manage everything you need in a self-contained **Workspace**.

This is similar to how application containerization technologies like [Docker](https://docker.com) makes applications portable across multiple platforms by packaging everything into a replicable and portable image:

![appcontainer.png](appcontainer.png)

Just like how Docker packages everything in a self-contained way that can run exactly the same on every platform, Cell packages everything in a self-contained way that can run exactly the same on multiple blockchains (EVM compatible blockchains for now).

![nftcontainer.png](nftcontainer.png)

Here's an example file system created by [Nuron](https://nuron.cell.computer), the "token management system" used by Cell:

```
<YOUR_HOME_DIRECTORY>
│
└── __nuron__
    └── v0
        └── home
            ├── config.json
            └── workspace
                │
                ├── <WORKSPACE 1>
                │   ├── db
                │   │   └── mixtape.db
                │   ├── fs
                │   │   ├── <IPFS file 0>
                │   │   ├── <IPFS file 1>
                │   │   ├── <IPFS file 2>
                │   │   ├── . . .
                │   │   └── <IPFS file n>
                │   └── web
                │       ├── index.html
                │       └── token.html
                │
                └── <WORKSPACE 2>
                    ├── db
                    │   └── mixtape.db
                    ├── fs
                    │   ├── <IPFS file 0>
                    │   ├── <IPFS file 1>
                    │   ├── <IPFS file 2>
                    │   ├── . . .
                    │   └── <IPFS file n>
                    └── web
                        ├── index.html
                        └── token.html
```

Each workspace folder contains everything you need to recreate an NFT collection:

1. **DB:** You can store the offchain tokens as well as token metadata in an SQLite database at `db/mixtape.db`
2. **Files:** Files are stored under the `fs` folder
3. **Website:** Statically generated websites for all your minting needs (you can customize yourself too)

This is extremely portable and flexible.

1. **Publish on the Web:** You can publish your entire NFT collection instantly on the web. Just need to publish the entire workspace.
2. **Publish as Git repository:** The entire workspace is packaged as a git repository, so you can instantly push it to git hosting services like GitHub, GitLab, etc. to version control your NFT collections as well as share them with your NFT collector community (to help them build derivative NFTs, etc.)
3. **Share Privately:** You can even share your NFT collection privately. Just zip the workspace file and send it over email
4. **Share over any Network:** You can use any network transport mechanism to share your NFT collections. For example you can post the entire workspace on [IPFS](https://ipfs.io/), [Hypercore](https://hypercore-protocol.org/), [BitTorrent](https://en.wikipedia.org/wiki/BitTorrent).

Each workspace is 100% **self contained and portable**, and has everything you need to browse and interact with your NFT collections, even including the website. Here's a "search engine" example (https://mferbase.mixtape.network):

![mferbase.png](mferbase.png)


---

# License & Philosophy

When it comes to protocols, **"HOW"** you can use them is as important as **"WHAT"** you can use them for.

**Cell is completely open, free, and has no owner, just like the Internet.**

"No owner" also means EVERYONE is an owner.

## 100% Open

Everything that powers Cell is completely open source with a **completely open license (MIT License)**.

1. **Smart Contract (Backend):** The "backend" is fully open sourced with an MIT license.
2. **Toolchain (Frontend):** Libraries, apps, tools, and everything that powers and integrates with Cell is MIT licensed as well.

Many projects and companies in the blockchain space try to monetize their protocols by open sourcing the protocols but keeping the actual UX closed sourced or not easily accessible (through obfuscation or adding complexity). These are not really "open" because while technically the contract is open source, you still have to rely on the core developer for interacting with the contract.

That's not what Cell is about. Everything around Cell is completely and transparently open sourced so **anyone who adopts the Cell protocol has total control over how they interact with the contract.**



## 100% Free

Most NFT protocol developers charge their users some fee one way or another. 

1. **Tax:** Pay X% of the sales
2. **Pay for usage:** Pay fixed amount for usage
2. **Freemium:** "It's free for now, but eventually we will charge you".

**Cell protocol has NO fee whatsoever.**

We DO encourage everyone to build services, products, or platforms on top of Cell protocol and make money in all kinds of ways including the above.

However it is crucial that **the base layer Cell protocol itself has no fee,** because that's what it was built for.

Cell is effectively a public utility protocol with no strings attached.

> **NOTE**
>
> It's important to note that one of the main reasons why Cell protocol takes NO cut for usage is because we want YOU to make money on top of Cell. Any money you make from using Cell is 100% yours.


## 100% Ownerless

One of the main design goals of Cell is **permissionless innovation.**

To achieve this, the protocol needs to completely get rid of any potential bureaucracy or centralizing factor that may slow down decision making or add psychological barrier when adopting or experimenting with/around the protocol ("am I allowed to do this?", "do I need to join some community or central organization?", etc.).

Cell is a protocol with no owner, and just like how nobody could stop you from publishing a website on the Interent, there's no one who can stop you from doing whatever you want with the protocol based on some "governance".

1. **No 3rd party dependency:** Cell protocol doesn't require a frontend, and does not require a 3rd party API provider. It does not even require connecting to the blockchain to create tokens (including JSON-RPC providers like Alchemy). You can create tokens all offchain (The minters will mint them through their browser connection to the blockchain later, but the NFT creator does NOT need to be connected to the blockchain at every step along the way).
2. **No proprietary UI:** Cell deliberately has no UI that it ships with by default. This is because Cell is too flexible and there can be various ways to create tokens (not just user facing interface, but for example you can build a bot that prints tokens autonomously). This also means there exists no "service provider" that you will have to rely on to build your NFTs. When you build NFTs using Cell protocol, you own the entire workflow from the start to the end. This is important for enterprise use cases since businesses who want to use NFTs for their business may feel uncomfortable relying on some 3rd party API provider, and would like to interface directly with the blockchain at all times.
3. **All will be open sourced:** Even though there is no "official UI" to interact with the Cell protocol, there will be many different ways, and a lot of the standard use cases will be built and open sourced, so people can easily use them.
4. **No governance:** There is no "protocol governers". **Think of Cell as just a tool (like Ruby on Rails, or JavaScript),** instead of some magical protocol community you have to belong to and participate in voting and stuff, just to build some NFTs. No politics, no worries about coin price (there is no coin). Just utility.

## What's the catch?

The immediate question you may ask is: **What's the catch? Why is this so open? Why are you doing this?**

The answer is: **"There is no catch".** Here's the rationale:

1. **Network effect:** Cell is a protocol without scaling limits because of its offchain-first paradigm. Unbounded scalability means there will be plenty of exponential opportunities for everyone IF and WHEN the protocol takes off, just like the early Internet.
2. **Grow the pie:** We want to get there as soon as possible so we can all build extremely powerful things and make a dent in the world, instead of being satisfied with slow innovation and keep doing the same old thing over and over that only serves a small group of people.
3. **Build together:** To achieve this, it is game theoretically more beneficial to eradicate all friction for the very entrepreneurs, artists, developers, creators, and hobbyists who can all build this future together and grow the pie exponentially, instead of trying to capture whatever is extractable from the small pie.


## How to Contribute

Agree with the philosophy and would like to help?

The best thing you can do to help the community is:

1. **Share Cell with others:** Share Cell with as many people as possible so we can grow the community as quickly as possible.
2. **Build on top:** Build NFT collections, frameworks, tools, or whatever.
3. **Share your work:** Open source libraries, frontends, engines, or anything that could help everyone else in the community.
4. **Share feedback:** Share ideas and feedback with the core dev and the community, so we can improve or come up with solutions to problems together.
5. **Network with other NFT creators using Cell protocol:** Cell protocol is extremely interoperable (thanks to the universal cross platform architecture). Let's find ways to collaborate and create synergy together. Join the Discord channel and help each other: https://discord.gg/BZtp5F6QQM


---

# Use Cases

## Ondemand Minting

Instead of pre-populating an NFT collection with your own content, allow users to create their own NFTs through your interactive NFT engine (such as web app, etc).

## Storefront Collections

Build NFTs that have a "storefront" interface, where each token is programmed with a different minting condition.

## Discounts, Giveaways, Raffle, Puzzles

Since you can program each token using the **token script**, and since you can write multiple token scripts for the same token, you can implement all kinds of ways to distribute your NFTs including:

1. **Discounts:** Lower the price for a limited time only using the `start` and `end` opcodes
2. **Giveaways:** Run various giveaway campaigns using the onchain `gift()` function, or using the token script using the opcodes such as `minter`, `minters`, etc.
3. **Puzzles:** Create hash puzzles. The first people to solve the puzzle can mint the token.
4. **Raffle:** Build an offchain raffle infrastructure and use the `gift()` function or the `minter` token script opcode to give away NFTs.

## Automated NFT publishing

Because Cell does not directly rely on the blockchain to create tokens (only need to connect to the blockchain when they need to be minted), you can create a perpetual autonomous NFT engine that keeps printing NFTs algorithmically.

## Autonomous AI NFT Artists

Because everything can be automated, it is even possible to create a fully self-sustainable AI artist that prints NFTs and makes money when people mint the automatically printed NFTs.


## Enterprise NFTs

NFTs are currently used mostly for speculative purposes because of the lack of scalability in most blockchains, as well as the requirement to rely on 3rd party APIs to work with NFTs (such as RPC providers).

1. **Self-sufficient:** Cell has gotten rid of all the 3rd party depenencies so anyone can fully own their entire NFT stack and UX without spending any money to any 3rd party, and without relying on a 3rd party infrastructure for anything.
2. **Scalable:** Because you can create unlimited tokens without being limited by the blockchain bandwidth, you can create millions and billions of tokens without worrying about the cost. For example you can create a million item collection, and only 1000 of them could end up being minted by the NFT minters, but it will still be profitable.

## Private NFTs

You can even create NFTs whose contents are private, while making use of the transparent public blockchains for tracking their ownership.

Because the workspace creates a local file system for all the files WITHOUT needing to publish to the IPFS network, you can easily tokenize private files, which then can be shared among a private group (or a public group of authorized users).

---

# FAQ

## 1. How's it different from lazy minting?

Both lazy minting and Cell use [EIP-712 typed data signature scheme](https://eips.ethereum.org/EIPS/eip-712) to authenticate data offchain.

But they are designed with a completely different philosophy and design goals, therefore result in a completely different architecture from each other.

### a. protocol unbundling

First, most of the popular "lazy minting" contracts (those implemented by NFT marketplaces) are implemented with a method called `mintAndTransfer()`, basically bundling the action of "minting" and "transferring" (via marketplace) in one transaction. 

There are many drawbacks to this approach (such as waste of gas), but ultimately the biggest problem is that the NFT contract is written from a service provider's point of view instead of from an NFT creator's point of view, which results in all kinds of conflict of interest and has various hidden externalities that do not benefit the creators at all.


Cell is a contract of the creators, by the creators, for the creators.

By being laser focused on achieving this goal, Cell can be as simple and efficient as possible. With Cell, it's just `mint`. No funny business, and every feature built into the Cell script exists solely for the creators. It's a minimal independent NFT contract that has ZERO ties to a 3rd party contract like marketplace contracts.

### b. portable

The hard part of building an offchain NFT engine that is absolutely decentralized is NOT the smart contract part. That's the easiest part. The hard part exists offchain, such as dealing with IPFS files, managing offchain tokens, etc.

Cell is not just an onchain smart contract. It's a multi-disciplinary framework that lets you achieve a specific goal: truly own and control your own NFT collection without relying on any 3rd party. In fact, the smart contract code is less than 1% of the entire Cell framework code base. Here are some of the important pieces of the puzzle that make Cell truly portable and decentralizable:

- [Mixtape](https://mixtape.cell.computer/#/): Ultraportable NFT database
- [Nuron](https://nuron.cell.computer/#/): Self-contained NFT file system + wallet RPC engine

These systems collectively provide a containerized NFT repository that can be shared and published easiliy just like sharing a git repository.

This means:

1. You don't have to store your NFT files on someone else's server (and later ask for their permission to retrieve your OWN files through their proprietary APIs)
2. You can publish your entire NFT collection archive so your NFT community can use it or fork it (for building derivative NFTs or building apps around the collection)
3. You don't have to worry about your own app performance being affected by someone else's infrastructure


### c. offchain as the univeresal storage

Lazy minted NFTs are stored on someone else's server. Cell NFTs are stored universally. They are both "offchain", but it's a huge difference because the purpose as well as the outcome are completely different.

With lazy minted NFTs, the "offchain NFTs" are 2nd class citizens. The NFTs technically don't exist until they get minted on the blockchain, and nobody treats the offchain NFTs seriously (Why would they? Until they are settled onchain, they are nothing more than some files stored on a private and centralized NFT marketplace server).

With Cell, the offchain NFTs are the first class citizens. Instead of thinking "we store NFTs on a blockchain", Cell's viewpoint is that it stores NFTs in a universal storage (IPFS-powered) and uses blockchains just to timestamp and trace the flow of the tokens. This is possible because Cell natively implements an onchain IPFS engine as well as offchain tools and libraries that collectively enable a seamless multi-disciplinary IPFS system that spans both onchain and offchain, which is the key to building NFTs that transcend blockchains.

> With Cell, you can store EVERYTHING on IPFS: NFT asset files, metadata files, and even the Cell script itself (since it's just a signed JSON object)

By adopting this opposite mindset ("NFTs are stored universally and blockchains are just used for tracing" vs. "NFTs are stored on the blockchain"), we can expand our imagination to build all kinds of cool open systems around NFTs, such as NFTs that simultaneously reside on multiple blockchains, cross-chain NFT swaps, and more.

---
