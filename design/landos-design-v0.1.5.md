# Landos — Sovereign Land Blockchain
## Design Document v0.1.5

**Status:** Draft — thinking document, not a final spec  
**Date:** 2026-06-01  
**Name:** Landos (LAND OS)  
**Token Ticker:** LOS  
**Steward:** TBD — creator acts as temporary steward only  

---

## 1. The Problem

Land ownership today is entirely dependent on governments and institutions:

- Registries are siloed, incompatible, and inconsistent across countries and regions
- Records are vulnerable to corruption — officials can alter, delete, or forge them
- People with money and power can take land from people without power
- In many parts of the world, records barely exist at all
- Families who have occupied land for generations can lose it because a document disappears or a registry entry changes

These are not edge cases. They are the everyday reality for hundreds of millions of people — farmers, indigenous communities, families with no legal recourse when someone more powerful decides to take what is theirs.

**The core problem: land ownership is controlled by whoever controls the registry. And registries can be corrupted.**

There is a second, equally important dimension to this problem: the majority of the world's land wealth is economically inert. Hernando de Soto estimated in 2000 that the world's poor hold approximately **$9.3 trillion in "dead capital"** — land and assets that have real value but cannot be used economically because they lack formal recognition. This land cannot be used as loan collateral. It cannot attract investment. It cannot be formally sold or transferred. It simply exists, valuable but locked.

**The compound problem: land is both insecure and economically dead for the people who need it most.**

---

## 2. The Vision

Two bodies of work define what Landos is trying to build.

**Bitcoin** proved that a monetary system could exist outside of government and institutional control. People could "be their own bank" — hold value in a wallet secured by cryptography, with no third party required. Bitcoin did not ask central banks for permission. It simply existed. And over time, as more people trusted it more than the alternative, it gained legitimacy from the ground up.

**Hernando de Soto** proved, through decades of fieldwork across developing economies, that the absence of formal property rights is one of the primary mechanisms that traps people in poverty. Formalizing ownership — creating a recognized, legible record — converts dead capital into live capital. It unlocks borrowing, investment, trade, and intergenerational wealth transfer. The record itself is the economic transformation.

Landos applies both principles to land.

**Landos makes it possible for people to be their own title registry — and for that registry entry to function as live economic capital from the moment it is created.**

A person's land ownership is recorded on a sovereign, decentralized blockchain that no government, corporation, or powerful individual controls. The record is permanent, immutable, and cryptographically verifiable. It cannot be altered by a bribe. It cannot be erased by a corrupt official. And it immediately makes the land legible to global capital markets — enabling economic participation that was previously impossible.

---

## 3. The Name

**Landos** — settled name as of v0.1.2.

**LAND OS** — the full concept behind the name.

Origins and meaning:
- **Land** — the subject is right in the name. No ambiguity.
- **OS** — operating system. Landos is not just a registry. It is the foundational layer that everything land-related runs on top of — the same way DOS was the foundational layer that everything else was built on.
- **Landos** — echoes Landon (human, grounded) and Thanos (powerful, inevitable, cannot be stopped). Still contains DOS.

The OS framing matters philosophically. An operating system does not do one thing — it provides the foundation for an unlimited number of things to be built on top of it. Landos starts with ownership records. Over time it can become a complete land knowledge and management system: ownership, tenure, boundaries, history, identity, community, rights. Whatever people need to build on top of it.

Just as no one in 1984 knew what would eventually run on DOS, no one today can fully predict what will be built on LAND OS.

---

## 4. Core Philosophy

### 4.1 Landos Belongs to No One

The creator of Landos is a temporary steward. Like Satoshi Nakamoto, the goal is to build something that eventually runs without its creator. The moment a central person or organization controls Landos, it becomes a target — for legal pressure, for corruption, for shutdown.

Landos is designed from the start to be ownerless infrastructure. A public good. A layer of the internet, not a company.

### 4.2 All Land Already Exists

Unlike most blockchain systems where assets are created over time, **all land on Earth already exists** and is pre-represented on the Landos blockchain at genesis.

This mirrors Bitcoin's supply model: all 21 million BTC exist in the protocol from the start — miners don't create them, they unlock them. Similarly, Landos doesn't require land to be "added" to the chain. Every parcel on Earth is already there. The work is in assigning ownership to the real owners.

This matters philosophically: no one is granting you anything. You are coming to claim what is already yours on the chain.

### 4.3 Not a Replacement — A Parallel Truth

Landos does not need governments to recognize it on day one. It runs alongside existing systems, offering an independent record that cannot be corrupted.

This is not an anarchist project — but it is not a cooperative one either. Landos does not seek government partnerships or wait for institutional approval. It simply exists. Like Bitcoin, which never asked central banks for permission and now has nation-states holding it as a reserve asset, Landos is designed to earn legitimacy from the ground up — through adoption, through trust, through the undeniable fact of a record that works.

Governments do not need to embrace Landos for it to function. But as more people register land on the chain, as more communities rely on it, and as the record proves itself more reliable than the alternatives, governments will find themselves relating to Landos on its terms — not the other way around. The countries that need it most are the ones whose existing registries have already failed. They have every reason to adopt a system that solves their problem. The door is open. Landos does not knock.

