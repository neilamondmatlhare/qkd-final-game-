# Codex Runbook — Build 02 Production Pass V

## Mission

Compile the approved visual target into the existing canonical HQ. Do not redesign A1–A10 and do not reduce the pass to one hero room.

## Primary command

```powershell
.\Tools\Unity.ps1 ProductionPassV
```

Then:

```powershell
.\Tools\Unity.ps1 CaptureEvidenceV
```

## Expected compile chain

1. rendering recovery / URP guard;
2. canonical Build 02 foundation regeneration;
3. Production II architectural base layer;
4. reusable Production V prefab compilation from vetted Kenney source assets;
5. whole-HQ Production V scene compile;
6. balanced Production V lighting;
7. camera-aware high-service tagging;
8. Unity AI Navigation rebuild;
9. base + milestone Production V validation;
10. save.

## Repair policy

If Unity reports an API, import, material, prefab, collider, NavMesh or asset-orientation issue, fix that implementation issue. Do **not** respond by deleting the affected room, reverting the environment to cubes, removing the reusable prefab approach, or starting Build 03.

## Character boundary

Do not spend this pass on final Alice/Bob/Eve or ambient character art. Preserve existing representative character roots/interactions where needed, but environment production is the priority.

## Visual standard

Use `Docs/ReferenceImages/ProductionV_Target_2026-08-25/` as composition/quality guidance and `HQ_CANONICAL_SPEC.json` as geometry authority. Every major room must read by function without relying on its floating label.

## Production V final assembly refinements

- Production V now **supersedes and removes the old Production II/III visual-density roots** before compiling the final environment, preventing doubled primitive furniture/hero geometry.
- The canonical Build-01/Build-02 gameplay skeleton remains underneath; only the superseded visual-density layers are removed.
- Large floating greybox department labels are disabled in the compiled presentation; room identity must come from architecture/equipment plus the minimal room HUD.
- `PQEnvironmentOptimizationV` uses Unity static batching/occludee/reflection-probe flags on the compiled visual environment rather than introducing a custom render-management system.
- Production-V lighting now adds three low-resolution, once-on-load reflection probes and a sparse whole-HQ LightProbeGroup to support later dynamic content.
- Characters remain intentionally outside this production pass.
