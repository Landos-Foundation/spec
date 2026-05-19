# Landos — Sovereign Land Blockchain
## Design Document v0.1.3

**Status:** Draft — thinking document, not a final spec  
**Date:** 2026-05-18  
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

---

## 2. The Vision

Bitcoin proved that a monetary system could exist outside of government and institutional control. People could "be their own bank" — hold value in a wallet secured by cryptography, with no third party required.

Landos applies the same principle to land.

**Landos makes it possible for people to be their own title registry.**

A person's land ownership is recorded on a sovereign, decentralized blockchain that no government, corporation, or powerful individual controls. The record is permanent, immutable, and cryptographically verifiable. It cannot be altered by a bribe. It cannot be erased by a corrupt official. It exists independent of whoever holds power today.

Just as Bitcoin did not ask central banks for permission, Landos does not ask governments for permission. It simply exists. And over time, as more people trust it more than the alternative, it gains legitimacy — the same way Bitcoin did.

The county assessor's office has worked for a long time in many parts of the world. It works because it is local — people who know the geography, know the community, know who lives where. The problem is not the concept. The problem is that a human in an office can be bribed, corrupted, or politically pressured. Landos takes that same local structure and makes it incorruptible.

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

Landos does not need governments to recognize it to function. It runs alongside existing systems, offering an independent record that cannot be corrupted. Over time, as trust grows, the Landos record may become more trusted than government registries in some contexts — especially where those registries are unreliable or corrupt.

### 4.4 Land Belongs to Communities

Land is not purely an individual thing. A person owns land within a community. Their neighbors know them. The town knows who lives where. The community has memory that no individual has. Landos encodes that social reality into the protocol — not as a workaround, but as a foundational design principle.

Communities in Landos are not defined by governments or institutions. They emerge organically from geography — from people who share proximity and have real relationships with each other.

---

## 5. The Token

### 5.1 One Token

Landos uses a single token. Bitcoin's model — one asset, one chain — funds the entire ecosystem through the value of that token. Two tokens introduce complexity and fragility. Landos follows the same principle.

**Token ticker: LOS**  
**Full token name:** TBD

### 5.2 One Coin = One Unit of Space

Each Landos token is uniquely tied to a specific, real, physical location on Earth via metadata — identified by a Coords URI that includes X (longitude), Y (latitude), and Z (altitude).

- **1 Landos token = 1 hectare of surface land** (X, Y)
- **8 decimal places** = fractional ownership (e.g., a 100m² apartment = 0.00000100 of a surface hectare token)
- **Token metadata** = the canonical Coords URI identifying the location in three dimensions
- **Z axis** = altitude above or below ground, enabling ownership of apartments, building floors, underground spaces, and subsurface rights

This is what separates Landos from every other crypto token. The coin has meaning beyond its price. It is the land — in three dimensions.

### 5.3 Token Supply — Two-Tier Model

Landos uses a two-tier supply model, both fully programmatic and written into the protocol at genesis. No human controls supply. The protocol controls supply.

#### Tier 1 — Surface Supply (Fixed)

The surface of the Earth is finite and does not change. The surface supply is therefore fixed at genesis:

- **~1.49 billion tokens** — one per hectare of Earth's total land area (148.94 million km²)
- This number is derived from geography, not chosen arbitrarily
- It never changes — you cannot create more land

#### Tier 2 — Z-Axis Supply (Programmatic)

The Z axis — altitude above and below ground — expands as the world develops. Buildings get taller. Underground infrastructure goes deeper. A fixed Z supply would either be too restrictive or full of phantom tokens representing space that will never exist.

Instead, Z-axis tokens are issued automatically by the protocol when real 3D space is registered on the chain. The rules are:

- **Issuance trigger** — a valid 3D space registration transaction containing a Coords URI with X, Y, and Z boundaries
- **Issuance amount** — calculated automatically by the protocol based on the volume of registered space
- **No human decides** — the protocol issues tokens the same way Bitcoin issues block rewards: automatically, trustlessly, according to fixed rules
- **Maximum altitude** — +1,000 meters above ground surface (programmed in as a protocol constant, covering current and foreseeable future construction)
- **Maximum depth** — -500 meters below ground surface (covering mines, tunnels, and underground infrastructure)
- **Total theoretical maximum** — calculable by anyone at any time from the protocol constants; never changes without a community-approved protocol upgrade
- **Z-axis unit volume definition** — requires further research; TBD

