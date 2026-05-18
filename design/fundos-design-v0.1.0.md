# Fundos — Sovereign Land Blockchain
## Design Document v0.1.0

**Status:** Draft — thinking document, not a final spec  
**Date:** 2026-05-17  
**Name:** Fundos (working name — temporary until permanent name is decided)  
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

Fundos applies the same principle to land.

**Fundos makes it possible for people to be their own title registry.**

A person's land ownership is recorded on a sovereign, decentralized blockchain that no government, corporation, or powerful individual controls. The record is permanent, immutable, and cryptographically verifiable. It cannot be altered by a bribe. It cannot be erased by a corrupt official. It exists independent of whoever holds power today.

Just as Bitcoin did not ask central banks for permission, Fundos does not ask governments for permission. It simply exists. And over time, as more people trust it more than the alternative, it gains legitimacy — the same way Bitcoin did.

---

## 3. The Name

**Fundos** — working name, subject to change.

Origins:
- Latin: *fundus* = land, estate, foundation
- English root: "fundamental", "foundation"
- Portuguese/Spanish: *fundos* = depths, funds
- Informal: Fun-DOS — a nod to DOS, the foundational operating system that everything was built on top of. Fundos aspires to be the foundational layer for land ownership that everything else builds on.

The name is temporary. The concept is not.

---

## 4. Core Philosophy

### 4.1 Fundos Belongs to No One

The creator of Fundos is a temporary steward. Like Satoshi Nakamoto, the goal is to build something that eventually runs without its creator. The moment a central person or organization controls Fundos, it becomes a target — for legal pressure, for corruption, for shutdown.

Fundos is designed from the start to be ownerless infrastructure. A public good. A layer of the internet, not a company.

### 4.2 All Land Already Exists

Unlike most blockchain systems where assets are created over time, **all land on Earth already exists** and is pre-represented on the Fundos blockchain at genesis.

This mirrors Bitcoin's supply model: all 21 million BTC exist in the protocol from the start — miners don't create them, they unlock them. Similarly, Fundos doesn't require land to be "added" to the chain. Every parcel on Earth is already there. The work is in assigning ownership to the real owners.

This matters philosophically: no one is granting you anything. You are coming to claim what is already yours on the chain.

### 4.3 Not a Replacement — A Parallel Truth

Fundos does not need governments to recognize it to function. It runs alongside existing systems, offering an independent record that cannot be corrupted. Over time, as trust grows, the Fundos record may become more trusted than government registries in some contexts — especially where those registries are unreliable or corrupt.

---

## 5. The Token

### 5.1 One Token

Fundos uses a single token. Bitcoin's model — one asset, one chain — funds the entire ecosystem through the value of that token. Two tokens introduce complexity and fragility. Fundos follows the same principle.

**Token name:** TBD

### 5.2 One Coin = One Land Parcel

Each Fundos token is uniquely tied to one piece of land on Earth via metadata. The token is not abstract — it represents a specific, real, physical place.

- **1 Fundos token = 1 land parcel**
- **8 decimal places** = fractional ownership (multiple people can own portions of one parcel)
- **Token metadata** = the canonical Coords URI identifying the parcel's location

This is what separates Fundos from every other crypto token. The coin has meaning beyond its price. It is the land.

### 5.3 Token Supply

The total supply of Fundos tokens corresponds to the total number of land parcels on Earth represented on the chain at genesis. This is a finite, real-world constrained supply — there is only so much land on Earth.

Exact supply mechanics: TBD — dependent on how parcels are defined and sized at genesis.

---

## 6. Land Identification

### 6.1 The Canonical Identifier — Coords URI

Every piece of land on the Fundos chain is identified by a **Coords URI** — an open, CC0, tamper-evident coordinate identifier defined by the Coords protocol (github.com/coordsapp).

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

Not everyone comes to Fundos with a Coords URI. A farmer might have a government parcel number. A community might have an Open Tenure record. A landowner might only have GPS coordinates.

The **XREF** (cross-reference system, name TBD) maps every major spatial identification system back to a single canonical Coords URI. Any ID from any system resolves to one Fundos location.

See: `xref-design-v0.1.0.md` for full XREF design.

Supported systems include H3, What3Words, WGS84, GeoJSON, Open Tenure, Plus Codes, MGRS, postal addresses, and national cadastral registries.

### 6.3 Geographic Foundation

Fundos builds on the following open geographic standards:

- **WGS84** — the universal GPS coordinate standard used by every device on Earth
- **GeoJSON (RFC 7946)** — open internet standard for encoding geographic boundaries
- **H3 (Uber)** — open source hexagonal grid for dividing Earth into hierarchical cells
- **Coords protocol** — canonical URI encoding for precise location identification

---

## 7. Connected Systems

### 7.1 Bitcoin Anchor

Fundos records are periodically anchored into the Bitcoin blockchain using **OpenTimestamps** — an open protocol by Bitcoin developer Peter Todd.

This means even if Fundos itself were attacked or destroyed, proof that land records existed at specific moments in time lives permanently in Bitcoin. No one can erase it.

Bitcoin is the trust anchor. Fundos does not depend on any other crypto project or chain.

### 7.2 Open Tenure (FAO)

