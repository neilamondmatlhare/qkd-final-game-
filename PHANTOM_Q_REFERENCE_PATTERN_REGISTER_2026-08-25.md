# Phantom Q Reference Pattern Register — 2026-08-25

**Purpose:** record what mature games, Unity samples and industrial simulations teach us, and translate each lesson into a Phantom Q production decision. References inform implementation; they do not override the Master Build Contract.

## Production-success references

### Hollow Knight — Unity case study
Source: https://unity.com/made-with-unity/hollow-knight

Observed pattern:
- Team Cherry used Unity built-ins and Asset Store extensions rather than building every system from scratch.
- The saved effort was redirected to art, atmosphere and feel.

Phantom Q adoption:
- Reuse commodity tools/assets when proven.
- Keep custom effort for WS04, security/learning hero systems, Alice/Bob/Eve and QKD hardware-linked behaviour.
- Do not confuse technical novelty with product quality.

### Blue Prince — Unity/Asset Store production pattern
Source: Unity Asset Store / Unity Blue Prince feature, checked 2026-08-25.

Observed pattern:
- rapid prototyping and long iteration around reusable room/content structures;
- extensive playtime used to refine systems rather than freezing the first acceptable version.

Phantom Q adoption:
- Build 01/A1–A10 is a validated baseline, not a ban on revision;
- improve a lock only when real play/visual evidence justifies it, then rerun affected checks.

### Dave the Diver — Unity case-study pattern
Source: Unity case-study references, checked 2026-08-25.

Observed pattern:
- mature Unity systems such as URP, Cinemachine and Input System used instead of custom equivalents everywhere;
- profiling/optimization remains iterative.

Phantom Q adoption:
- retain URP/Input System/Cinemachine package baseline;
- profile before reducing detail;
- keep camera state authored by Phantom Q but use mature Unity systems when they materially improve implementation.

## Unity rendering benchmark

### URP 3D Sample — The Terminal / Oasis
Source: https://unity.com/demos/urp-3d-sample

Pattern to study:
- PBR material richness;
- lighting and post-processing used to create spatial hierarchy;
- decals/surface breakup and authored environmental density;
- multiplatform URP presentation without requiring photorealism.

Phantom Q adoption:
- Production Pass II moves the benchmark from “URP shader works” to “room has believable material/lighting/composition depth.”
- Copy techniques, not the sample's visual identity.

## Industrial-simulation references

### Unity industrial digital-twin guidance
Source: https://unity.com/resources/industrial-digital-twin-ebook

Pattern:
- a useful simulation goes beyond static 3D/animation;
- behaviour, real-time signals and hardware/controller integration remain separate from visualization;
- avoid overmodeling and siloed workflows;
- reuse an open ecosystem where it reduces development time.

Phantom Q adoption:
- authoritative simulation/physical truth stays below Unity presentation;
- physical QKD telemetry can drive the same service/state contracts as simulated QKD;
- visual fidelity increases where it improves operation/learning, not merely polygon count.

### SEW-EURODRIVE + realvirtual.io virtual commissioning
Source: https://unity.com/resources/sew-eurodrive

Pattern:
- risk-free simulation, continuous testing and standardized controller interfaces improve reliability;
- hardware/controller integration belongs behind stable interfaces rather than room-specific scripts;
- the same 3D model can support engineering, training and demonstration.

Phantom Q adoption:
- keep `IQKDService` / integration boundaries and authoritative state model;
- Build 02 HQ must remain useful later for training, physical-hardware demonstration and multiplayer rather than becoming a one-use visual set.

### Unity manufacturing use cases
Source: https://unity.com/solutions/manufacturing

Pattern:
- immersive training, design visualization and simulation share the same real-time 3D platform;
- high-fidelity simulation should be tested on the target deployment rather than reduced pre-emptively.

Phantom Q adoption:
- compact HQ uses its size advantage for detail;
- desktop 60 FPS target is measured, then web/mobile tiers are derived from evidence.

## Reusable asset sources — current review

### Kenney Furniture Kit
Source: https://kenney.nl/assets/furniture-kit
- 140 files; CC0.
- Use for commodity seating/tables/furniture after exact curation.

### Kenney Factory Kit
Source: https://kenney.nl/assets/factory-kit
- 140 files; CC0; industrial/warehouse/factory focus.
- Use for Engineering/service storage/secondary industrial dressing.

### Kenney Space Station Kit
Source: https://kenney.nl/assets/space-station-kit
- 90 files; CC0.
- Evaluate selected technical/interior props; do not let the pack define Phantom Q's architecture.

### Kenney Building Kit
Source: https://kenney.nl/assets/building-kit
- 80 files; CC0.
- Evaluate secondary structural/utility pieces in a sandbox before promotion.

### Quaternius Modular Sci-Fi MegaKit
Source: https://quaternius.com/packs/modularscifimegakit.html
- 277 models; CC0; FBX/OBJ/glTF; grid-based.
- Free subset is suitable for architecture experiments; source edition includes Unity URP implementation/custom shaders/optimized collisions.
- Treat as a module/resource source, not a final Phantom Q art identity.

## Research loop rule

For each meaningful feature:

`research → choose current best → build → play/test → compare → profile → research again → keep/replace → revalidate`

A reference changes a locked decision only when it produces a material improvement under the Master Build Contract's definition of “better.”