#### Why This Works

The surface supply is fixed because the Earth's surface is fixed. The Z supply is programmatic because human development in the vertical dimension is real, ongoing, and unpredictable over centuries. Making Z issuance automatic and rule-based — rather than controlled by any person or organization — means the protocol is sovereign over its own supply. Exactly as Bitcoin intended.

### 5.4 Token Incentives for Early Network Building

Landos faces a bootstrap problem: in the early days, there are no neighbors on the chain, no accumulated habitation records, no existing community of validators. Participation requires incentive before it becomes self-sustaining.

The solution: **early validators are rewarded with LOS tokens for completing validation work** — walking boundaries, vouching for neighbors, registering parcels, completing identity verification. This mirrors Bitcoin's approach: early miners received large rewards because the network needed them. As the network grows, the work becomes normalized, and eventually validation becomes a requirement of the system rather than an incentivized option.

The incentive schedule is milestone-based — rewards taper as the network reaches defined milestones in registered parcels and active validators, not on a fixed time schedule. Written into the protocol at genesis. Not controlled by any person.

---

## 6. Land Identification

### 6.1 The Canonical Identifier — Coords URI

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

### 6.2 The XREF — Cross-Reference System

Not everyone comes to Landos with a Coords URI. A farmer might have a government parcel number. A community might have an Open Tenure record. A landowner might only have GPS coordinates.

The **XREF** (cross-reference system, name TBD) maps every major spatial identification system back to a single canonical Coords URI. Any ID from any system resolves to one Landos location.

See: `xref-design-v0.1.0.md` for full XREF design.

Supported systems include H3, What3Words, WGS84, GeoJSON, Open Tenure, Plus Codes, MGRS, postal addresses, and national cadastral registries.

### 6.3 Geographic Foundation

Landos builds on the following open geographic standards:

- **WGS84** — the universal GPS coordinate standard used by every device on Earth
- **GeoJSON (RFC 7946)** — open internet standard for encoding geographic boundaries
- **H3 (Uber)** — open source hexagonal grid for dividing Earth into hierarchical cells
- **Coords protocol** — canonical URI encoding for precise location identification

---

## 7. Connected Systems

### 7.1 Bitcoin Anchor

Landos records are periodically anchored into the Bitcoin blockchain using **OpenTimestamps** — an open protocol by Bitcoin developer Peter Todd.

This means even if Landos itself were attacked or destroyed, proof that land records existed at specific moments in time lives permanently in Bitcoin. No one can erase it.

Bitcoin is the trust anchor. Landos does not depend on any other crypto project or chain.

### 7.2 Open Tenure (FAO)

Open Tenure is a mobile application developed by the UN Food and Agriculture Organization that allows communities to document land rights on the ground using basic mobile devices, GPS, photos, and community consensus.

Open Tenure solves the human, on-the-ground documentation problem. Landos solves the permanent, immutable record problem. Together:

- Open Tenure captures and validates community land claims in the real world
- Those validated claims are written to the Landos chain via the XREF
- The record becomes permanent and sovereign

Open Tenure handles the people layer. Landos handles the truth layer.

### 7.3 Decentralized Identity (DIDs)

Land ownership on Landos is tied to **W3C Decentralized Identifiers (DIDs)** — an official internet standard since 2022. A DID is a self-sovereign identity that no central authority controls.

A person owns their Landos identity the same way they own their land — through cryptography, not permission.

---

## 8. Consensus Mechanism

### 8.1 Status

The Landos consensus mechanism is under active development. No final design has been selected. What follows are working concepts.

### 8.2 Base Layer — Tendermint BFT

Landos uses **Tendermint BFT** (Byzantine Fault Tolerant) consensus as its base layer, implemented via the **Cosmos SDK**. Tendermint is proven, energy-efficient, and handles the hard distributed systems problems — node agreement, fork resolution, network partitions — without requiring proof of work.

Cosmos SDK is purpose-built for application-specific blockchains. It handles the networking and consensus layer, allowing Landos to focus on what makes it unique: the Proof of Land application layer on top.

### 8.3 Application Layer — Proof of Land

On top of Tendermint, Landos runs **Proof of Land** — a novel consensus model where validator weight is determined not by liquid token stake alone, but by a combination of:

- Registered land on the chain
- Accumulated habitation score
- Neighbor quorum attestations
- Community hub standing