### 4.4 Land Belongs to Communities

Land is not purely an individual thing. A person owns land within a community. Their neighbors know them. The town knows who lives where. The community has memory that no individual has. Landos encodes that social reality into the protocol — not as a workaround, but as a foundational design principle.

Communities in Landos are not defined by governments or institutions. They emerge organically from geography — from people who share proximity and have real relationships with each other.

---

## 5. The Landos Foundation

### 5.1 Why a Foundation Exists

Landos is designed to be ownerless infrastructure — but ownerless infrastructure still requires humans to do certain work, especially early on. Support workers need to be hired. They need to be paid. Edge cases need human review. The protocol needs to be maintained and developed before it can fully govern itself.

The Landos Foundation exists to handle these practical functions. It is not a governing body. It does not control the protocol. It does not own the chain. It is a minimal operational wrapper — the smallest possible organization that allows the network to function while it grows toward true decentralization.

The goal of the Foundation is to make itself unnecessary. As the network matures, its functions are progressively transferred to protocol-level automation, community governance, and the decentralized node network. The Foundation winds down as Landos grows up.

### 5.2 What the Foundation Does

The Foundation's mandate is narrow and explicitly limited:

- **Support operations** — hiring and managing human support workers who handle escalated recovery cases and edge cases that automation cannot resolve
- **Paying support workers in LOS** — the Foundation holds a LOS allocation for this purpose; workers are compensated from this allocation
- **Early protocol stewardship** — coordinating initial development, documentation, and tooling before community governance is operational
- **Stakeholder communications** — serving as a contact point for external parties (developers, communities, governments) during the early adoption phase

### 5.3 What the Foundation Does Not Do

- It does not control the protocol or have authority over the blockchain
- It does not hold user funds, keys, or land records
- It cannot alter, freeze, or revoke land registrations
- It does not make governance decisions — those belong to the protocol and the community
- It does not have veto power over node operators or validators

### 5.4 Accountability

The Foundation's LOS allocation, expenditures, and operational decisions are publicly documented. Its mandate is defined and limited at the protocol level — not by its own charter alone. Over time, as governance mechanisms mature, the community can reduce or restructure the Foundation's role through the standard governance process.

The Foundation is a temporary scaffold, not a permanent structure.

---

## 6. The Token Model

### 6.1 Three Layers, Not Two

Previous versions of this document described two instruments — the Land Record NFT and LOS. Through further design work, it became clear that there is a more foundational layer beneath both: the **Parcel Record**.

Landos is built on three layers:

1. **The Parcel Record** — the canonical on-chain fact that a piece of geography has been registered and validated. This is the foundational primitive of the entire system — not an asset you hold, but a registered record that everything else is built on top of. Like a UTXO in Bitcoin, the Parcel Record is what the protocol reasons about at its core.
2. **The Land Record NFT (Deed)** — the on-chain ownership record for a specific Parcel Record. This is what a landowner holds. To a non-technical user, this is simply "the deed."
3. **LOS** — a fungible token representing economic exposure to the global land value unlocked by Landos.

The Parcel Record is invisible to most users — a farmer in Kenya doesn't need to know it exists. They just know they have a deed. But developers and institutions building on top of Landos interact with the Parcel Record directly.

These are modeled on established patterns in both traditional finance and the web3 RWA (Real World Asset) space. In traditional finance, you can own a specific property (deed) or invest in real estate value without owning property (REIT). Landos brings both instruments on-chain, anchored to a sovereign geographic record that neither traditional finance nor previous blockchain projects have had.

---

### 6.2 The Parcel Record

The Parcel Record is the foundational primitive of Landos. It represents the on-chain existence of a specific piece of geography — nothing more, nothing less.

Key properties:
- **One Parcel Record per geographic location** — identified by its canonical Coords URI
- **Not a tradeable asset** — the Parcel Record is a protocol-level fact, not a token. Ownership is expressed through the Land Record NFT that sits on top of it.
- **Permanent lineage** — a Parcel Record is never silently modified or deleted. Every change leaves a traceable on-chain history.
- **Foundation for all other instruments** — the Land Record NFT, mortgages, leases, easements, and any future instruments are all anchored to a Parcel Record.

**Parcel lifecycle:**

Parcel Records are not static. Real-world land changes, and the protocol must handle it faithfully:

- **Subdivision** — one parcel split into two or more. The original Parcel Record is retired; new records are created. The transaction history preserves full lineage.
- **Consolidation** — two or more adjacent parcels merged into one. Original records retired; new record created with lineage intact.
- **Boundary adjustment** — a shared boundary between two parcels is moved by mutual agreement. Both Parcel Records are modified, not retired. Requires neighbor quorum from both sides and governance approval above a size threshold.
- **Contested boundary change** — one party claims a boundary has changed; the other disputes it. Feeds directly into the contested/disputed status system.

A Parcel Record should never disappear or silently change. Someone tracing land history 50 years from now should be able to follow every split, merge, and boundary shift through the on-chain record.

---

### 6.4 The Land Record NFT (Deed)

