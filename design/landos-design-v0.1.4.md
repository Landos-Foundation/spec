# Landos — Sovereign Land Blockchain
## Design Document v0.1.4

**Status:** Draft — thinking document, not a final spec  
**Date:** 2026-05-29  
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

## 5. The Token Model

### 5.1 Two Instruments, Not One

Previous versions of this document described a single token (LOS) tied directly to land parcels on a one-to-one basis. Through further design work, it became clear that this conflated two fundamentally different financial instruments with different purposes, different holders, and different rules.

Landos uses **two separate instruments**:

1. **The Land Record NFT** — the on-chain ownership record for a specific parcel of land
2. **LOS** — a fungible token representing economic exposure to the global land value unlocked by Landos

These are modeled on established patterns in both traditional finance and the web3 RWA (Real World Asset) space. In traditional finance, you can own a specific property (deed) or invest in real estate value without owning property (REIT). Landos brings both instruments on-chain.

---

### 5.2 The Land Record NFT

The Land Record NFT is the on-chain deed. It is a non-fungible token uniquely tied to a specific parcel of land, identified by its Coords URI.

Key properties:
- **One NFT per parcel** — each unique piece of land has one canonical NFT
- **Keyed to the Coords URI** — the NFT metadata contains the canonical location identifier, stored permanently on-chain (never off-chain)
- **Ownership = holding the NFT** — whoever holds the NFT is the registered owner on the Landos chain
- **Transfer = standard NFT transfer** — signed by the current owner's private key, recorded on-chain
- **Fractional ownership** — handled through semi-fungible token standards (e.g., for apartments, shared family land, building floors); design TBD
- **Status** — the NFT carries the parcel's current ownership status (Unregistered → Claimed → Pending → Partial → Confirmed → Contested → Reverted)

The Land Record NFT does not require LOS to exist. It does not change in value based on LOS price. It is the land record — pure and simple.

---

### 5.3 LOS — The Economic Layer

LOS is a fungible token. It is not a deed, and holding LOS does not give you ownership of any specific piece of land.

**What LOS represents:**

LOS captures the economic value created by Landos's core function: converting dead capital into live capital. Every parcel registered on Landos moves from economically inert to economically active. That transformation has real value — globally estimated at trillions of dollars in currently unlocked potential. LOS is the instrument through which that aggregate value is accessible to anyone in the world.

This is analogous to a global land REIT — not tied to any single property, but representing a stake in the aggregate economic activity that Landos enables across all registered land worldwide.

**What gives LOS value:**

- Every land registration, transfer, validation, and transaction on Landos requires a small fee paid in LOS
- Node operators earn LOS for running the network (see Section 6)
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

### 5.4 Token Supply

**Land Record NFTs:** Supply is determined by geography. The surface of the Earth contains approximately 148.94 million km² of land. The exact NFT supply and parcel sizing methodology is TBD — to be defined in a separate parcel definition document.

**LOS:** Total supply, distribution schedule, and the split between node rewards, validator rewards, and any genesis allocation are TBD. The supply model will follow Bitcoin's principle of fixed, programmatic, non-human-controlled issuance.

---

### 5.5 Registration Fees and Access

Registering land on Landos requires a small fee paid in LOS. This fee:
- Compensates node operators and validators who do the work of securing the network
- Creates a cost barrier against spam registrations
- Is designed to be minimal — not a barrier to the people Landos exists to serve

**Fee assistance mechanism:** There must be a protocol-level mechanism by which a landowner who cannot afford the registration fee can access funds to cover it. The design of this mechanism is TBD. Possible approaches include community hub funds, validator subsidies for underserved regions, and sponsored registration programs. This is a priority design item.

---

## 6. Node Economics

### 6.1 Nodes Are the Network

The strength of Bitcoin is not just its cryptography. It is the tens of thousands of independently operated nodes distributed around the world, each one enforcing the rules and maintaining the record. No single actor can shut down what has no center.

Landos requires the same foundation. Nodes are not an implementation detail — they are the security model.

### 6.2 Tiered Node Model

Landos uses a tiered node architecture designed to maximize participation by making it accessible at multiple levels of hardware and commitment:

**Full Nodes**
- Store the complete Landos blockchain
- Validate all transactions and enforce all protocol rules
- Highest hardware requirements
- Earn the highest LOS rewards