Validators are landowners. Their stake is tied to something real, finite, and meaningful. Dishonest behavior risks that stake. The people who secure the network are the people whose land lives on the network — they have the most to lose if it fails.

### 8.4 Guiding Principle

No single mechanism makes Landos secure. Like Bitcoin — where the combination of proof of work, longest chain rule, and economic incentives creates robustness — Landos uses a combination of mechanisms specifically designed around land, human presence, and community knowledge.

---

## 9. Ownership Validation Mechanisms

Establishing that a person owns a piece of land is a human and social problem, not just a technical one. People know who lives where. Communities know their own members. Landos encodes that social knowledge into the protocol cryptographically.

No single mechanism is sufficient on its own. Together they are very hard to game. A bad actor trying to falsely claim land would need to fake physical presence, corrupt neighbors, forge delegated vouchers, and spoof identity verification simultaneously — across multiple independent systems.

### 9.1 Proof of Habitation

A landowner proves physical presence at their registered land over time using a mobile app connected to the Coords location of their parcel. Every verified period of presence accumulates into a habitation score.

Key properties:
- **Time is the proof** — presence accumulates over days, months, years
- **Cannot be faked at scale** — a bad actor can sit on a corner of land for an hour; a real owner has been there for years
- **Naturally rewards real occupants** — the farmer living on their land accumulates proof just by living their life
- **Resistant to wealth concentration** — you cannot buy more hours in a day

**Multi-signal verification:** Presence requires simultaneous confirmation of GPS location, device accelerometer data (proving natural movement, not a stationary device), and periodic randomized check-ins that cannot be predicted in advance. No single signal is sufficient.

**Anti-gaming considerations:** Device farming (multiple phones left on land), collusion rings, proxy presence (paying someone to hold a phone), and signal simulation all require further design work. Community corroboration from neighbors on adjacent parcels provides a cross-validation layer.

### 9.2 Neighbor Quorum

Inspired by multisig wallets in Bitcoin. The Neighbor Quorum requires M of N neighbors to cryptographically sign off on a land claim.

How it works:
- A landowner designates a set of N neighbors — people with their own wallets and DIDs on the Landos chain
- The protocol requires M of those N to sign an attestation (default: 3-of-5)
- Each neighbor signs with their own private key — a cryptographic act that puts their own stake behind the claim
- Neighbors can optionally attach a written statement — how long they have known the person, what they know about the land — creating a permanent community memory record

**Default parameters:** 3-of-5. Variants: 2-of-3 for sparse rural areas, 5-of-7 for dense urban areas. Subject to revision.

**Why this is hard to fake:** Neighbors physically live next to you. They know who lives where. You cannot easily buy 3 out of 5 neighbors' cryptographic signatures. A bad actor would need to corrupt multiple real people who know the truth — and those people have their own stake at risk if they vouch fraudulently.

### 9.3 AR Boundary Walking

A neighbor or validator physically walks the boundary of a parcel with their phone. Inspired by the mechanics of Pokémon Go, which proved that millions of people will travel to real locations when there is a meaningful reason to show up.

The experience:
- The Landos app overlays the registered boundary on the real world through the camera (augmented reality)
- GPS data logs the validator's position continuously as they walk
- The camera captures terrain, landmarks, and boundary markers
- The validator confirms that what they see on the ground matches what the chain says the boundary is
- A liveness challenge (a real-time visual or audio cue) is issued during the walk, requiring a response — proving the validator is physically present, not replaying a recording
- The completed walk is signed with the validator's private key

**Requirements:** At least two independent validators must walk the same boundary before a boundary confirmation is recorded. GPS path must match the registered boundary shape — a straight-line walk of a complex polygon fails automatically.

### 9.4 Delegated Vouching

Not every landowner can be physically present. An elderly person may not be mobile. A diaspora landowner may own land in a country they no longer live in.

Delegated Vouching allows a landowner to assign trusted parties — a relative, a friend, a community elder — who can sign attestations on their behalf.

Key properties:
- The delegation is recorded on-chain and is revocable at any time by the landowner
- A trusted party signs with their own DID — they put their own reputation behind the voucher
- Delegation does not transfer ownership — it only grants the ability to vouch
- The protocol may weight delegated attestations lower than direct presence

### 9.5 Community Memory

When neighbors sign attestations, they can attach written statements to the record. These accumulate over time into a living history of a piece of land: who has lived there, for how long, what the community knows.