The Land Record NFT is the on-chain deed. It is a non-fungible token uniquely tied to a specific Parcel Record, identified by its Coords URI.

Key properties:
- **One NFT per parcel** — each unique piece of land has one canonical NFT
- **Keyed to the Coords URI** — the NFT metadata contains the canonical location identifier, stored permanently on-chain (never off-chain)
- **Ownership = holding the NFT** — whoever holds the NFT is the registered owner on the Landos chain
- **Transfer = standard NFT transfer** — signed by the current owner's private key, recorded on-chain
- **Fractional ownership** — handled through semi-fungible token standards (e.g., for apartments, shared family land, building floors); design TBD
- **Status** — the NFT carries the parcel's current ownership status (Unregistered → Claimed → Pending → Partial → Confirmed → Contested → Reverted)

The Land Record NFT does not require LOS to exist. It does not change in value based on LOS price. It is the land record — pure and simple.

---

### 6.5 LOS — The Economic Layer

LOS is a fungible token. It is not a deed, and holding LOS does not give you ownership of any specific piece of land.

**What LOS represents:**

LOS captures the economic value created by Landos's core function: converting dead capital into live capital. Every parcel registered on Landos moves from economically inert to economically active. That transformation has real value — globally estimated at trillions of dollars in currently unlocked potential. LOS is the instrument through which that aggregate value is accessible to anyone in the world.

This is analogous to a global land REIT — not tied to any single property, but representing a stake in the aggregate economic activity that Landos enables across all registered land worldwide.

**What gives LOS value:**

- Every land registration, transfer, validation, and transaction on Landos requires a small fee paid in LOS
- Node operators earn LOS for running the network (see Section 7)
- Validators earn LOS for completing validation work
- As more dead capital is formalized through Landos, network activity grows, LOS demand grows
- The connection to global land value is real but indirect: LOS reflects the aggregate economic activity of the world's land being made legible and tradeable

**What LOS is not:**

- It is not a deed or a title to any land
- Holding LOS does not give you any rights over any specific parcel
- It is not a stablecoin or pegged to any fiat currency

**Investor access:**

An investor anywhere in the world who wants economic exposure to the global land market — particularly the massive dead capital being unlocked — can hold LOS without owning or managing any property. This is the equivalent of a foreigner investing in a REIT rather than buying property directly.

---

### 6.6 Token Supply

**Land Record NFTs:** Supply is determined by geography. The surface of the Earth contains approximately 148.94 million km² of land. The exact NFT supply and parcel sizing methodology is TBD — to be defined in a separate parcel definition document.

**LOS:** Total supply, distribution schedule, and the split between node rewards, validator rewards, Foundation allocation, and any genesis allocation are TBD. The supply model will follow Bitcoin's principle of fixed, programmatic, non-human-controlled issuance.

---

### 6.7 Registration Fees and Access

Registering land on Landos requires a small fee paid in LOS. This fee:
- Compensates node operators and validators who do the work of securing the network
- Creates a cost barrier against spam registrations
- Is designed to be minimal — not a barrier to the people Landos exists to serve

**Fee assistance mechanism:** There must be a protocol-level mechanism by which a landowner who cannot afford the registration fee can access funds to cover it. The design of this mechanism is TBD. Possible approaches include community hub funds, validator subsidies for underserved regions, and sponsored registration programs. This is a priority design item.

---

## 7. Node Economics

### 7.1 Nodes Are the Network

The strength of Bitcoin is not just its cryptography. It is the tens of thousands of independently operated nodes distributed around the world, each one enforcing the rules and maintaining the complete record. No single actor can shut down what has no center. No regional actor can corrupt what every node in the world can verify.

Landos requires the same foundation. Nodes are not an implementation detail — they are the security model.

### 7.2 Node Types

Landos uses three node types:

**Full Nodes**
- Store the complete Landos blockchain
- Independently validate every transaction and enforce every protocol rule
- No node is trusted — every node verifies everything itself
- Highest hardware requirements
- Earn the highest LOS rewards
- The backbone of the network's security

**Light Nodes (SPV)**
- Store block headers only
- Verify specific transactions against Merkle proofs provided by full nodes
- Trust the chain's proof-of-work, not any individual node
- Can run on standard consumer hardware (laptop, Raspberry Pi)
- Earn smaller LOS rewards than full nodes
- Lower barrier to entry — critical for global distribution

**Relay Nodes**
- Store some or all of the chain and serve data on request
- Do not validate — they are pipes, not authorities
- A full node or SPV node receiving data from a relay node verifies it independently; the relay node cannot lie in a way that survives verification
- Earn modest LOS rewards for bandwidth and data availability
- Earn nothing for validation, because they perform none

There are no geographic or regional node types. A node that holds only a subset of the chain cannot independently verify the full record — it must trust someone else's view of the data it doesn't have. That trust is an attack surface. In regions where corruption is most likely, local control of a regional node is exactly the threat Landos is designed to eliminate.

### 7.3 How Nodes Earn LOS

Node operators earn LOS through two mechanisms:

**Uptime and availability** — nodes that remain online and serve the network reliably earn LOS proportional to their availability. This incentivizes a stable, always-on network backbone.

