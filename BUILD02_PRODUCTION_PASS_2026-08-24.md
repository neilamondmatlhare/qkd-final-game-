# Build 02 — Whole HQ Playable Production Foundation: Production Pass

**Target:** Unity 6000.5.9f1  
**Purpose:** advance the complete A1–A10 HQ from validated structural foundation to a coherent playable production foundation without jumping early to Build 03.

## Execution chain

```text
Known-good Build 02
→ activate and validate URP
→ regenerate canonical Build 01 skeleton
→ generate whole-HQ Build 02 production layer
→ apply vetted commodity asset replacements when available
→ enable Build 02 scene in Build Settings
→ run Unity validator
→ Play Mode whole-HQ walkthrough
→ profile
→ A1–A10 loop
→ Build 02 lock
```

Run locally:

```powershell
.\Tools\Unity.ps1 ProductionPass
```

The command optionally attempts the CC0 commodity intake, then opens Unity in batch mode and executes the Build 02 Production Pass. If the network is unavailable, the pass continues using deterministic production placeholders.

## Changes in this production pass

- Real URP pipeline/renderer bootstrap and quality assignment rather than only having the URP package installed.
- Validator now fails if URP is not active or error/Standard shaders remain in the active Build 02 scene.
- Camera has URP additional camera data and post-processing enabled.
- Global Volume profile is generated with restrained ACES tonemapping, colour adjustment, bloom and vignette.
- Room lighting moves from one prototype point light to emissive panels + multiple downlights + restrained fill light.
- Architectural language strengthened with structural columns, trims, accent rails, glass identity bands, doorway frames/status strips and open ceiling ribs.
- Quantum L1 identity strengthened with optical rail, source/intercept/detection stations, optical mounts and a restrained path preview.
- Minimal production HUD improved and remains distinct from the developer HUD.
- Input is routed through one `PQInputRouter` abstraction rather than being polled independently by player/interactions.
- Optional third-party resolver refuses unrelated fallback models and preserves canonical roots/colliders/IDs.
- Build Settings are made deterministic for `02_HQ_PLAYABLE_FOUNDATION.unity`.
- Existing Phantom Q Q-emblem artwork recovered from the earlier project is now reused directly in Reception and Central Operations; the earlier BB84 Spatial Lab visual is retained as a Quantum quality/spatial reference.

## What remains a local Unity gate

This package cannot be truthfully called visually complete until Unity 6000.5.9f1 has:

1. compiled with zero errors;
2. generated the URP assets/Volume profile/materials/scenes;
3. passed `Phantom Q > Build 02 > Validate Current Build 02 Scene`;
4. been walked in Play Mode from exterior through the full HQ route;
5. shown zero magenta/error materials;
6. been profiled on the target PC.

Those results should feed back into this build rather than being deferred automatically to Build 03.