Community memory is:
- Permanently recorded on the chain
- Cryptographically signed by the person who wrote it
- Timestamped and Bitcoin-anchored
- Publicly readable by anyone

Over time, a parcel with decades of community attestations becomes extraordinarily difficult to falsely claim. The social record compounds the same way habitation time compounds.

---

## 10. Ownership Status System

Land ownership in Landos is not a boolean. It is a spectrum of evidence. A farmer who has lived on his land for 40 years, has neighbors who know him, but has never held a government document is not an owner under a true/false system — but he has overwhelming evidence of ownership. The status system captures that reality.

Every parcel on the Landos chain has a status at all times. Status transitions are individual transactions written permanently to the chain. The full history of a parcel's status is always visible.

### 10.1 Statuses

**Unregistered**
Land exists on the chain — all land does at genesis — but no claim has been made. This is the starting state of every parcel.

**Claimed**
A person has asserted ownership. Their identity is verified via DID and identity verification. The claim is on-chain with a timestamp. No additional validation has been completed yet.

**Pending**
Active validation is in progress. Some mechanisms are complete, others are not yet. A real person is actively working toward higher confirmation. The chain records which mechanisms are complete and which remain.

**Partial**
Meaningful validation exists but the parcel has not reached full confirmation. For example: habitation is confirmed and 2 of 5 neighbors have signed, but AR boundary walk has not been completed. Partial status represents a credible claim. It is still Bitcoin-anchored. It still has legal weight in communities that recognize Landos records.

**Confirmed**
All required validation mechanisms are complete. The strongest status. The exact requirements for Confirmed — the number and combination of mechanisms needed — is TBD pending full design of the validation scoring system.

**Contested**
Two or more parties have competing claims on the same parcel. Flagged automatically by the protocol when overlapping claims are detected. Routed to the relevant Community Hub for resolution. Neither claim advances until the contest is resolved.

**Reverted**
A parcel that was previously Claimed or higher has returned to Unregistered status — most commonly through the succession process when no heir comes forward within the defined window. Community memory and historical records remain on the chain permanently. Only the ownership token is released.

### 10.2 Validation Scoring

The path from Claimed to Confirmed runs through a set of validation mechanisms. Not all mechanisms need to be complete — a defined score threshold determines when Confirmed status is reached. The exact scoring model and threshold are TBD.

This means a landowner can see exactly where they stand and what remains. The system is transparent about what it knows and what it does not yet know.

### 10.3 Why This Matters

A conflict zone landowner who can only reach Partial status still has a permanent, timestamped, Bitcoin-anchored record of their claim. If they are ever able to complete validation, the chain updates. If they cannot, the Partial record still exists as evidence — stronger than nothing, useful in many contexts.

This mirrors how land evidence works in the real world. A deed is stronger than a tax receipt. A tax receipt is stronger than a neighbor's testimony. A neighbor's testimony is stronger than nothing. Landos encodes that spectrum.

---

## 11. Transfers and Succession

### 11.1 Standard Transfers — Send and Receive

Land tokens transfer between wallets the same way Bitcoin transfers between wallets. A landowner signs a transaction with their private key, specifying the destination wallet and the amount (which may be a fraction of a token for partial land transfers). The chain records it. The new wallet is the owner.

Fractional transfers support land subdivision — selling part of a parcel, dividing land between children, transferring a specific floor of a building.

### 11.2 Succession Records

**⚠ This section requires legal review before finalization. The design below is a working concept only.**

When a landowner dies, their private key dies with them. Without a plan, their land is locked on the chain permanently — which is unacceptable. Land is not like money. A family farm cannot simply be lost because a password was forgotten.

The Succession Record is an on-chain document, signed by the landowner with their own private key, that defines what happens to their land if they can no longer act on their own behalf. It is like a will, but it lives on the chain and cannot be altered without the owner's key.

A Succession Record can designate:
- **Named successors** — one or more wallet addresses that inherit the land
- **Fractional allocation** — how land is divided among multiple successors
- **Trusted executor** — a person authorized to trigger the succession (but not to alter it)

**Trigger mechanisms under consideration:**

*Dead man's switch with community confirmation:* The owner signs a periodic "I am still alive" transaction. If they miss the window, the chain does not automatically transfer — instead it opens a community confirmation period during which the named successor and a neighbor quorum must confirm the transfer before it executes.