**Validation work** — nodes that participate in confirming land claims, processing registrations, and executing validation tasks earn additional LOS for that work. Relay nodes earn for availability only — they perform no validation.

The specific reward amounts, the ratio between uptime rewards and validation rewards, and the schedule for both are TBD. The design principle is that running a node should always be economically rational once LOS has meaningful value, creating a self-reinforcing network effect.

### 7.4 Making Nodes Easy to Run

Previous blockchain projects — including Bitcoin in its early years — suffered from node operation being too technically demanding for ordinary people. Landos must make node operation accessible. This means:

- Simple installation with minimal technical knowledge required
- Clear documentation and tooling
- Light and relay node options for lower-powered hardware
- A path from zero to running a node that any technically curious person can follow

The easier it is to run a node, the more nodes exist. The more nodes exist, the more secure and decentralized the network. This is a design and UX priority, not just an engineering consideration.

The chain will grow large over time as land records accumulate. This is a scaling and hardware problem — to be addressed through state pruning, compression, and the long-term decline in storage costs — not through data fragmentation or geographic sharding.

---

## 8. Land Identification

### 8.1 The Canonical Identifier — Coords URI

Every piece of land on the Landos chain is identified by a **Coords URI** — an open, CC0, tamper-evident coordinate identifier defined by the Coords protocol (github.com/coordsapp).

Example:
```
coords:l1:v1:37.774900,-122.419400,15.25*1c86401e
```

This identifier:
- Belongs to no government or institution
- Is derived purely from geography (WGS84 coordinates)
- Includes a checksum for integrity verification
- Is universally unique — one location, one ID, forever

### 8.2 The XREF — Cross-Reference System

Not everyone comes to Landos with a Coords URI. A farmer might have a government parcel number. A community might have an Open Tenure record. A landowner might only have GPS coordinates.

The **XREF** (cross-reference system, name TBD) maps every major spatial identification system back to a single canonical Coords URI. Any ID from any system resolves to one Landos location.

See: `xref-design-v0.1.0.md` for full XREF design.

Supported systems include H3, What3Words, WGS84, GeoJSON, Open Tenure, Plus Codes, MGRS, postal addresses, and national cadastral registries.

### 8.3 Geographic Foundation

Landos builds on the following open geographic standards:

- **WGS84** — the universal GPS coordinate standard used by every device on Earth
- **GeoJSON (RFC 7946)** — open internet standard for encoding geographic boundaries
- **H3 (Uber)** — open source hexagonal grid for dividing Earth into hierarchical cells
- **Coords protocol** — canonical URI encoding for precise location identification

---

## 9. Connected Systems

### 9.1 Bitcoin Anchor

Landos records are periodically anchored into the Bitcoin blockchain using **OpenTimestamps** — an open protocol by Bitcoin developer Peter Todd.

This means even if Landos itself were attacked or destroyed, proof that land records existed at specific moments in time lives permanently in Bitcoin. No one can erase it.

Bitcoin is the trust anchor. Landos does not depend on any other crypto project or chain.

### 9.2 Open Tenure (FAO)

Open Tenure is a mobile application developed by the UN Food and Agriculture Organization that allows communities to document land rights on the ground using basic mobile devices, GPS, photos, and community consensus.

Open Tenure solves the human, on-the-ground documentation problem. Landos solves the permanent, immutable record problem. Together:

- Open Tenure captures and validates community land claims in the real world
- Those validated claims are written to the Landos chain via the XREF
- The record becomes permanent and sovereign

Open Tenure handles the people layer. Landos handles the truth layer.

### 9.3 Decentralized Identity (DIDs)

Land ownership on Landos is tied to **W3C Decentralized Identifiers (DIDs)** — an official internet standard since 2022. A DID is a self-sovereign identity that no central authority controls.

A person owns their Landos identity the same way they own their land — through cryptography, not permission.

---

## 10. Consensus Mechanism

### 10.1 Status

The Landos consensus mechanism is under active development. No final design has been selected. What follows are working concepts.

### 10.2 Base Layer — Tendermint BFT

Landos uses **Tendermint BFT** (Byzantine Fault Tolerant) consensus as its base layer, implemented via the **Cosmos SDK**. Tendermint is proven, energy-efficient, and handles the hard distributed systems problems — node agreement, fork resolution, network partitions — without requiring proof of work.

Cosmos SDK is purpose-built for application-specific blockchains. It handles the networking and consensus layer, allowing Landos to focus on what makes it unique: the Proof of Land application layer on top.

### 10.3 Application Layer — Proof of Land

On top of Tendermint, Landos runs **Proof of Land** — a novel consensus model where validator weight is determined not by liquid token stake alone, but by a combination of:

- Registered land on the chain
- Accumulated habitation score
- Neighbor quorum attestations
- Community hub standing

Validators are landowners. Their stake is tied to something real, finite, and meaningful. Dishonest behavior risks that stake. The people who secure the network are the people whose land lives on the network — they have the most to lose if it fails.

### 10.4 Guiding Principle

No single mechanism makes Landos secure. Like Bitcoin — where the combination of proof of work, longest chain rule, and economic incentives creates robustness — Landos uses a combination of mechanisms specifically designed around land, human presence, and community knowledge.

