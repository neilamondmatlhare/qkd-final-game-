# Phantom Q Engineers — Build 01 Validation Report

## Status

**Specification-level validation: PASS** before Unity import.

The included Unity Editor validator runs again after the greybox scene is generated. It checks the canonical room centres/footprints, Workstation 04, security transitions, player controller, oblique camera, Alice prototype and NavMeshSurface.

## Loop checks applied

| Earlier decision | Build 01 implementation check |
|---|---|
| A1 — one persistent operational HQ | One master greybox scene; no room-as-level split |
| A2 — Central Ops is the heart | Central Ops remains at `(0,0,0)` with four primary route directions |
| A3 — critical adjacency | Explicit transition geometry for Ops↔Foundations, Ops↔Communications, Comm↔Crypto, Ops/Comm↔SOC, SOC↔Red Team, Engineering↔Quantum |
| A4 — canonical room geometry | All 11 room centres and footprints encoded in builder and validator |
| A5 — campaign routes | Early campaign cluster remains compact; no mandatory hub return inserted |
| A6 — character routes | Alice uses internal Central Ops entry marker and WS04 marker; Bob remains deliberately absent as a physical NPC |
| A7 — clearance | T0/T1/T2/T3/T4/T5-equivalent secure door objects use a zone access profile; dev override can be toggled |
| A8 — interaction distribution | WS04 and specialist room markers are present; specialist systems remain future build steps rather than being faked into one terminal |
| A9 — camera/handling | 60° pitch, 45° yaw, 40° FOV, 15 m distance, 3.2 m/s player baseline |
| A10 — partition | Build 01 stays as one master scene first; folder structure is ready for later production partitioning |

## Important intentional limits of Build 01

This is the **whole-HQ greybox and systems baseline**, not finished art and not the complete campaign. It intentionally does not fabricate final crypto/SOC/QKD interfaces before their interaction systems are built and tested. Cinemachine and ProBuilder are installed in the project, but the first deterministic camera/geometry baseline uses lightweight runtime/editor code so the master layout can be regenerated and audited consistently.

## Unity-side pass condition

Do not call the HQ greybox locked until all of the following are true in Play Mode:

1. Player can enter from the south approach and navigate the whole building with developer access enabled.
2. Camera preserves orientation and does not require manual rotation.
3. T0/T1/T2/T3/T4/T5 door objects are visible and behave consistently.
4. Current room changes correctly in the developer HUD.
5. Alice can traverse her prototype route without being blocked.
6. Central Ops, Foundations, Communications, Crypto, SOC and Red Team route lengths feel compact rather than tedious.
7. Engineering, Quantum, Advanced Compute and Secure Core feel deeper without breaking the HQ mental map.
8. No room centre or footprint differs from `HQ_CANONICAL_SPEC.json` without a documented reason.

If a Play Mode test fails, modify the greybox and rerun **Phantom Q → Build 01 → Validate Current HQ Scene** before continuing to room polish or campaign implementation.
