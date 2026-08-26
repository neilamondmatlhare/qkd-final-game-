# Phantom Q Build 02 — Production Pass III: Full-HQ Authored Upgrade

**Status:** large whole-HQ production upgrade, not a micro-validation pass.  
**Target:** Unity 6000.5.9f1.  
**Roadmap:** still Build 02. Build 03 Prologue remains blocked until the HQ is visually/playably accepted.

## Why this pass is deliberately larger

Production II proved the render pipeline and exposed the next problem: the scene was structurally stronger but still read as a procedural environment. The returned evidence also showed lighting overexposure and high ceiling/service elements blocking the raised-oblique camera. Most important, the curated asset resolver reported zero applied replacements even though the CC0 packs had been downloaded.

Production III therefore makes a **large** step in one pass:

`lighting recovery → camera-aware architecture → exact commodity replacement → authored room dressing across all 11 spaces → full-HQ visual density`

The pass does not enlarge the canonical A4 footprint. It makes the existing compact HQ denser, more believable and closer to the approved slide/environment direction.

## Approved visual references carried in the project

`Docs/ReferenceImages/HQ_Approved_Design_Deck_2026-08-25/`

1. `01_Arrival_HQ.png` — readable headquarters, entrance path, glass/office/technical identity, visible restricted facilities.
2. `02_Functional_Zones.png` — every area must visibly support a capability: Learn / Operate / Attack-Test / Monitor-Respond / Engineer.
3. `03_Capability_Expansion.png` — dense compact HQ with distinct room equipment and colour families.
4. `04_Character_Movement.png` — raised-oblique room readability, direct movement and contextual interaction.
5. `05_Digital_Physical_QKD.png` — simulation and real hardware are two providers of the same authoritative QKD event model.

These references are design targets, not exact floor-plan replacements. `HQ_CANONICAL_SPEC.json` remains spatial authority.

## Room completion standard

### Exterior / Arrival
Must read as a real Phantom Q facility before the player reaches Reception: façade rhythm, controlled approach, double-door entrance, columns/glazing, plants, arrival lighting and brand identity. Do not expand into a large campus.

### Reception / Identity
Corporate and secure rather than lobby-only: real waiting furniture, identity workstations, access display, plants, T0 threshold and visible route toward Central Ops.

### Central Operations
The visual heart of HQ. Uses a real workstation ring/U arrangement, main operational wall, HQ Command/Authorisation side, staff workstations, clear central aisle and **WS04 as persistent hero anchor**. Room identity must not depend on a floating label.

### Training & Foundations
Learning through evidence and objects: collaborative tables, evidence/timeline wall, fact-assumption-unknown area, source/transfer/receiver reasoning and enough circulation for guided interaction.

### Cryptography
Must communicate protect/transform/verify: symmetric and asymmetric zones, secure key/trust cabinets, real consoles, seating and trust/signing display. Hero crypto benches remain Phantom Q custom.

### Communications
Must communicate transmit/route/remote endpoint: real computer stations, infrastructure cabinets, route wall, source/remote endpoint positions and visible channel relationship.

### SOC
Must read as investigation/correlation rather than a monitor wall: central Trace Table remains hero custom, analyst stations surround it, evidence wall, side display, infrastructure cabinets and incident-preservation capacity.

### Red Team
Must preserve `AUTHORISE → TARGET/SCOPE → OPERATE`. Real consoles and secure storage add density, but room access remains separate from action authority.

### Engineering
Must become a real workshop: industrial machine, robot arm, scanner, worktables, screens, parts crates, tool storage, service pipes, racks and equipment route. Use commodity assets aggressively here rather than procedural cubes.

### Quantum Wing
Must communicate `Alice/source → optical path → Eve/intercept → Bob/receiver` before labels. Custom QKD table/rails/roles remain, with real station computers, instruments, racks, optical mounts, cable/service infrastructure and clear Alice/Eve/Bob floor zones. Presentation never becomes QKD truth.

### Advanced Compute
Infrastructure density + central simulation/processing station. Visually distinguish from Communications through compute banks and model/simulation focus.

### Secure Core
Restrained high-trust architecture. Central protected machine, shield/structure and status interface; do not clutter it like another office.

## Exact asset use in this pass

The local returned project already contains the downloaded Kenney CC0 packs. Production III now populates exact mappings for commodity slots rather than leaving the map empty. Additional authored dressing directly uses exact known assets from:

- Kenney Furniture Kit;
- Kenney Space Station Kit;
- Kenney Factory Kit;
- Kenney Building Kit.

Imported materials are converted on instantiated production visuals to URP/Lit copies so third-party Standard materials do not recreate the magenta problem.

Hero assets remain custom: WS04, evidence board, crypto benches, communications hero display, SOC trace table, Red Team target/authorisation systems, Quantum optical table/Alice/Eve/Bob apparatus and hero characters.

## Lighting correction

Production III deliberately lowers room-light intensity, fill intensity, bloom, exposure and emissive pulse range. The goal is not a dim HQ; it is **readable PBR/material detail** rather than white/cyan clipping.

## Camera-aware architecture correction

A9 cutaway is extended to high beams, ceiling ribs, overhead rails, cable trays and service elements. These objects remain part of the world but can hide when they obstruct the camera-to-player line.

## Run

```powershell
.\Tools\Unity.ps1 ProductionPassIII
```

Then use Play Mode. If Codex finds compile/import issues, repair them in this same pass rather than reducing the scope back to small incremental geometry changes.