---

## 11. Ownership Validation Mechanisms

Establishing that a person owns a piece of land is a human and social problem, not just a technical one. People know who lives where. Communities know their own members. Landos encodes that social knowledge into the protocol cryptographically.

No single mechanism is sufficient on its own. Together they are very hard to game. A bad actor trying to falsely claim land would need to fake physical presence, corrupt neighbors, forge delegated vouchers, and spoof identity verification simultaneously — across multiple independent systems.

### 11.1 Proof of Habitation

A landowner proves physical presence at their registered land over time using a mobile app connected to the Coords location of their parcel. Every verified period of presence accumulates into a habitation score.

Key properties:
- **Time is the proof** — presence accumulates over days, months, years
- **Cannot be faked at scale** — a bad actor can sit on a corner of land for an hour; a real owner has been there for years
- **Naturally rewards real occupants** — the farmer living on their land accumulates proof just by living their life
- **Resistant to wealth concentration** — you cannot buy more hours in a day

**Multi-signal verification:** Presence requires simultaneous confirmation of GPS location, device accelerometer data (proving natural movement, not a stationary device), and periodic randomized check-ins that cannot be predicted in advance.

**Anti-gaming considerations:** Device farming, collusion rings, proxy presence, and signal simulation require further design work.

### 11.2 Neighbor Quorum

Inspired by multisig wallets in Bitcoin. The Neighbor Quorum requires M of N neighbors to cryptographically sign off on a land claim.

How it works:
- A landowner designates a set of N neighbors — people with their own wallets and DIDs on the Landos chain
- The protocol requires M of those N to sign an attestation (default: 3-of-5)
- Each neighbor signs with their own private key — a cryptographic act that puts their own stake behind the claim
- Neighbors can optionally attach a written statement creating a permanent community memory record

**Default parameters:** 3-of-5. Variants: 2-of-3 for sparse rural areas, 5-of-7 for dense urban areas. Subject to revision.

### 11.3 AR Boundary Walking

A neighbor or validator physically walks the boundary of a parcel with their phone. The Landos app overlays the registered boundary on the real world through the camera. GPS data logs the validator's position. A liveness challenge proves physical presence. The completed walk is signed with the validator's private key.

**Requirements:** At least two independent validators must walk the same boundary before a boundary confirmation is recorded.

### 11.4 Delegated Vouching

A landowner assigns trusted parties who can sign attestations on their behalf. The delegation is on-chain, revocable, and does not transfer ownership.

### 11.5 Community Memory

Attestation statements accumulate over time into a living history of each parcel — permanently recorded, cryptographically signed, Bitcoin-anchored.

---

## 12. Griefing Defense

Griefing is the act of filing bad-faith claims against real landowners — not to succeed, but to cause harm. Forcing someone into a dispute is costly and stressful regardless of outcome, especially for someone with no legal resources. A system that can be weaponized this way fails the people it exists to protect.

Landos addresses griefing through five interlocking mechanisms. None of them alone is sufficient. Together they make bad-faith attacks expensive, slow, and likely to backfire.

### 12.1 Land Witness

A Land Witness is a neutral third party — someone with no relationship to either party in a claim and no stake in the outcome — who witnesses and certifies a transaction or attestation. Structurally, a Land Witness cannot be a beneficiary of the claim they are certifying.

The Land Witness role is distinct from the neighbor quorum (which involves people who know the landowner) and from validators (who process transactions). A Land Witness provides independent, disinterested certification — the on-chain equivalent of a notary.

Land Witnesses accumulate a Personal Validation Score (see 12.3) through their witnessing activity. A Land Witness who certifies fraudulent transactions is penalized through their score and subject to protocol-level penalties.

### 12.2 Interested Party Exclusion

Certain people are structurally excluded from attesting in certain situations. The protocol enforces this automatically — it is not a manual review.

Examples:
- A neighbor with an active adjacent claim cannot participate in the quorum for the parcel they border
- A family member named in a succession record cannot serve as a recovery contact for that same account
- A Land Witness with any on-chain relationship to either party in a dispute cannot certify that dispute

Interested Party Exclusion removes the most obvious vectors for collusion before they can be exploited.

### 12.3 Personal Validation Score (PVS)

Every account on Landos accumulates a Personal Validation Score — a cumulative record of honest participation over time. PVS is built through:

- Attestations made that were later validated as legitimate
- Disputes participated in that were resolved correctly
- Recovery approvals that held up under review
- Land Witness certifications that proved accurate

PVS grows slowly. It is damaged by bad behavior — approving fraudulent claims, participating in failed bad-faith disputes, certifying false attestations. It never resets.

PVS serves as a trust signal throughout the protocol. A neighbor quorum composed of high-PVS participants carries more weight than one composed of new or low-PVS accounts. A Land Witness with high PVS provides stronger certification. A low-PVS account attempting to file a claim against a confirmed parcel triggers additional scrutiny.

PVS is distinct from the habitation score (which measures physical presence) and hub standing (which measures community participation at the hub level).

### 12.4 Hold Period

Any claim filed against an already-confirmed parcel triggers an automatic Hold Period before any action can be taken. During this period:

