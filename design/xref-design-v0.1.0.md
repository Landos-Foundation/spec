# XREF — Spatial Cross-Reference System
## Design Document v0.1.0

**Status:** Draft  
**Date:** 2026-05-17  
**Name:** TBD (working name: XREF)  
**Home:** TBD — Coords, Fundos, or standalone  

---

## 1. The Problem

The Earth has one geography. But humans have built dozens of independent systems to describe it.

- H3 (Uber's hexagonal grid)
- What3Words
- WGS84 latitude/longitude
- GeoJSON polygons
- Google Plus Codes / Open Location Code
- MGRS (Military Grid Reference System)
- National and regional cadastral/parcel registries (country-specific)
- Open Tenure community IDs
- Postal addresses
- FIPS codes (US)
- Land title registry numbers

Every one of these systems identifies real places on Earth. None of them talk to each other. A plot of land in Kenya might have a government parcel number, an H3 cell ID, a GPS coordinate, and an Open Tenure record — all pointing to the same piece of ground, with no common key connecting them.

This fragmentation is not accidental. It is a byproduct of siloed institutions, systems built in isolation, and the absence of a universal open standard for location identity.

**XREF solves this by creating a single canonical key for every location on Earth — and mapping every other system's identifier back to that key.**

---

## 2. The Solution

XREF is a cross-reference protocol and database that:

1. Accepts a location identifier from **any supported spatial system**
2. Resolves it to a **single canonical Coords URI**
3. Returns all **other known identifiers** for that same location across all other systems

The canonical key is the **Coords URI** — an open, CC0, tamper-evident identifier defined by the Coords protocol (coordsapp/spec).

Example canonical key:
```
coords:l1:v1:37.774900,-122.419400,15.25*1c86401e
```

This URI belongs to no government, no company, no institution. It is derived purely from geography.

---

## 3. Core Concepts

### 3.1 The Canonical ID

Every unique location resolves to exactly one Coords URI. This is the XREF primary key. All foreign system IDs are secondary — they are aliases that point to the canonical ID.

### 3.2 Foreign Systems

A **foreign system** is any spatial identification system other than Coords. Each foreign system has:

- A **system code** — a short, unique identifier (e.g., `H3`, `W3W`, `CADASTRE_NG`, `OT`, `PLUS`)
- A **foreign ID** — the identifier within that system
- An optional **resolution** — for systems that operate at multiple scales (e.g., H3 resolution 0–15)
- An optional **geometry type** — point, polygon, cell

### 3.3 Mappings

A **mapping** is the link between a foreign system ID and a canonical Coords URI.

```
mapping {
  coords_id:      string    // canonical Coords URI
  system_code:    string    // e.g. "H3", "W3W", "CADASTRE_NG"
  foreign_id:     string    // the ID in that system
  geometry_type:  string    // "point" | "polygon" | "cell"
  resolution:     int?      // optional, for hierarchical systems
  contributor:    string?   // who added this mapping
  added_at:       timestamp
  source_url:     string?   // reference to source data
}
```

---

## 4. Supported Systems (Initial)

| System Code     | System Name                        | Type    | Notes                          |
|-----------------|-------------------------------------|---------|--------------------------------|
| `H3`            | Uber H3 Hexagonal Grid              | Cell    | Resolution 0–15                |
| `W3W`           | What3Words                          | Point   | 3m x 3m squares                |
| `WGS84`         | WGS84 Lat/Lon                       | Point   | Decimal degrees                |
| `GEOJSON`       | GeoJSON Polygon                     | Polygon | RFC 7946                       |
| `PLUS`          | Google Plus Codes / OLC             | Cell    | Open Location Code             |
| `MGRS`          | Military Grid Reference System      | Cell    | NATO standard                  |
| `OT`            | Open Tenure (FAO)                   | Polygon | Community land records         |
| `FIPS`          | FIPS County/Tract Code              | Polygon | US only                        |
| `CADASTRE_*`    | National Cadastral Registries       | Polygon | Country-specific suffix        |
| `ADDR`          | Postal Address                      | Point   | Geocoded to Coords             |

`CADASTRE_*` uses ISO 3166-1 alpha-2 country codes as suffix — e.g., `CADASTRE_NG` for Nigeria, `CADASTRE_BR` for Brazil.

---

## 5. Query Interface

### 5.1 Forward Lookup — Foreign ID → Coords URI

Given a foreign system code and foreign ID, return the canonical Coords URI.

```
GET /resolve?system=H3&id=8928308280fffff

→ {
    "coords_id": "coords:l1:v1:37.774900,-122.419400,0.00*xxxxxxxx",
    "system": "H3",
    "foreign_id": "8928308280fffff",
    "resolution": 9
  }
```

### 5.2 Reverse Lookup — Coords URI → All Foreign IDs

Given a Coords URI, return all known foreign system mappings for that location.

```
GET /lookup?coords_id=coords:l1:v1:37.774900,-122.419400,15.25*1c86401e

→ {
    "coords_id": "coords:l1:v1:37.774900,-122.419400,15.25*1c86401e",
    "mappings": [
      { "system": "H3",       "foreign_id": "8928308280fffff", "resolution": 9 },
      { "system": "W3W",      "foreign_id": "filled.count.soap" },
      { "system": "PLUS",     "foreign_id": "849VCWC8+R9" },
      { "system": "CADASTRE_US", "foreign_id": "06075010800" }
    ]
  }
```

### 5.3 Cross-System Lookup — Foreign ID → Foreign ID

Given a foreign system ID, return the equivalent ID in another foreign system (resolved through the canonical Coords URI).

```
GET /translate?from_system=H3&from_id=8928308280fffff&to_system=W3W

→ {
    "from": { "system": "H3", "id": "8928308280fffff" },
    "to":   { "system": "W3W", "id": "filled.count.soap" },
    "via":  "coords:l1:v1:37.774900,-122.419400,0.00*xxxxxxxx"
  }
```

---

## 6. Data Model Considerations

### 6.1 Point vs. Area

Some systems identify points. Some identify polygons or cells. A government parcel is an area — it may contain thousands of Coords point URIs within its boundary.

**XREF handles this by anchoring to the centroid or representative point of an area**, with the geometry type noted in the mapping. Full polygon support (storing the boundary) is a future consideration.

### 6.2 Precision and Resolution

Different systems have different precision. H3 resolution 15 is ~1m². What3Words squares are ~3m². WGS84 at 6 decimal places is ~10cm. XREF does not enforce precision matching — it records what it receives and notes the resolution.

### 6.3 Conflict Resolution

Two contributors might map different Coords URIs to the same foreign ID. XREF records all mappings but flags conflicts for community review. **No mapping is authoritative by default.** Trust is earned through contributor reputation and corroboration over time.

---

## 7. Governance and Contribution

XREF is designed to be open and contributed to by anyone. Mappings can be submitted by:

- Automated importers (H3 cells, Plus Codes — computable from coordinates)
- Community contributors (Open Tenure records, local knowledge)
- Institutional sources (government cadastral data, when available)

No single entity controls the XREF. Like the Coords protocol itself, the goal is for the XREF to be **ownerless infrastructure** — a public good that any system can query.

---

## 8. Open Questions

The following are unresolved and require further discussion:

1. **Where does XREF live?** Three options:
   - As a new repo under `coordsapp/` — natural fit since Coords URI is the canonical key
   - As a component of Fundos — since Fundos is the primary consumer
   - As a fully independent protocol — maximizes neutrality and adoption

2. **What is it named?** Working name is XREF. Candidates: Rosetta, Meridian, Nexus, GeoXREF, Pivot. TBD.

3. **Decentralized or centralized database?** A centralized database is simpler to build and query. A decentralized one is more resilient and aligned with Fundos values. Likely centralized first, decentralized later.

4. **How are polygon-to-polygon mappings handled?** A government parcel boundary and an H3 cell may overlap partially. Full spatial intersection logic is complex. Deferred to v0.2.0.

5. **Who resolves conflicts?** When two contributors map conflicting data, a governance mechanism is needed. Community voting? Stake-weighted? Reputation-based? TBD.

6. **What is the data storage format?** Likely a simple key-value or relational store to start. Blockchain-anchored state is a future consideration for Fundos integration.

---

## 9. Relationship to Fundos

Regardless of where XREF ultimately lives, its relationship to Fundos is clear:

- Every land token on the Fundos blockchain has a **Coords URI as its metadata identifier**
- The XREF is how existing real-world land records — government parcel IDs, Open Tenure records, cadastral numbers — map onto that Coords URI
- A landowner anywhere in the world can come to Fundos with whatever ID they have, and the XREF resolves it to the canonical location on the chain
- This means Fundos does not require a new global registration system — it absorbs all existing systems through the XREF

XREF is the bridge between the world as it is and the world as Fundos sees it.

---

## 10. Relationship to Coords

The Coords protocol defines the **canonical URI format and encoding**. XREF consumes that format as its primary key but does not change it. XREF is a layer on top of Coords, not a modification to it.

Whether XREF lives inside the `coordsapp` organization or separately, the Coords spec remains unchanged.

---

*End of v0.1.0 — this is a thinking document, not a final design. All sections are subject to change.*