*Trusted executor trigger:* A designated trusted person signs a transaction initiating succession. Requires neighbor quorum confirmation before execution.

*Legal document bridge:* A verified death certificate or probate document, processed through the identity verification partner, triggers succession. Reintroduces some institutional trust but only at the point of death.

These mechanisms may be combined. Full design is pending legal review.

**Default when no Succession Record exists:**

If a landowner dies with no Succession Record and no family member or heir comes forward within a defined window, the parcel reverts to Unregistered status. Community memory and all historical records remain permanently on the chain. The ownership token is released and the land becomes claimable again — the same way abandoned land eventually becomes available again in many physical jurisdictions.

This section will be significantly expanded after legal consultation.

### 11.3 Lost Key Recovery

If a living person loses their private key, they lose access to their land token. This is a serious problem that has no perfect solution — any recovery mechanism that works without the original key introduces a potential attack vector or central authority.

This problem is unresolved. It is one of the most important open questions in the design. It will require its own dedicated design process.

---

## 12. Community Hubs

### 12.1 The Concept

Every registered parcel on Landos belongs to a Community Hub — a geographic grouping of parcels whose owners share proximity and have real relationships with each other.

Community Hubs are not imported from political boundaries. Counties work in the US. Districts, prefectures, parishes, barangays, upazilas — every country has its own structure, and many parts of the world have no formal local government structure at all. Landos cannot depend on political geography that varies, changes, and in some places does not exist.

Instead, Community Hubs **emerge organically** from registration activity. When enough parcels in proximity are registered on the chain, a hub activates. The geography defines the hub — not a government, not a platform administrator.

### 12.2 How Hubs Are Determined

A parcel's hub membership is determined by its Coords URI — its geographic coordinates. This is automatic and cannot be manipulated. You do not choose your community hub any more than you choose your neighborhood.

The geographic hierarchy:

**Planet → Continent → Country → Region → District → City/Town → Neighborhood → Parcel**

Every parcel sits somewhere in this tree. The active hub for a parcel is the lowest level at which enough registered parcels exist to form a functioning community. In a dense city, that might be at the neighborhood level. In a rural area, it might be at the district level.

### 12.3 What a Hub Does

- **Validation context** — Neighbor Quorum validators are drawn from the same hub. Your neighbors on the chain are your neighbors in geography.
- **Community memory** — Attestations, history, and stories about land accumulate at the hub level as well as the parcel level.
- **Local governance** — Protocol decisions that affect a region are surfaced to that region's hub members first.
- **Contested claim resolution** — When two parties claim the same parcel, the contest is routed to the hub for community review before any higher-level process.

### 12.4 Multiple Hub Membership

A person with land in multiple locations belongs to multiple hubs — one per property. Their DID is one. Their hub memberships are many. This mirrors the real world: a person who owns land in two countries has obligations and relationships in both places.

### 12.5 Hub Activation Threshold

A hub activates when a minimum number of parcels in a geographic area are registered and have reached at least Claimed status. The exact threshold is TBD. Below the threshold, parcels in that area are associated with the nearest active hub at a higher geographic level.

### 12.6 Disputed Territories

Some places on Earth are claimed by two or more governments simultaneously. Landos does not take political positions. The Coords URI — derived purely from geography — is neutral. A parcel in a disputed territory gets a Coords URI based on its physical location, not on which government claims it. The hub structure reflects geography, not political allegiance.

How contested political territories are handled at the hub governance level is an open question requiring careful design.

---

## 13. Identity Verification

### 13.1 The Problem

A wallet can be stolen. A DID can be transferred. Without connecting a cryptographic identity to a real human being, someone could take another person's wallet and claim to be the landowner.

Identity verification is the layer that connects the cryptographic key to the human being behind it.

### 13.2 The Approach

Landos does not store biometric data. Storing faces, fingerprints, or identity documents creates legal liability, ethical risk, and political exposure that conflicts with Landos's design as ownerless infrastructure.

Instead, Landos partners with third-party identity verification providers. The initial partner is **Persona**. These providers:
- Verify the person's identity using facial recognition and document verification
- Store the raw biometric data themselves — Landos never receives it
- Return a signed cryptographic credential in the **W3C Verifiable Credentials** format, confirming that a real verified human is connected to a specific DID

That credential is recorded in the person's DID on the Landos chain. Landos trusts the credential, not the raw data. The human-to-key connection is established without Landos touching a single face.