- The existing owner is notified immediately through all registered contact points
- The parcel status moves to Contested but the existing owner's rights are not affected
- No transfer, no recovery, and no status change can occur until the Hold Period expires
- The existing owner can present evidence, gather attestations, and prepare a response

The Hold Period gives real owners time to respond before anything irreversible happens. It also imposes a time cost on bad-faith actors — a griefing campaign that takes months to execute per parcel is far less attractive than one that moves quickly.

Exact Hold Period duration is TBD — likely calibrated to the severity of the claim and the confirmation history of the parcel.

### 12.5 Dispute Bond

To file a claim against a confirmed parcel, the claimant must stake a Dispute Bond in LOS. This bond:

- Is held in escrow for the duration of the dispute
- Is forfeited in full if the claim is found to be bad faith
- A portion of the forfeited bond is awarded to the existing owner as compensation for the disruption
- The remainder is burned or allocated to the network

The Dispute Bond does not prevent legitimate claims — someone with a real competing claim should be willing to stake something behind it. It specifically targets bad-faith actors who file claims with no intention of prevailing, purely to cause harm.

Bond amount is TBD — must be high enough to deter griefing, low enough that a legitimate claimant with a real dispute is not priced out.

---

## 13. Ownership Status System

Every parcel on the Landos chain has a status at all times. Status transitions are individual transactions written permanently to the chain.

**Unregistered** → **Claimed** → **Pending** → **Partial** → **Confirmed** → **Contested** → **Reverted**

See v0.1.3 for full status definitions and transition rules.

---

## 14. Transfers and Succession

Land Record NFTs transfer between wallets via standard NFT transfer mechanics — signed by the current owner's private key. Fractional transfers support subdivision.

Succession records allow landowners to designate heirs on-chain. Full design requires legal review — see v0.1.3 for working concepts.

For lost key recovery, see Section 16.

---

## 15. Community Hubs

Every registered parcel belongs to a Community Hub — a geographic grouping of parcels whose owners share proximity. Hubs emerge organically from registration activity, not from political boundaries. They handle local validation context, community memory, local governance, and contested claim resolution.

See v0.1.3 for full Community Hub design.

---

## 16. Identity Verification

Landos partners with third-party identity verification providers (initial partner: Persona) using W3C Verifiable Credentials. Landos never stores biometric data — it trusts the credential returned by the provider.

See v0.1.3 for full identity verification design.

---

## 17. Key Recovery

### 16.1 The Problem of Lost Keys

A private key is the only proof of ownership on the Landos chain. There is no customer support line that can reset it. There is no central authority that can override it. This is by design — but it creates a real and serious problem: people lose keys. Phones break. People die. A farmer who registered their land on Landos and then loses their private key should not lose their land.

Key recovery on Landos does not restore a lost private key — that is cryptographically impossible, and storing keys anywhere recoverable would be a security vulnerability. What recovery does is authorize a **key rotation**: the old key is invalidated, a new one takes its place, and the Land Record NFT transfers to the new wallet. The chain records it as a recovery event, permanently and transparently.

### 16.2 The Recovery Portal

Key recovery is handled through a dedicated web portal — separate from the main Landos interface — where users authenticate with their DID and PIN. The portal never holds or sees private keys. It facilitates the recovery process and, when all conditions are satisfied, authorizes a key rotation on-chain.

### 16.3 Recovery Factors

At account creation, every Landos user registers three recovery factors:

**Primary email** — required at registration. Users are warned explicitly and repeatedly: this email is a lifeline. Losing access to it makes recovery significantly harder. Treat it like a key to your home. Users must acknowledge this warning before completing registration.

**PIN** — a secondary factor known only to the user, used alongside the DID to authenticate recovery requests.

**Recovery contacts** — three designated people (neighbors, family members, or other trusted individuals) who are verified at registration time as having active DID accounts on Landos. They are notified when designated and asked to confirm. They are re-confirmed annually to ensure their accounts remain active and their willingness to serve continues.

### 16.4 Recovery Paths

Recovery is tiered by which factors remain intact:

| Factors Available | Recovery Path | Friction |
|---|---|---|
| DID + PIN + email | Automated — standard verification flow | Low |
| DID + email, lost PIN | Email-based PIN reset, then standard flow | Low |
| PIN + email, lost DID | Email-based DID recovery, then standard flow | Low |
| Email + recovery contacts, lost DID + PIN | Contact attestation + identity verification | Medium |
| Recovery contacts only, lost everything else | High-threshold contact quorum + Persona identity verification + human review | High |

No recovery path is instant. All recovery requests are subject to a **72-hour time-lock** during which the original owner — if still in control of any registered contact point — can cancel the attempt. This protects against social engineering attacks.

Every recovery attempt triggers notifications to all registered contact points. Every recovery event is permanently recorded on-chain as a distinct transaction type.

### 16.5 Recovery Contacts

Recovery contacts are distinct from the neighbor quorum used for ownership validation. They are specifically designated for account recovery and carry explicit responsibilities:

- Must hold an active DID account on Landos at time of designation
- Receive explicit notification that they have been named as a recovery contact
- Re-confirm annually that they are willing and able to serve this role
- Sign recovery attestations with their own private key — a cryptographic act that puts their own account standing behind the claim
- Contacts who approve a fraudulent recovery are subject to protocol-level penalties

In the worst-case scenario — a user has lost their key, their DID, their email, and cannot reach any recovery contact — community-level recovery through a high-threshold neighbor quorum combined with Persona identity verification is the path of last resort. This requires human review and is designed to be difficult by necessity.

### 16.6 Support and Automation

The vast majority of recovery cases — lost PIN, lost DID with email intact, lost email with contacts intact — are handled entirely through automated flows guided by an AI-assisted portal. Users are walked through the process step by step without requiring human intervention.

Human support workers engage only when automation cannot resolve the case. Support workers are hired and managed by the Landos Foundation (see Section 5) and compensated in LOS. Their incentives align with the network: a healthy, trustworthy network means their rewards are worth more. Support workers who approve fraudulent recoveries are subject to the same penalty structure as recovery contacts — they stake their standing on every decision they make.

This model keeps support costs manageable at scale while ensuring that every edge case has a human path to resolution.

---

## 18. Security and Decentralization

Landos is designed to have no off switch.

- **No central server** — nodes run across many jurisdictions globally
- **No foundation with a bank account that controls the protocol** — the Foundation handles operations; it does not control the chain
- **No CEO** — no individual to arrest or coerce
- **Open source** — the code is publicly verifiable by anyone
- **Bitcoin anchored** — records survive even if Landos is attacked
- **Geographic distribution** — shutting Landos down would require simultaneous action across dozens of countries
- **Community hub structure** — thousands of independent local hubs mean no single point of failure

---

## 19. What Others Have Tried

Landos is not the first project to attempt blockchain-based land registration. Understanding why previous attempts failed is essential to building something that works.

| Project | Approach | Outcome | Why It Failed |
|---|---|---|---|
| Honduras / Factom (2015) | Government partnership, anchor records to Bitcoin | Never launched | Political resistance — corrupt officials blocked a system designed to stop corruption |
| Bitland / Ghana (2014+) | Community-based registration | Never delivered objectives after 10+ years | Organization failure, adoption problem, no path from informal to formal |
| Republic of Georgia / Bitfury | Hash government records to permissioned chain | Launched but minimal impact | Just hashed existing government records — still government-controlled, no real decentralization |
| Sweden / ChromaWay (2016+) | Government partnership, smart contracts | Technically worked, legally stalled | Swedish law requires paper signatures — one legal technicality stopped a working system |
| Medici Land Governance | Government partnership, multiple jurisdictions | Limited scale | Dependent on government adoption speed |

**The pattern:** Every project either required government cooperation and got strangled by it, or used permissioned chains that governments still controlled — which defeats the purpose. Not one project solved the core de Soto problem: getting informal, unregistered land into a formal system without going through the corrupt institutions that caused the problem.

**What Landos does differently:**
- Does not wait for government permission — builds adoption from the ground up
- Uses a public, decentralized chain — no government controls the nodes
- Community validation instead of institutional validation
- Explicitly grounded in de Soto's dead capital framework — solving the economic problem, not just the technical one
- Designed for the countries where existing registries have already failed

---

## 20. Inspiration and Prior Art

Landos stands on the shoulders of existing work — the same way Bitcoin assembled HashCash, b-money, Merkle trees, and digital signatures into something new.

| Component | Existing Work Used |
|---|---|
| Cryptographic security | SHA-256, ECDSA, Merkle trees |
| Dead capital framework | Hernando de Soto, *The Mystery of Capital* (2000) |
| Land identification | WGS84, GeoJSON (RFC 7946), H3, Coords protocol |
| Bitcoin anchoring | OpenTimestamps (Peter Todd) |
| Self-sovereign identity | W3C DIDs |
| Identity verification | Persona (W3C Verifiable Credentials) |
| Community land documentation | Open Tenure (FAO) |
| Proof of location | FOAM protocol, IEEE Proof of Location research |
| Consensus base layer | Tendermint BFT / Cosmos SDK |
| Consensus application layer | Proof of Stake (Ethereum) |
| Multisig validation | Bitcoin multisig wallet design |
| Location-based participation | Pokémon Go (Niantic) |
| Local registry model | County assessor systems |
| RWA token model | Established web3 RWA patterns (RealT, Centrifuge, Propy) |
| Investment without direct ownership | REIT structure (traditional finance) |

---

## 21. What Landos Is Not

- **Not a government project** — it does not require institutional permission to function
- **Not an anarchist project** — it earns legitimacy through adoption, not through opposition
- **Not a company** — it is ownerless infrastructure; the Foundation is a minimal operational scaffold, not a controlling entity
- **Not connected to other crypto projects** — except Bitcoin as a trust anchor
- **Not replacing existing land systems** — it runs alongside them as a parallel, incorruptible record
- **Not a single token tied to specific parcels** — LOS is a separate economic layer from land ownership records
- **Not finished** — this is a v0.1.5 thinking document

---

## 22. Open Questions

