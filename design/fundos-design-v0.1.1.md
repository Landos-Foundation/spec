# Fundos — Sovereign Land Blockchain
## Design Document v0.1.1

**Status:** Draft — thinking document, not a final spec  
**Date:** 2026-05-18  
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

### 5.2 One Coin = One Unit of Space

Each Fundos token is uniquely tied to a specific, real, physical location on Earth via metadata — identified by a Coords URI that includes X (longitude), Y (latitude), and Z (altitude).

- **1 Fundos token = 1 hectare of surface land** (X, Y)
- **8 decimal places** = fractional ownership (e.g., a 100m² apartment = 0.00000100 of a surface hectare token)
- **Token metadata** = the canonical Coords URI identifying the location in three dimensions
- **Z axis** = altitude above or below ground, enabling ownership of apartments, building floors, underground spaces, and subsurface rights

This is what separates Fundos from every other crypto token. The coin has meaning beyond its price. It is the land — in three dimensions.

### 5.3 Token Supply — Two-Tier Model

Fundos uses a two-tier supply model, both fully programmatic and written into the protocol at genesis. No human controls supply. The protocol controls supply.

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

Powerful interests will