Using the W3C Verifiable Credentials standard means the credential format is not locked to Persona — if the provider changes, the format stays the same.

### 13.3 Status

Working concept. Partner selection, credential governance, and the handling of jurisdictions where identity verification is unavailable or unsafe all require further design work.

---

## 14. Security and Decentralization

Landos is designed to have no off switch.

- **No central server** — nodes run across many jurisdictions globally
- **No foundation with a bank account** — no single legal entity to pressure, sue, or raid
- **No CEO** — no individual to arrest or coerce
- **Open source** — the code is publicly verifiable by anyone
- **Bitcoin anchored** — records survive even if Landos is attacked
- **Geographic distribution** — shutting Landos down would require simultaneous action across dozens of countries
- **Community hub structure** — thousands of independent local hubs mean no single point of failure at the community level

Powerful interests will resist this system. The defense against them is not legal — it is structural. There is nothing to shut down.

---

## 15. Inspiration and Prior Art

Landos stands on the shoulders of existing work — the same way Bitcoin assembled HashCash, b-money, Merkle trees, and digital signatures into something new.

| Component | Existing Work Used |
|---|---|
| Cryptographic security | SHA-256, ECDSA, Merkle trees |
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

---

## 16. What Landos Is Not

- **Not a government project** — it does not seek or require institutional recognition
- **Not a company** — it is ownerless infrastructure
- **Not connected to other crypto projects** — except Bitcoin as a trust anchor
- **Not replacing existing land systems** — it runs alongside them as a parallel, incorruptible record
- **Not finished** — this is a v0.1.3 thinking document

---

## 17. Open Questions

1. **Full token name** — ticker is LOS; full name TBD
2. **Z-axis unit volume definition** — requires further research before decision
3. **Genesis block** — what goes in it and what does it declare?
4. **Proof of Land scoring model** — exact weighting of validation mechanisms; threshold for Confirmed status
5. **Neighbor Quorum parameters** — 3-of-5 is working default; needs revisiting as design matures
6. **Proof of Habitation anti-gaming** — device farming, collusion rings, proxy presence, signal simulation; needs deeper design
7. **AR Boundary Walking anti-gaming** — GPS spoofing, video replay; liveness verification direction set but needs full design
8. **Hub activation threshold** — minimum registered parcels to activate a Community Hub
9. **Hub boundary definition** — how geographic hub boundaries are drawn without political boundaries
10. **Disputed territories** — how politically contested land is handled at the hub governance level
11. **Succession and inheritance** — ⚠ requires legal review; working concept only
12. **Lost key recovery** — unresolved; one of the most important open problems
13. **Collective and community ownership** — indigenous communities, communal land; no design yet
14. **The mobile app** — validation layer depends on an app not yet designed; offline and low-connectivity requirements
15. **Privacy** — public records may create risk for landowners in some regions; privacy options TBD
16. **Node economics** — transaction fees, validator compensation, network financial sustainability
17. **Land subdivision and merging** — how parcels split or combine in the token model
18. **Governance** — supermajority + time lock + gradual creator exit; details TBD
19. **Token incentive schedule** — milestone-based tapering; exact parameters TBD
20. **The whitepaper** — not yet; design must stabilize first

---

## 18. Related Documents

- `xref-design-v0.1.0.md` — XREF spatial cross-reference system design
- Coords protocol spec: github.com/coordsapp/spec
- Coords reference implementation: github.com/coordsapp/core

---

*End of v0.1.3 — this is a thinking document, not a final design. All sections subject to change.*

---

## Changelog

| Version | Date | Changes |
|---|---|---|
| v0.1.0 | 2026-05-17 | Initial draft |
| v0.1.1 | 2026-05-18 | Token model expanded to 3D (X, Y, Z); two-tier supply model introduced; Z-axis programmatic issuance defined |
| v0.1.2 | 2026-05-18 | Name changed to Landos (LAND OS); ownership validation mechanisms expanded; identity verification added; token incentive bootstrap model added |
| v0.1.3 | 2026-05-18 | Token ticker confirmed as LOS; ownership status system introduced (Unregistered → Claimed → Pending → Partial → Confirmed → Contested → Reverted); transfers and succession section added (legal review flagged); Community Hubs introduced; Tendermint BFT / Cosmos SDK confirmed as base layer; open questions expanded to 20 items |
