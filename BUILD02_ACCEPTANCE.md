# Build 02 Acceptance Gate — Production Foundation

Build 02 is promoted only when **static package validation + Unity generation/validation + Play Mode visual/handling evidence** all pass.

## A. Static package gate

- Unity target = `6000.5.9f1` / `b57deb96f08d`.
- Package manifest and `packages-lock.json` match the known-good local baseline.
- Build 01 canonical builder remains present.
- Build 02 Production Pass, URP bootstrap, validator, interaction, cutaway, input, HUD and asset-slot systems are present.
- Resource registry and third-party intake record exist.
- `.meta` coverage under `Assets` is complete.
- No known old package/editor baseline remains in active project/readme configuration.

Run:

```text
python Tools/validate_spec.py
python Tools/validate_build02_static.py
```

## B. Unity 6000.5.9f1 generation gate

1. Package Manager/import and compilation become idle.
2. Console has **zero compiler errors**.
3. Run `Phantom Q > Build 02 > Run Full Production Pass`.
4. Confirm real `PQ_URP.asset` + `PQ_URP_Renderer.asset` are generated and active.
5. Confirm generated scenes:
   - `Assets/PhantomQ/Scenes/01_HQ_MASTER_GREYBOX.unity`
   - `Assets/PhantomQ/Scenes/02_HQ_PLAYABLE_FOUNDATION.unity`
6. Confirm Build Settings contains the enabled Build 02 playable-foundation scene.
7. Run `Phantom Q > Build 02 > Validate Current Build 02 Scene` and confirm **PASS**.
8. Confirm **zero magenta**, `Hidden/InternalErrorShader`, or active Built-in `Standard` materials in the scene.

## C. Whole-HQ Play Mode gate

Walk:

`Exterior → Reception → T0 → Central Ops → Foundations → Crypto ↔ Communications → SOC → T2/Red Team → Engineering → Quantum → Advanced Compute → Secure Core threshold`

Verify:

- camera stays raised-oblique/fixed orientation and room profiles remain within A9 ranges;
- upper-wall cutaway preserves room readability;
- doors/readers work with developer access, then enforce restrictions with it disabled;
- room identity is visible through architecture/equipment, not only floating labels;
- Alice conversation, WS04, Foundations evidence board, and Crypto workbench operate;
- minimal HUD is readable and debug HUD remains separate;
- Quantum visibly contains Alice/source, Eve/intercept, Bob/detection and optical-path structure;
- no major NPC/prop blocks circulation or key interaction markers.

## D. Visual/production gate

- Whole HQ has one coherent Phantom Q material/lighting language.
- Every major room has L1 production dressing; no single hero room is polished while the rest remains raw cubes.
- Commodity asset replacements are vetted; hero/security/QKD systems remain controlled.
- The pink/error-shader problem is solved globally through URP configuration/material validation, not manually patched per object.

## E. Performance gate

Profile on the target PC and record:

- FPS;
- CPU and GPU frame time;
- batches/draw calls;
- memory;
- spikes/GC observations.

Optimise measured bottlenecks rather than reducing quality pre-emptively.

## F. Continuous A1–A10 loop

A Build 02 PASS is the current validated baseline, not a ban on improvement. If real furniture, camera behaviour, QKD equipment footprint or other evidence reveals an earlier design problem, improve it for a documented reason and rerun dependent checks.

**Only after this gate passes does Build 03 — Complete Prologue Vertical Slice begin.**
