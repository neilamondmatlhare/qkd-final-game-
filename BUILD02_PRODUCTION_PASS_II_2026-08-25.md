# Build 02 — Production Pass II: Whole-HQ Authored Density + Rendering Recovery

**Date:** 2026-08-25  
**Target editor:** Unity 6000.5.9f1  
**Build boundary:** still Build 02. Build 03 remains blocked until visual/Play Mode/full-scope acceptance passes.

## Why this pass exists

The previous Production Pass proved the whole-HQ structure and Unity generation, but a real screenshot showed magenta rendering and the environment still read predominantly as procedural building blocks. Production Pass II therefore targets two linked problems without changing the canonical HQ:

1. recover/verify URP rendering globally;
2. substantially increase whole-HQ authored visual density and production identity.

## Execution order

```text
same canonical Production Pass
→ global rendering recovery
→ regenerate exact Build 01 + Build 02 foundation
→ rendering recovery/invalid-shader scan again
→ apply Production Layer II to all 11 spaces + exterior/service spine
→ apply exact curated asset map only
→ Unity base + Production II validation
→ save same playable Build 02 scene
→ human Play Mode / profiler / full-scope review
```

## Rendering recovery

`PQBuild02RenderingRecovery`:
- ensures the real Phantom Q URP pipeline/renderer is active;
- forces import of required URP Lit/Unlit shader assets;
- reimports the Phantom Q URP assets;
- inspects Phantom Q materials;
- repairs only genuinely invalid, error-shader or Built-in Standard assignments;
- scans active scene renderers and refuses promotion if invalid assignments remain;
- reloads the same `02_HQ_PLAYABLE_FOUNDATION.unity` scene rather than creating a replacement visual prototype.

## Project-local first import

The earlier global `EditorPrefs` first-import marker has been replaced by:

`Library/PhantomQ/Build02_ProductionPassII_v1.ok`

`Library` is excluded from distribution, so every fresh extraction receives its own initialization state.

## Production Layer II

`PQHQProductionLayerII` adds an authored non-authoritative visual layer without moving room volumes/IDs/doors/WS04/campaign markers.

### Exterior / Reception
- actual facade backbone and architectural glazing;
- entrance canopy lighting, pylon, bollards, planters and approach emphasis;
- identity/access portal composition.

### Central Operations
- operational ring composition;
- HQ Command/Authorisation dais;
- overhead structure and stronger WS04 zone emphasis;
- Central Ops remains spatial/narrative heart.

### Foundations
- evidence timeline wall;
- Fact / Assumption / Unknown manipulation table;
- object-led investigation identity.

### Cryptography
- secure key/trust cabinets;
- asymmetric/trust work zone;
- stronger lab wall treatment.

### Communications
- route table;
- rack banks and live endpoint/network identity.

### SOC
- central trace/correlation table;
- evidence/timeline wall;
- rack infrastructure;
- investigation density rather than decorative monitor count.

### Red Team
- physically separate Authorise → Target/Scope → Operate concepts;
- room access still does not imply action authority.

### Engineering
- electronics/test and assembly/repair bench zones;
- industrial storage;
- cable trays and explicit service/equipment route.

### Quantum Wing
- enlarged optical table identity;
- two optical rails, pedestal/mount sequence and path guide;
- explicit Alice Source → Eve Intercept → Bob Receiver spatial stations;
- instrumentation/racks/cable route;
- physical-QKD room remains presentation of authoritative physical/simulated truth, not the truth itself.

### Advanced Compute / Secure Core
- compute rack banks and central processing island;
- Secure Core stays visually high-trust/minimal rather than being filled with invented gameplay.

### Lighting/reflection support
- three low-resolution realtime reflection-probe regions;
- HQ LightProbeGroup for staff/hero characters;
- restrained emissive motion only on state/identity accents.

## Curated reuse change

The former keyword-first resolver has been removed from production authority.

Current flow:

`fetch vetted source → import sandbox → generate catalog → inspect → write exact assetPath mapping → apply exact mapping`

`PQAssetIntakeCatalog` inventories models but never changes the scene. `PRODUCTION_ASSET_MAP.json` is the only automatic promotion source.

Hero assets remain custom/HERO_LOCK as defined by `PRODUCTION_ASSET_MANIFEST_2026-08-25.json`.

## Local commands

```powershell
.\Tools\Unity.ps1 RenderingRecovery
.\Tools\Unity.ps1 FetchCC0
.\Tools\Unity.ps1 CatalogAssets
.\Tools\Unity.ps1 ProductionPassII
.\Tools\Unity.ps1 CaptureEvidence
```

Recommended normal path:

```powershell
.\Tools\Unity.ps1 ProductionPassII
.\Tools\Unity.ps1 CaptureEvidence
```

## Promotion gate

Do not call Build 02 complete until the target editor provides evidence for:
- zero compiler errors;
- Production II validator PASS;
- zero visible magenta/error shaders;
- full exterior → Secure Core threshold walkthrough;
- camera/cutaway/access/HUD/representative interactions observed;
- room identities recognizable without relying on giant labels;
- target-PC profiling;
- A1–A10 rerun against dressed geometry;
- full-scope role-play acceptance review.

## Visual proof helper

After a successful Unity generation, `Tools/Unity.ps1 CaptureEvidence` renders 12 fixed raised-oblique PNGs (exterior + 11 canonical spaces) from the same Build 02 scene into `Docs/VisualEvidence/Build02_ProductionII`. Upper cutaway walls are hidden only for the capture. This gives Codex/reviewers a repeatable whole-HQ visual comparison before/after changes; Play Mode acceptance remains mandatory.
