# Phantom Q — Visual-to-Unity Production Blueprint

**Purpose:** convert approved Phantom Q visual intent into a repeatable Unity production system without rebuilding the HQ from scratch.

## Production rule

`approved visual target → structural decomposition → reusable prefab families → room recipe → Unity generation → investor evidence`

The canonical map is not redesigned. `HQ_CANONICAL_SPEC.json` remains the spatial authority. Visual references determine density, composition, material treatment, operational landmarks and room character.

## Structure-for-structure translation

Each reference image is decomposed into nine layers:

1. **Spatial skeleton** — room bounds, transitions, stable IDs, WS04 and interaction anchors from the canonical spec.
2. **Architecture kit** — wall, glass, secure wall, doors, ceilings, columns, trims, services and cutaway elements using base prefabs + variants.
3. **Commodity asset library** — furniture, racks, instruments, storage, plants and infrastructure from vetted reusable sources.
4. **Hero systems** — Phantom Q-specific interactive equipment and campaign anchors.
5. **Room production recipe** — explicit composition and density rules for each department.
6. **Material language** — shared Phantom Q PBR treatment that visually unifies mixed-source assets.
7. **Movement/navigation** — Unity AI Navigation and room-specific route anchors; no custom pathfinder unless proven necessary.
8. **Camera/presentation** — PQ state decides why the camera changes; Cinemachine/cutaway machinery handles framing and obstruction.
9. **Evidence output** — deterministic investor and acceptance captures from the same playable scene.

## Investor proof principle

Investor evidence must demonstrate implemented systems, not only aspirational concept art. For each major capability keep a pair:

`design target / reference → actual Unity capture`

The preferred proof sequence is:

`Arrival → Reception → Central Ops / WS04 → Foundations → Crypto → Communications → SOC → Red Team → Engineering → Quantum → Advanced Compute → Secure Core`

At least one capture per major room must show: architecture, hero landmark, ordinary operations, circulation and interaction readiness. Quantum evidence must additionally show the Alice → Eve → Bob apparatus relationship. Engineering evidence must show real workshop density. SOC evidence must show evidence/correlation workflow rather than decorative monitors.

## Room maturity rule

A room is not visually complete because it has a label and furniture. It reaches production maturity when:

- the department is recognisable without its floating label;
- one hero landmark explains the department purpose;
- ordinary supporting props make the space believable;
- full 3.2 m vertical composition is used without breaking the raised-oblique camera;
- circulation remains clear;
- the room can host its future verbs and lesson modules;
- its materials/lighting belong to the same Phantom Q organisation.

## Lesson plug-in principle

Further lessons must plug into the existing HQ rather than spawning a second disconnected tutorial game.

A lesson module declares:

- required zone(s);
- role/capability prerequisites;
- required interaction anchors;
- objective sequence using `Brief → Predict → Configure → Run → Inspect → Decide → Explain`;
- authoritative service(s) it consumes;
- role-safe information projections;
- optional physical-hardware binding;
- completion evidence;
- reset/retry behaviour.

The lesson may change room state, equipment state, dialogue, evidence and permitted interactions. It may not move canonical geometry or bypass access/security truth.

## Reuse-first implementation

Use Unity Prefabs/Prefab Variants for repeated architecture and props so changes propagate through the whole HQ. Unity's prefab system is specifically designed to reuse and synchronise configured GameObjects, while variants provide controlled room/security/lab specialisations.

Use Unity AI Navigation for NavMesh generation, dynamic obstacles and links. Do not write a new pathfinding engine unless profiling/behaviour proves the package inadequate.

Use existing vetted asset libraries for commodity objects. Custom effort is reserved for Phantom Q hero systems, characters, QKD apparatus, campaign evidence and unique operational interfaces.

## Build 02 target after this blueprint

Build 02 should become a reusable *world platform* rather than a single finished scene. After this layer, Build 03 and later incidents should primarily add mission data, room states, lesson modules, dialogue/evidence and new hero systems—not rebuild reception desks, navigation, room shells or camera logic.
