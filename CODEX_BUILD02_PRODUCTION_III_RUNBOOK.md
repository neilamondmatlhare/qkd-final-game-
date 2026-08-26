# Codex Runbook — Build 02 Production Pass III

## Intent

Do **not** turn this into another small validation-only iteration. The user has explicitly requested a large production push. Preserve A1–A10 and fix compile/import problems, but keep the full-HQ authored scope.

## Primary command

```powershell
.\Tools\Unity.ps1 ProductionPassIII
```

Production III performs the existing rendering recovery/base generation, Production II structure, exact curated commodity replacement, full-HQ Production III dressing, lighting recovery and camera-aware obstruction tagging.

## What Codex should repair if Unity reports errors

- compile/API compatibility in Unity 6000.5.9f1;
- FBX material import/URP conversion issues;
- missing exact asset paths if a Kenney package layout differs;
- oversized/undersized imported assets by correcting Production III target size/yaw/position;
- camera blockers or circulation problems caused by authored dressing;
- overexposure remaining after the global lighting tuner.

Do not solve an error by deleting the whole Production III layer or returning to primitive-only rooms.

## Visual target

Use the five approved reference images under `Docs/ReferenceImages/HQ_Approved_Design_Deck_2026-08-25/` alongside the Master Build Contract and Full-Scope Roleplay Acceptance. They show the intended density, professional HQ identity, room-specific equipment and raised-oblique readability.

## Priority order if fixes are required

1. zero compile errors / same canonical scene;
2. no magenta third-party materials;
3. lighting readable rather than clipped;
4. Central Ops, SOC, Engineering and Quantum retain their authored hero composition;
5. all other rooms keep the large density pass;
6. movement/cutaway/door access remains usable.
