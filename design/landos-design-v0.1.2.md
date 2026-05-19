# Landos — Sovereign Land Blockchain
## Design Document v0.1.2

**Status:** Draft — thinking document, not a final spec  
**Date:** 2026-05-18  
**Name:** Landos (LAND OS)  
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

---

## 3. The Name

**Landos** — settled name as of v0.1.2. Previously working name was Fundos.

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

---

## 5. The Token

### 5.1 One Token

Landos uses a single token. Bitcoin's model — one asset, one chain — funds the entire ecosystem through the value of that token. Two tokens introduce complexity and fragility. Landos follows the same principle.

**Token name:** TBD

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

#### Why This Works

The surface supply is fixed because the Earth's surface is fixed. The Z supply is programmatic because human development in the vertical dimension is real, ongoing, and unpredictable over centuries. Making Z issuance automatic and rule-based — rather than controlled by any person or organization — means the protocol is sovereign over its own supply. Exactly as Bitcoin intended.

### 5.4 Token Incentives for Early Network Building

Landos faces a bootstrap problem: in the early days, there are no neighbors on the chain, no accumulated habitation records, no existing community of validators. Participation requires incentive before it becomes self-sustaining.

The solution: **early validators are rewarded with tokens for completing validation work** — walking boundaries, vouching for neighbors, registering parcels, completing identity verification. This mirrors Bitcoin's approach: early miners received large rewards because the network needed them. As the network grows, the work becomes normalized, and eventually validation becomes a requirement of the system rather than an incentivized option.

The incentive schedule is programmatic — written into the protocol at genesis, not controlled by any person.

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

### 8.2 Working Name: Proof of Land

The consensus model being explored is called **Proof of Land** — a variant of Proof of Stake where the stake is anchored to real registered land parcels rather than purely liquid tokens.

Core idea: validators on the Landos network are landowners. Their stake is tied to their real land on the chain. Dishonest behavior risks that stake — which is connected to something real, finite, and meaningful.

This aligns incentives in a unique way: the people who secure the network are the people whose land lives on the network. They have the most to lose if it fails.

### 8.3 Guiding Principle

No single mechanism makes Landos secure. Like Bitcoin — where the combination of proof of work, longest chain rule, and economic incentives creates robustness — Landos uses a combination of mechanisms specifically designed around land, human presence, and community knowledge. The mechanisms below are the spokes of that system.

---

## 9. Ownership Validation Mechanisms

Establishing that a person owns a piece of land is a human and social problem, not just a technical one. People know who lives where. Communities know their own members. Landos encodes that social knowledge into the protocol cryptographically. No single mechanism is sufficient on its own. Together they are very hard to game.

### 9.1 Proof of Habitation

A landowner proves physical presence at their registered land over time using a mobile app connected to the Coords location of their parcel. Every verified period of presence accumulates into a record of habitation.

Key properties:
- **Time is the proof** — presence accumulates over days, months, years
- **Cannot be faked at scale** — a bad actor can sit on a corner of land for an hour; a real owner has been there for years
- **Naturally rewards real occupants** — the farmer living on their land accumulates proof just by living their life
- **Resistant to wealth concentration** — you cannot buy more hours in a day

Anti-gaming considerations are unresolved. GPS spoofing, phone-at-location without presence, and other attack vectors require further design work.

### 9.2 Neighbor Quorum

Inspired by multisig wallets in Bitcoin, the Neighbor Quorum requires M of N neighbors to cryptographically sign off on a land claim.

How it works:
- A landowner designates a set of N neighbors — people with their own wallets and DIDs on the Landos chain
- The protocol requires M of those N to sign an attestation (e.g., 3 of 5)
- Each neighbor signs with their own private key — a cryptographic act that puts their stake behind the claim
- Neighbors can optionally attach a written statement — how long they have known the person, what they know about the land — creating a permanent community memory record on the chain

Why this is hard to fake: neighbors physically live next to you. They know who lives where. You cannot easily buy 3 out of 5 neighbors' cryptographic signatures. A bad actor claiming someone else's land would need to corrupt multiple real people who know the truth.

This is a social consensus mechanism — not a technical one. That is its strength.

### 9.3 AR Boundary Walking

Inspired by the mechanics of Pokémon Go, which proved that millions of people will physically travel to real locations when there is a reason to show up.

In Landos, a neighbor or validator physically walks the boundary of a parcel with their phone. The experience:
- The Landos app shows the registered boundary overlaid on the real world through the camera (augmented reality)
- GPS data logs the validator's position continuously as they walk
- The camera captures terrain, landmarks, and boundary markers
- The validator confirms that what they see on the ground matches what the chain says the boundary is
- When complete, they sign the boundary confirmation with their private key

The result is a cryptographic record that says: *this person was physically at these coordinates at this time, walked this boundary, and their camera and GPS confirmed it matched the registered parcel.* This is a qualitatively different kind of attestation than clicking a button.

Anti-gaming considerations: GPS spoofing, video replay attacks, and camera manipulation require further design work.

### 9.4 Delegated Vouching

Not every landowner can be physically present to validate their own land. An elderly person may not be mobile. A diaspora landowner may own land in a country they no longer live in. An absentee owner may be temporarily away.

Delegated Vouching allows a landowner to assign one or more **trusted parties** — a relative, a longtime friend, a community elder — who can sign attestations on their behalf.

Key properties:
- The delegation is recorded on-chain and is revocable at any time by the landowner
- A trusted party signs with their own DID — they put their own reputation behind the voucher
- Delegation does not transfer ownership — it only grants the ability to vouch
- The protocol may limit the weight of delegated attestations compared to direct presence

