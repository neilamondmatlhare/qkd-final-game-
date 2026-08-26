# Phantom Q — Third-Party Asset Intake

**Reviewed:** 24 August 2026  
**Rule:** reuse commodity assets; custom-build the objects that define Phantom Q's identity, learning behaviour, security semantics and QKD apparatus.

## Automatic optional CC0 intake

`Tools/Fetch-CC0Assets.ps1` can fetch a small vetted commodity pool into `Assets/ThirdParty/Kenney`. A failed download does **not** invalidate the project; the deterministic production placeholders remain active until a vetted replacement exists.

| Pack | Primary use | Licence | Official source |
|---|---|---|---|
| Kenney Furniture Kit | chairs, tables, general office furniture | CC0 | https://kenney.nl/assets/furniture-kit |
| Kenney Factory Kit | Engineering/service storage and industrial dressing | CC0 | https://kenney.nl/assets/factory-kit |
| Kenney Modular Space Kit | selective technical interior modules/props | CC0 | https://kenney.nl/assets/modular-space-kit |
| Kenney UI Pack | generic UI primitives/reference | CC0 | https://kenney.nl/assets/ui-pack |

The convenience downloader uses OpenGameArt mirrors for the ZIP payloads; licence/source decisions are based on the official Kenney pages.

## Manually evaluated sources

### Quaternius Modular Sci-Fi MegaKit

Candidate for structural wall, door, corridor, glass and technical modules. It should be curated rather than used as a single visual identity. Phantom Q geometry, access boundaries, signage, material language and camera cutaway rules remain authoritative.

Official source: https://quaternius.com/packs/modularscifimegakit.html

### Additional Kenney candidates found during the production loop

- **Space Station Kit** — 90 CC0 3D files; candidate for selective technical/lab props.
- **Building Kit** — 80 CC0 3D files; candidate for secondary structural/utility pieces.

They remain evaluation candidates rather than automatic dependencies; the whole-HQ Phantom Q material/scale/signage language remains authoritative.

### Poly Haven / ambientCG

CC0 PBR material/HDRI sources. Use selectively for concrete, metal, glass-adjacent surfaces and environmental material detail. Imported textures must be reviewed for resolution/memory cost before production use.

- https://polyhaven.com/license
- https://ambientcg.com/

## Internal project reuse comes before third-party intake

Build 02 also checks prior Phantom Q packages before creating or downloading replacements. The current production pass recovered:

- `Assets/PhantomQ/Art/Brand/PhantomQ_Q_Emblem.png` — canonical reusable Phantom Q brand artwork, now used by the HQ production builder.
- `Docs/ReferenceImages/BB84_SPATIAL_LAB_REFERENCE.png` — an earlier Alice/Eve/Bob BB84 lab visual retained as a spatial/quality reference for the Quantum Wing.

These are **not third-party dependencies**. They are recorded here because the intake order is deliberate: existing Phantom Q work → Unity/mature libraries → vetted external assets → custom build only where necessary.

## Asset-slot policy

`PQAssetSlot` is a semantic replacement point, not permission to replace gameplay objects blindly.

**Commodity slots suitable for automatic/fast replacement:** seating, ordinary desks, racks/storage, generic industrial instruments and non-hero terminals.

**Keep custom or manually curated:** Workstation 04, Phantom Q access readers/secure doors, Foundations evidence system, Crypto workbenches, Communications network wall, SOC case/trace systems, Red Team target/authorisation consoles, Alice/Bob/Eve persistent character assets, and the physical/digital QKD apparatus.

## Intake gate

Before an external asset becomes part of the canonical build, check:

1. source and licence;
2. Unity 6000.5.9f1 / URP compatibility;
3. scale and orientation;
4. shader/material compatibility (no Standard/error shader in the active scene);
5. collider complexity;
6. texture/memory cost;
7. WebGL/IL2CPP/mobile implications where relevant;
8. whether it materially improves the project over the current production placeholder.

A newer or prettier asset is not automatically better. Integration must preserve A1–A10 and stable IDs.
