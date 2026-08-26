# Codex Runbook — Build 02 Production VI

## Objective

Compile the existing canonical HQ into the high-grade environment target without reducing scope. Characters stay deferred.

## Primary commands

```powershell
.\Tools\Unity.ps1 ProductionPassVI
.\Tools\Unity.ps1 CaptureEvidenceVI
```

Optional PBR intake before the pass:

```powershell
.\Tools\Fetch-PolyHaven-PBR.ps1
```

## Repair policy

If Unity reports API/import/material/prefab issues, repair the implementation and rerun. Do **not** solve errors by deleting Production VI, restoring visible greybox walls, dropping rooms, removing the architectural skin, or moving to Build 03.

## Expected scene roots

- `BUILD02_PRODUCTION_LAYER_V_REFERENCE_COMPILED_HQ` — curated commodity/hero-proxy V layer retained as reusable content.
- `BUILD02_PRODUCTION_VI_ARCHITECTURAL_SKIN` — new visible room shell/floors.
- `BUILD02_PRODUCTION_VI_AUTHORED_ENVIRONMENT` — room-specific built-in composition.
- `BUILD02_PRODUCTION_VI_LIGHTING` — broad architectural lighting.

The Build 01/Build 02 greybox remains underneath for geometry/colliders/IDs but its visible wall/floor skin is suppressed.

## Evidence

`CaptureEvidenceVI` writes 16 1920×1080 views to `Docs/VisualEvidence/Build02_ProductionVI/` using room-specific investor/player compositions. Foreground cutaway surfaces are hidden only when they block the focal subject.