**Light Nodes (SPV)**
- Store block headers and hashed indexes only
- Verify transactions without storing the full chain
- Can run on standard consumer hardware (laptop, Raspberry Pi)
- Earn smaller LOS rewards than full nodes
- Lower barrier to entry — critical for global distribution

**Geographic Nodes**
- A node type unique to Landos, made possible by the geographic nature of land records
- Store full data only for a specific geographic region (e.g., a country, a region, a Community Hub area)
- Serve as authoritative local nodes for their region
- Earn LOS rewards for serving their region reliably
- Enables participation by people with limited storage who still want to contribute meaningfully to their local area

### 6.3 How Nodes Earn LOS

Node operators earn LOS through two mechanisms:

**Uptime and availability** — nodes that remain online and serve the network reliably earn LOS proportional to their availability. This incentivizes a stable, always-on network backbone.

**Validation work** — nodes that participate in confirming land claims, processing registrations, and executing validation tasks earn additional LOS for that work.

The specific reward amounts, the ratio between uptime rewards and validation rewards, and the schedule for both are TBD. The design principle is that running a node should always be economically rational once LOS has meaningful value, creating a self-reinforcing network effect.

### 6.4 Making Nodes Easy to Run

Previous blockchain projects — including Bitcoin in its early years — suffered from node operation being too technically demanding for ordinary people. Landos must make node operation accessible. This means:

- Simple installation with minimal technical knowledge required
- Clear documentation and tooling
- Light and geographic node options for lower-powered hardware
- A path from zero to running a node that any technically curious person can follow

The easier it is to run a node, the more nodes exist. The more nodes exist, the more secure and decentralized the network. This is a design and UX priority, not just an engineering consideration.

---

## 7. Land Identification

### 7.1 The Canonical Identifier — Coords URI

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

### 7.2 The XREF — Cross-Reference System

Not everyone comes to Landos with a Coords URI. A farmer might have a government parcel number. A community might have an Open Tenure record. A landowner might only have GPS coordinates.

The **XREF** (cross-reference system, name TBD) maps every major spatial identification system back to a single canonical Coords URI. Any ID from any system resolves to one Landos location.

See: `xref-design-v0.1.0.md` for full XREF design.

Supported systems include H3, What3Words, WGS84, GeoJSON, Open Tenure, Plus Codes, MGRS, postal addresses, and national cadastral registries.

### 7.3 Geographic Foundation

Landos builds on the following open geographic standards:

- **WGS84** — the universal GPS coordinate standard used by every device on Earth
- **GeoJSON (RFC 7946)** — open internet standard for encoding geographic boundaries
- **H3 (Uber)** — open source hexagonal grid for dividing Earth into hierarchical cells
- **Coords protocol** — canonical URI encoding for precise location identification

---

## 8. Connected Systems

### 8.1 Bitcoin Anchor

Landos records are periodically anchored into the Bitcoin blockchain using **OpenTimestamps** — an open protocol by Bitcoin developer Peter Todd.

This means even if Landos itself were attacked or destroyed, proof that land records existed at specific moments in time lives permanently in Bitcoin. No one can erase it.

Bitcoin is the trust anchor. Landos does not depend on any other crypto project or chain.

### 8.2 Open Tenure (FAO)

Open Tenure is a mobile application developed by the UN Food and Agriculture Organization that allows communities to document land rights on the ground using basic mobile devices, GPS, photos, and community consensus.

Open Tenure solves the human, on-the-ground documentation problem. Landos solves the permanent, immutable record problem. Together:

- Open Tenure captures and validates community land claims in the real world
- Those validated claims are written to the Landos chain via the XREF
- The record becomes permanent and sovereign

Open Tenure handles the people layer. Landos handles the truth layer.

### 8.3 Decentralized Identity (DIDs)

Land ownership on Landos is tied to **W3C Decentralized Identifiers (DIDs)** — an official internet standard since 2022. A DID is a self-sovereign identity that no central authority controls.

A person owns their Landos identity the same way they own their land — through cryptography, not permission.

---

## 9. Consensus Mechanism

### 9.1 Status

The Landos consensus mechanism is under active development. No final design has been selected. What follows are working concepts.

### 9.2 Base Layer — Tendermint BFT