This mechanism ensures that Landos works for people in difficult circumstances, not just for those with perfect access to their land.

### 9.5 Community Memory

When neighbors sign attestations — whether in a Neighbor Quorum or an AR Boundary Walk — they can attach statements to the record. These statements accumulate over time into a living history of a piece of land: who has lived there, for how long, what the community knows.

This community memory is:
- Permanently recorded on the chain
- Cryptographically signed by the person who wrote it
- Timestamped and Bitcoin-anchored
- Available to anyone who needs to understand the history of a parcel

Over time, a piece of land with decades of community attestations becomes extraordinarily difficult to falsely claim. The social record compounds the same way habitation time compounds.

---

## 10. Identity Verification

### 10.1 The Problem

A wallet can be stolen. A DID can be transferred. Without connecting a cryptographic identity to a real human being, someone could take another person's wallet and claim to be the landowner.

Identity verification is the layer that connects the cryptographic key to the human being behind it.

### 10.2 The Approach

Landos does not store biometric data. Storing faces, fingerprints, or identity documents creates legal liability, ethical risk, and political exposure that conflicts with Landos's design as ownerless infrastructure.

Instead, Landos partners with third-party identity verification providers. These companies (such as Jumio, Onfido, Persona, or equivalent) specialize in verifying real human identities. They:
- Verify the person's identity using facial recognition and document verification
- Store the raw biometric data themselves — Landos never receives it
- Return a signed cryptographic credential confirming that a real, verified human is connected to a specific DID

That credential is recorded in the person's DID on the Landos chain. Landos trusts the credential, not the raw data. The human-to-key connection is established without Landos touching a single face.

### 10.3 Status

This is a working concept. The specific partnership model, the credential format, the verification provider selection, and the governance of this layer require further design work. This section will be expanded in future versions.

---

## 11. Security and Decentralization

Landos is designed to have no off switch.

- **No central server** — nodes run across many jurisdictions globally
- **No foundation with a bank account** — no single legal entity to pressure, sue, or raid
- **No CEO** — no individual to arrest or coerce
- **Open source** — the code is publicly verifiable by anyone
- **Bitcoin anchored** — records survive even if Landos is attacked
- **Geographic distribution** — shutting Landos down would require simultaneous action across dozens of countries

Powerful interests will resist this system. The defense against them is not legal — it is structural. There is nothing to shut down.

---

## 12. Inspiration and Prior Art

Landos stands on the shoulders of existing work — the same way Bitcoin assembled HashCash, b-money, Merkle trees, and digital signatures into something new.

| Component | Existing Work Used |
|---|---|
| Cryptographic security | SHA-256, ECDSA, Merkle trees |
| Land identification | WGS84, GeoJSON (RFC 7946), H3, Coords protocol |
| Bitcoin anchoring | OpenTimestamps (Peter Todd) |
| Self-sovereign identity | W3C DIDs |
| Community land documentation | Open Tenure (FAO) |
| Proof of location | FOAM protocol, IEEE Proof of Location research |
| Consensus foundation | Proof of Stake (Ethereum) |
| Multisig validation | Bitcoin multisig wallet design |
| Location-based participation | Pokémon Go (Niantic) |
| Identity verification | Jumio, Onfido, Persona (category reference) |

---

## 13. What Landos Is Not

- **Not a government project** — it does not seek or require institutional recognition
- **Not a company** — it is ownerless infrastructure
- **Not connected to other crypto projects** — except Bitcoin as a trust anchor
- **Not replacing existing land systems** — it runs alongside them as a parallel, incorruptible record
- **Not finished** — this is a v0.1.2 thinking document

---

## 14. Open Questions

1. **Token name** — TBD
2. **Token supply constants** — exact protocol constants for max altitude (+1,000m) and max depth (-500m) need final validation; Z-axis unit volume definition TBD
3. **Consensus mechanism** — Proof of Land is a working concept; full design TBD
4. **Genesis block** — what goes in it and what does it declare?
5. **Anti-gaming for Proof of Habitation** — GPS spoofing, phone-at-location without presence
6. **Anti-gaming for AR Boundary Walking** — GPS spoofing, video replay, camera manipulation
7. **Neighbor Quorum parameters** — what are the right values of M and N? Does it vary by parcel size or region?
8. **Identity verification** — partner selection, credential format, governance of this layer
9. **Governance** — how are protocol changes decided once the creator steps away?
10. **Token incentive schedule** — exact parameters for early validator rewards and the tapering curve
11. **The whitepaper** — not yet written; will follow when the design is more settled

---

## 15. Related Documents

- `xref-design-v0.1.0.md` — XREF spatial cross-reference system design
- Coords protocol spec: github.com/coordsapp/spec
- Coords reference implementation: github.com/coordsapp/core

---

*End of v0.1.2 — this is a thinking document, not a final design. All sections subject to change.*

---

## Changelog

| Version | Date | Changes |
|---|---|---|
| v0.1.0 | 2026-05-17 | Initial draft |
| v0.1.1 | 2026-05-18 | Token model expanded to 3D (X, Y, Z); two-tier supply model introduced; Z-axis programmatic issuance defined |
| v0.1.2 | 2026-05-18 | Name changed from Fundos to Landos (LAND OS); ownership validation mechanisms expanded (Neighbor Quorum, AR Boundary Walking, Delegated Vouching, Community Memory); identity verification section added; token incentive bootstrap model added; prior art table updated |