Open Tenure is a mobile application developed by the UN Food and Agriculture Organization that allows communities to document land rights on the ground using basic mobile devices, GPS, photos, and community consensus.

Open Tenure solves the human, on-the-ground documentation problem. Fundos solves the permanent, immutable record problem. Together:

- Open Tenure captures and validates community land claims in the real world
- Those validated claims are written to the Fundos chain via the XREF
- The record becomes permanent and sovereign

Open Tenure handles the people layer. Fundos handles the truth layer.

### 7.3 Decentralized Identity (DIDs)

Land ownership on Fundos is tied to **W3C Decentralized Identifiers (DIDs)** — an official internet standard since 2022. A DID is a self-sovereign identity that no central authority controls.

A person owns their Fundos identity the same way they own their land — through cryptography, not permission.

---

## 8. Consensus Mechanism

### 8.1 Status

The Fundos consensus mechanism is under active development. No final design has been selected. What follows are working concepts.

### 8.2 Working Name: Proof of Land

The consensus model being explored is called **Proof of Land** — a variant of Proof of Stake where the stake is anchored to real registered land parcels rather than purely liquid tokens.

Core idea: validators on the Fundos network are landowners. Their stake is tied to their real land on the chain. Dishonest behavior risks that stake — which is connected to something real, finite, and meaningful.

This aligns incentives in a unique way: the people who secure the network are the people whose land lives on the network. They have the most to lose if it fails.

### 8.3 Spoke: Proof of Habitation

One component of Proof of Land currently being explored:

A landowner can prove physical presence at their registered land over time using a mobile app connected to the Coords location of their parcel. Every verified hour of presence accumulates into a record of habitation.

Key properties:
- **Time is the proof** — presence accumulates over days, months, years
- **Cannot be faked at scale** — a bad actor can sit on a corner of land for an hour; a real owner has been there for years
- **Naturally rewards real occupants** — the farmer living on their land accumulates proof just by living their life
- **Resistant to wealth concentration** — you cannot buy more hours in a day

Anti-gaming considerations are unresolved. This is a working concept, not a final design.

### 8.4 Other Possible Spokes

The following may be additional components of the consensus model — not yet defined:

- **Community corroboration** — neighboring landowners validate each other's claims (similar to Open Tenure's model)
- **Bitcoin-anchored timestamps** — proof of existence at a specific moment in time
- **Stake slashing** — dishonest validators lose their land stake
- **Delegated presence** — landowners who cannot validate themselves can delegate to trusted parties

### 8.5 Guiding Principle

No single mechanism makes Fundos secure. Like Bitcoin — where the combination of proof of work, longest chain rule, and economic incentives creates robustness — Fundos will likely use a combination of mechanisms specifically designed around land and human presence rather than computation or capital alone.

---

## 9. Security and Decentralization

Fundos is designed to have no off switch.

- **No central server** — nodes run across many jurisdictions globally
- **No foundation with a bank account** — no single legal entity to pressure, sue, or raid
- **No CEO** — no individual to arrest or coerce
- **Open source** — the code is publicly verifiable by anyone
- **Bitcoin anchored** — records survive even if Fundos is attacked
- **Geographic distribution** — shutting Fundos down would require simultaneous action across dozens of countries

Powerful interests will resist this system. The defense against them is not legal — it is structural. There is nothing to shut down.

---

## 10. Inspiration and Prior Art

Fundos stands on the shoulders of existing work — the same way Bitcoin assembled HashCash, b-money, Merkle trees, and digital signatures into something new.

| Component | Existing Work Used |
|---|---|
| Cryptographic security | SHA-256, ECDSA, Merkle trees |
| Land identification | WGS84, GeoJSON (RFC 7946), H3, Coords protocol |
| Bitcoin anchoring | OpenTimestamps (Peter Todd) |
| Self-sovereign identity | W3C DIDs |
| Community land documentation | Open Tenure (FAO) |
| Proof of location | FOAM protocol, IEEE Proof of Location research |
| Consensus foundation | Proof of Stake (Ethereum) |

---

## 11. What Fundos Is Not

- **Not a government project** — it does not seek or require institutional recognition
- **Not a company** — it is ownerless infrastructure
- **Not connected to other crypto projects** — except Bitcoin as a trust anchor
- **Not replacing existing land systems** — it runs alongside them as a parallel, incorruptible record
- **Not finished** — this is a v0.1.0 thinking document

---

## 12. Open Questions

1. **Final name** — Fundos is a working name. Token name TBD.
2. **Token supply mechanics** — how are parcels sized and counted at genesis?
3. **Consensus mechanism** — Proof of Land with Proof of Habitation is a working concept; full design TBD
4. **Genesis block** — what goes in it and what does it declare?
5. **Anti-gaming for Proof of Habitation** — GPS spoofing, phone-at-location without presence, etc.
6. **Governance** — how are protocol changes decided once the creator steps away?
7. **The whitepaper** — not yet written; will follow when the design is more settled

---

## 13. Related Documents

- `xref-design-v0.1.0.md` — XREF spatial cross-reference system design
- Coords protocol spec: github.com/coordsapp/spec
- Coords reference implementation: github.com/coordsapp/core

---

*End of v0.1.0 — this is a thinking document, not a final design. All sections subject to change.*