Landos uses **Tendermint BFT** (Byzantine Fault Tolerant) consensus as its base layer, implemented via the **Cosmos SDK**. Tendermint is proven, energy-efficient, and handles the hard distributed systems problems — node agreement, fork resolution, network partitions — without requiring proof of work.

Cosmos SDK is purpose-built for application-specific blockchains. It handles the networking and consensus layer, allowing Landos to focus on what makes it unique: the Proof of Land application layer on top.

### 9.3 Application Layer — Proof of Land

On top of Tendermint, Landos runs **Proof of Land** — a novel consensus model where validator weight is determined not by liquid token stake alone, but by a combination of:

- Registered land on the chain
- Accumulated habitation score
- Neighbor quorum attestations
- Community hub standing

Validators are landowners. Their stake is tied to something real, finite, and meaningful. Dishonest behavior risks that stake. The people who secure the network are the people whose land lives on the network — they have the most to lose if it fails.

### 9.4 Guiding Principle

No single mechanism makes Landos secure. Like Bitcoin — where the combination of proof of work, longest chain rule, and economic incentives creates robustness — Landos uses a combination of mechanisms specifically designed around land, human presence, and community knowledge.

---

## 10. Ownership Validation Mechanisms

Establishing that a person owns a piece of land is a human and social problem, not just a technical one. People know who lives where. Communities know their own members. Landos encodes that social knowledge into the protocol cryptographically.

No single mechanism is sufficient on its own. Together they are very hard to game. A bad actor trying to falsely claim land would need to fake physical presence, corrupt neighbors, forge delegated vouchers, and spoof identity verification simultaneously — across multiple independent systems.

### 10.1 Proof of Habitation

A landowner proves physical presence at their registered land over time using a mobile app connected to the Coords location of their parcel. Every verified period of presence accumulates into a habitation score.

Key properties:
- **Time is the proof** — presence accumulates over days, months, years
- **Cannot be faked at scale** — a bad actor can sit on a corner of land for an hour; a real owner has been there for years
- **Naturally rewards real occupants** — the farmer living on their land accumulates proof just by living their life
- **Resistant to wealth concentration** — you cannot buy more hours in a day

**Multi-signal verification:** Presence requires simultaneous confirmation of GPS location, device accelerometer data (proving natural movement, not a stationary device), and periodic randomized check-ins that cannot be predicted in advance.

**Anti-gaming considerations:** Device farming, collusion rings, proxy presence, and signal simulation require further design work.

### 10.2 Neighbor Quorum

Inspired by multisig wallets in Bitcoin. The Neighbor Quorum requires M of N neighbors to cryptographically sign off on a land claim.

How it works:
- A landowner designates a set of N neighbors — people with their own wallets and DIDs on the Landos chain
- The protocol requires M of those N to sign an attestation (default: 3-of-5)
- Each neighbor signs with their own private key — a cryptographic act that puts their own stake behind the claim
- Neighbors can optionally attach a written statement creating a permanent community memory record

**Default parameters:** 3-of-5. Variants: 2-of-3 for sparse rural areas, 5-of-7 for dense urban areas. Subject to revision.

### 10.3 AR Boundary Walking

A neighbor or validator physically walks the boundary of a parcel with their phone. The Landos app overlays the registered boundary on the real world through the camera. GPS data logs the validator's position. A liveness challenge proves physical presence. The completed walk is signed with the validator's private key.

**Requirements:** At least two independent validators must walk the same boundary before a boundary confirmation is recorded.

### 10.4 Delegated Vouching

A landowner assigns trusted parties who can sign attestations on their behalf. The delegation is on-chain, revocable, and does not transfer ownership.

### 10.5 Community Memory

Attestation statements accumulate over time into a living history of each parcel — permanently recorded, cryptographically signed, Bitcoin-anchored.

---

## 11. Ownership Status System

Every parcel on the Landos chain has a status at all times. Status transitions are individual transactions written permanently to the chain.

**Unregistered** → **Claimed** → **Pending** → **Partial** → **Confirmed** → **Contested** → **Reverted**

See v0.1.3 for full status definitions and transition rules.

---

## 12. Transfers and Succession

Land Record NFTs transfer between wallets via standard NFT transfer mechanics — signed by the current owner's private key. Fractional transfers support subdivision.

