# Build 02 — Production Pass V: Whole HQ Visual Compile

**Target:** Unity 6000.5.9f1 / URP 17.5.0  
**Scope:** all 11 canonical HQ spaces + arrival + service spine  
**Characters:** no new character production in this pass  
**Purpose:** convert the approved visual target into the actual persistent Unity HQ at large scale.

## What changed in production method

The pass no longer treats room dressing as a sequence of hand-built primitives. The production chain is:

`canonical skeleton → compiled reusable prefabs → room compositions → Phantom Q hero composites → balanced lighting → AI Navigation → investor evidence`

Build 01/A1–A10 remains the geometric authority. The new layer is visual/operational composition on top of that foundation.

## Reusable prefab chop-shop

`PQProductionPrefabCompilerV` converts vetted Kenney Furniture / Factory / Space Station / Building models into a reusable Phantom Q prefab library under:

`Assets/PhantomQ/Art/Prefabs/ProductionV/`

Repeated furniture, infrastructure and architecture are therefore instantiated as prefabs rather than recreated as cubes or raw FBX placements in every room.

## Whole-HQ room compile

`PQHQProductionLayerV` builds the full environment in one milestone:

- exterior forecourt and façade;
- Reception/Identity workflow and lounge;
- Central Ops mission-control floor, WS04 frame and HQ Command island;
- Foundations evidence/timeline and Fact/Assumption/Unknown stations;
- Crypto symmetric/asymmetric/trust zones;
- Communications rack banks, route wall and source/remote endpoints;
- SOC analyst perimeter, central trace table, incident/evidence wall and preservation infrastructure;
- Red Team authority zone, target/scope table and controlled operations positions;
- Engineering electronics benches, real industrial equipment, repair/assembly, storage and overhead services;
- Quantum Alice/Eve/Bob control positions, optical table/rail, instrumentation, detector/source/intercept clusters and rack/service infrastructure;
- Advanced Compute rack banks and simulation island;
- Secure Core protected centre and security ring;
- technical service spine.

## Lighting

`PQLightingProductionV` disables broad room-fill lighting, caps old downlights, adds modest room key lights, reduces emissive pulses and applies a low-bloom ACES profile so PBR/material detail remains readable.

## Navigation

`PQNavigationProductionV` rebuilds the existing Unity AI Navigation/NavMesh surfaces after dressing. The project does not invent a separate pathfinder.

## Investor proof

`PQInvestorEvidenceCaptureV` creates 18 fixed 1920×1080 captures from the same Build 02 scene. These are implementation evidence, not concept renders.

## Local execution

```powershell
.\Tools\Unity.ps1 ProductionPassV
.\Tools\Unity.ps1 CaptureEvidenceV
```

Codex should repair ordinary compile/import/scale/API issues while preserving the large room scope. A technical error is not permission to revert the environment to primitive-only dressing.

## Build 03 gate

Build 03 remains blocked until the whole-HQ environment is visually/playably accepted and profiled. Production V is deliberately a large world-production pass so later campaign work can use the HQ rather than rebuild it.

## Production V final assembly refinements

- Production V now **supersedes and removes the old Production II/III visual-density roots** before compiling the final environment, preventing doubled primitive furniture/hero geometry.
- The canonical Build-01/Build-02 gameplay skeleton remains underneath; only the superseded visual-density layers are removed.
- Large floating greybox department labels are disabled in the compiled presentation; room identity must come from architecture/equipment plus the minimal room HUD.
- `PQEnvironmentOptimizationV` uses Unity static batching/occludee/reflection-probe flags on the compiled visual environment rather than introducing a custom render-management system.
- Production-V lighting now adds three low-resolution, once-on-load reflection probes and a sparse whole-HQ LightProbeGroup to support later dynamic content.
- Characters remain intentionally outside this production pass.