**Resolved since v0.1.3:**
- Token model: two instruments (Land Record NFT + LOS fungible token) — decided ✓
- Philosophical foundation: Bitcoin + de Soto as the two pillars — decided ✓
- Node model: three types — full nodes (validate everything), light/SPV nodes (verify via Merkle proofs), relay nodes (serve data, no validation authority); no geographic nodes — decided ✓
- Government relationship: legitimacy earned through adoption, not permission — decided ✓
- Key recovery: tiered recovery system via dedicated portal; email + PIN + 3 recovery contacts at registration; 72-hour time-lock; AI-assisted automation with LOS-rewarded human escalation — direction set ✓
- Landos Foundation: minimal operational entity for support operations, worker compensation in LOS, and early stewardship; no protocol control — decided ✓

**Active open questions:**

1. **Full token name** — ticker is LOS; full name TBD
2. **LOS total supply and distribution** — supply cap, genesis allocation, node/validator reward schedule, Foundation allocation TBD
3. **NFT standard** — which Cosmos SDK NFT standard to use; fractional ownership (semi-fungible) design TBD
4. **Registration fee subsidy mechanism** — how landowners who cannot afford fees access assistance TBD
5. **Node reward specifics** — exact reward amounts, uptime vs. validation ratio, tapering schedule TBD
6. **Z-axis / 3D ownership** — unit volume definition, vertical extent constants TBD
7. **Genesis block** — what it contains and what it declares TBD
8. **Proof of Land scoring model** — exact weighting of validation mechanisms; threshold for Confirmed status TBD
9. **Neighbor Quorum parameters** — 3-of-5 default; needs revisiting as design matures
10. **Proof of Habitation anti-gaming** — device farming, collusion rings, proxy presence, signal simulation TBD
11. **AR Boundary Walking anti-gaming** — GPS spoofing, video replay TBD
12. **Hub activation threshold** — minimum registered parcels to activate a Community Hub TBD
13. **Hub boundary definition** — how geographic hub boundaries are drawn without political boundaries TBD
14. **Disputed territories** — how politically contested land is handled at hub governance level TBD
15. **Succession and inheritance** — ⚠ requires legal review; working concept in v0.1.3
16. **Key recovery — penalty specifics** — protocol-level penalties for contacts/workers who approve fraudulent recoveries TBD
17. **Key recovery — worst-case quorum threshold** — exact parameters for last-resort neighbor quorum recovery TBD
18. **Foundation structure** — legal jurisdiction, governance, wind-down trigger TBD
19. **Collective and community ownership** — indigenous communities, communal land; no design yet
20. **The mobile app** — validation layer depends on an app not yet designed; offline/low-connectivity required
21. **Privacy** — public records may create risk for landowners in some regions TBD
22. **Land subdivision and merging** — how parcels split or combine TBD
23. **Governance** — protocol upgrade process, supermajority + time lock + gradual creator exit TBD
24. **The whitepaper** — not yet; design must stabilize first

---

## 23. Related Documents

- `landos-design-v0.1.4.md` — previous version
- `landos-design-v0.1.3.md` — ownership status system, community hubs, succession design
- `xref-design-v0.1.0.md` — XREF spatial cross-reference system design
- Coords protocol spec: github.com/coordsapp/spec
- Coords reference implementation: github.com/coordsapp/core

---

*End of v0.1.5 — this is a thinking document, not a final design. All sections subject to change.*

---

## Changelog

| Version | Date | Changes |
|---|---|---|
| v0.1.0 | 2026-05-17 | Initial draft (as Fundos) |
| v0.1.1 | 2026-05-18 | Token model expanded to 3D (X, Y, Z); two-tier supply model introduced |
| v0.1.2 | 2026-05-18 | Name changed to Landos (LAND OS); ownership validation mechanisms expanded; identity verification added |
| v0.1.3 | 2026-05-18 | Token ticker LOS confirmed; ownership status system; transfers and succession; Community Hubs; Tendermint BFT confirmed |
| v0.1.4 | 2026-05-29 | Token model redesigned: two instruments (Land Record NFT + LOS fungible token); De Soto dead capital framework added as philosophical pillar; node economics section added (tiered nodes, LOS rewards); prior art / failed projects analysis added; government relationship clarified (legitimacy earned through adoption, not permission); open questions updated |
| v0.1.5 | 2026-05-30 | Landos Foundation added (Section 5): minimal operational entity, support operations, LOS worker compensation, no protocol control; key recovery system added (Section 16): tiered recovery paths, recovery portal, 3 recovery contacts at registration, 72-hour time-lock, AI-assisted automation, LOS-rewarded human escalation; node model finalized: relay nodes added, geographic nodes removed; sections renumbered throughout; What Landos Is Not updated to reflect Foundation and 4.3 framing |
| v0.1.5 | 2026-06-01 | Asset model clarified: Parcel Record introduced as foundational protocol primitive (Section 6.2); token model updated from two instruments to three layers (Parcel Record → Land Record NFT → LOS); parcel lifecycle defined (subdivision, consolidation, boundary adjustment, contested boundary); section 6 renumbered throughout. Griefing defense added (Section 12): Land Witness, Interested Party Exclusion, Personal Validation Score (PVS), Hold Period, Dispute Bond; all sections renumbered |