Succession records allow landowners to designate heirs on-chain. Full design requires legal review — see v0.1.3 for working concepts.

Lost key recovery remains an open and critical problem. See Open Questions.

---

## 13. Community Hubs

Every registered parcel belongs to a Community Hub — a geographic grouping of parcels whose owners share proximity. Hubs emerge organically from registration activity, not from political boundaries. They handle local validation context, community memory, local governance, and contested claim resolution.

See v0.1.3 for full Community Hub design.

---

## 14. Identity Verification

Landos partners with third-party identity verification providers (initial partner: Persona) using W3C Verifiable Credentials. Landos never stores biometric data — it trusts the credential returned by the provider.

See v0.1.3 for full identity verification design.

---

## 15. Security and Decentralization

Landos is designed to have no off switch.

- **No central server** — nodes run across many jurisdictions globally
- **No foundation with a bank account** — no single legal entity to pressure, sue, or raid
- **No CEO** — no individual to arrest or coerce
- **Open source** — the code is publicly verifiable by anyone
- **Bitcoin anchored** — records survive even if Landos is attacked
- **Geographic distribution** — shutting Landos down would require simultaneous action across dozens of countries
- **Community hub structure** — thousands of independent local hubs mean no single point of failure

---

## 16. What Others Have Tried

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

## 17. Inspiration and Prior Art

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

## 18. What Landos Is Not

- **Not a government project** — it does not require institutional permission to function
- **Not an anarchist project** — it cooperates with governments and welcomes adoption
- **Not a company** — it is ownerless infrastructure
- **Not connected to other crypto projects** — except Bitcoin as a trust anchor
- **Not replacing existing land systems** — it runs alongside them as a parallel, incorruptible record
- **Not a single token tied to specific parcels** — LOS is a separate economic layer from land ownership records
- **Not finished** — this is a v0.1.4 thinking document

---

## 19. Open Questions

**Resolved since v0.1.3:**
- Token model: two instruments (Land Record NFT + LOS fungible token) — decided ✓
- Philosophical foundation: Bitcoin + de Soto as the two pillars — decided ✓
- Node model: tiered (full, light/SPV, geographic) earning LOS for uptime + validation — direction set ✓
- Government relationship: legitimacy earned through adoption, not permission — decided ✓

**Active open questions:**

1. **Full token name** — ticker is LOS; full name TBD
2. **LOS total supply and distribution** — supply cap, genesis allocation, node/validator reward schedule TBD
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
16. **Lost key recovery** — unresolved; one of the most important open problems
17. **Collective and community ownership** — indigenous communities, communal land; no design yet
18. **The mobile app** — validation layer depends on an app not yet designed; offline/low-connectivity required
19. **Privacy** — public records may create risk for landowners in some regions TBD
20. **Land subdivision and merging** — how parcels split or combine TBD
21. **Governance** — protocol upgrade process, supermajority + time lock + gradual creator exit TBD
22. **The whitepaper** — not yet; design must stabilize first

---

## 20. Related Documents

- `landos-design-v0.1.3.md` — previous version (ownership status system, community hubs, succession design)
- `xref-design-v0.1.0.md` — XREF spatial cross-reference system design
- Coords protocol spec: github.com/coordsapp/spec
- Coords reference implementation: github.com/coordsapp/core

---

*End of v0.1.4 — this is a thinking document, not a final design. All sections subject to change.*

---

## Changelog

| Version | Date | Changes |
|---|---|---|
| v0.1.0 | 2026-05-17 | Initial draft (as Fundos) |
| v0.1.1 | 2026-05-18 | Token model expanded to 3D (X, Y, Z); two-tier supply model introduced |
| v0.1.2 | 2026-05-18 | Name changed to Landos (LAND OS); ownership validation mechanisms expanded; identity verification added |
| v0.1.3 | 2026-05-18 | Token ticker LOS confirmed; ownership status system; transfers and succession; Community Hubs; Tendermint BFT confirmed |
| v0.1.4 | 2026-05-29 | Token model redesigned: two instruments (Land Record NFT + LOS fungible token); De Soto dead capital framework added as philosophical pillar; node economics section added (tiered nodes, LOS rewards); prior art / failed projects analysis added; government relationship clarified (cooperative, not adversarial); open questions updated |
