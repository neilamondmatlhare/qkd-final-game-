# Phantom Q Build 02 — Production Pass Implementation Report

**Prepared:** 24 August 2026  
**Target editor:** Unity 6000.5.9f1  
**Status:** source/package production pass executed; local Unity compile/render/Play Mode gate still required on the target editor.

## Base preserved

This pass started from the Codex-ready Build 02 project that had already been merged onto Build 01, compiled in Unity 6000.5.9f1, generated both HQ scenes, and fixed the prior `MaterialPropertyBlock` field-initializer defect.

## Meaningful changes executed

### Rendering
- Added `PQRenderPipelineBootstrap` to create/repair a real `UniversalRendererData` + `UniversalRenderPipelineAsset` using the URP public factory and assign it in Graphics/Quality settings.
- Build 02 generation now runs the render-pipeline guard before generating production materials.
- Camera now carries `UniversalAdditionalCameraData` with post-processing/shadows enabled.
- Added generated global Volume profile: restrained Bloom, Color Adjustments, ACES tonemapping and low vignette.
- Unity validator now checks active URP, URP Lit availability, error shaders, Standard shaders and the URP camera/Volume layer.

### Whole-HQ production language
- Preserved all canonical room sizes/relationships/IDs.
- Strengthened split lower/upper wall architecture with skirting, structural columns, open ceiling ribs, departmental accent rails and selected glass identity bands.
- Strengthened secure-door presentation with persistent frames, seam/detail, header status strip, threshold and access-reader layer while preserving the same access logic.
- Reworked prototype room lighting into emissive ceiling panels + multiple downlights + restrained fill, with one soft-shadow key per room and a lower-intensity global directional/Trilight environment.

### Quantum identity
- Preserved Alice/source, Eve/intercept and Bob/detection spatial stations.
- Added optical rail, mount/components, restrained emissive path preview and source/detector instrumentation so the room reads as a QKD laboratory at L1 rather than a generic labelled office.

### Input / UI
- Centralised movement/interact/back input behind `PQInputRouter`; player/interactions no longer directly poll keyboard/gamepad devices independently.
- Added a minimal production-facing Phantom Q HUD separate from the developer HUD, with safe late binding to room events and neutral interaction wording.

### Reuse-first asset pipeline
- Recovered the existing Phantom Q Q emblem from the user's earlier Phantom Quantum project and now reuse it as actual Reception/Central Ops in-world branding instead of recreating the mark.
- Retained the earlier BB84 Spatial Lab Alice/Eve/Bob image as an internal Quantum spatial/quality reference rather than treating it as a final locked art style.
- Added optional `Tools/Fetch-CC0Assets.ps1` for a vetted Kenney CC0 commodity pool.
- Added `PQAssetSlotProductionResolver`; it preserves gameplay roots/colliders/IDs and refuses an unrelated first-model fallback.
- Hero/security/QKD assets remain manual/custom by policy.

### Build/validation discipline
- Build 02 playable foundation is enabled in `EditorBuildSettings.asset`.
- First-import bootstrap now runs the full Production Pass under a new v3 key so this production revision regenerates on a previously used editor.
- Static validator now checks the production scripts, URP activation code, shared input route, roadmap lock, Build Settings, old-version regression, native-object field-initializer regression and `.meta` coverage.
- Project vision roadmap corrected: finish Build 02 → Build 03 complete Prologue; no immediate isolated QKD detour.

## Static result

- `python Tools/validate_spec.py` — PASS
- `python Tools/validate_build02_static.py` — PASS
- C# delimiter sanity across `Assets/PhantomQ/**/*.cs` — PASS

## Required target-editor result

This environment cannot run the user's Unity 6000.5.9f1 Editor. The handoff must therefore still run:

`powershell -ExecutionPolicy Bypass -File .\Tools\Unity.ps1 ProductionPass`

Then verify zero compiler errors, Unity validator PASS, zero magenta, whole-HQ Play Mode route and profiler evidence. Any real failure feeds back into Build 02; it is not automatically deferred to Build 03.
