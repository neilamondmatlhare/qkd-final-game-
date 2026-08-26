# Build 02 Production Pass VI — Source Implementation Report

Date: 2026-08-25
Base: Production V Whole-HQ QA handoff (technical PASS; visual gate failed)
Target: High-grade reference-driven environment; characters deferred

## QA findings converted directly into implementation

Production V proved the canonical map, prefab import, NavMesh and whole-HQ population. Its visual QA failed because the visible shell still read as a greybox/prop layout, the lighting created clipped pools against black rooms, and the evidence camera read as a construction survey.

Production VI therefore changes **environment production**, not the HQ foundation.

## Environment implementation added

- 7 bundled tileable architectural textures: graphite panels, light stone, dark floor tile, technical floor, brushed metal, acoustic panel and concrete.
- 18-material Production VI URP palette including controlled glass and room accents.
- 7 reusable architectural kit prefabs compiled once: operational, security, technical, core, normal glass, secure glass and ceiling/light rail.
- whole-HQ room skin derived algorithmically from existing `PQRoomVolume` bounds; no new floor-plan source was introduced;
- base greybox renderers for floor/wall/ceiling skin are suppressed while colliders, persistent IDs, room triggers and canonical coordinates remain;
- secure-door positions are detected and architectural wall modules skip those openings;
- authored room composition across Reception, Central Ops, Foundations, Crypto, Communications, SOC, Red Team, Engineering, Quantum, Advanced Compute and Secure Core;
- character/prototype renderers are hidden for this environment-only milestone without deleting their logic objects;
- Production V spotlight-pool lighting is replaced by broad room ambient lights, one controlled hero key, feature-wall wash, Trilight ambient and restrained ACES/bloom;
- Production VI investor capture uses lower room-specific compositions and hides only cutaway surfaces intersecting the camera-to-focus ray;
- optional `Tools/Fetch-PolyHaven-PBR.ps1` is provided for CC0 PBR material replacement, with bundled fallback textures keeping the build deterministic/offline capable.

## Static/source checks executed here

- `python Tools/validate_spec.py` — PASS, 11 rooms / 14 transitions / 26 physical edges / A1–A10.
- `python Tools/validate_build02_static.py` — PASS.
- `python Tools/validate_build02_production_v_static.py` — PASS on retained technical base.
- `python Tools/validate_build02_production_vi_static.py` — PASS.
- C# delimiter sanity — PASS across 66 source files.

## Required target-editor work

Run Unity 6000.5.9f1:

```powershell
.\Tools\Unity.ps1 ProductionPassVI
.\Tools\Unity.ps1 CaptureEvidenceVI
```

Codex should repair compile/API/import errors without deleting room scope or returning to visible greybox walls. Visual sign-off requires reviewing the 16 rendered VI captures plus the whole-HQ Play Mode route and profiler evidence.
