# Phantom Q Engineers — Build 02 Locks and Continuous Validation Loop

Date baseline reviewed: 2026-08-24

## Build objective
Build 02 is the **Whole HQ Playable Production Foundation**. It must move Build 01 from a dimensional greybox to a coherent, playable Headquarters foundation without fragmenting the building into unrelated room projects.

## Non-negotiable world locks
- One persistent Phantom Q Headquarters.
- Central Operations is the spatial/narrative heart and Workstation 04 persists.
- Arrival: Exterior → Reception/Identity → T0 → Central Operations.
- Foundations remains close to Central Ops.
- Crypto and Communications form a tightly linked specialist cluster.
- Communications bridges Central Ops, Crypto and SOC.
- SOC is close to normal operations but access-controlled.
- Red Team sits one security layer deeper than SOC.
- Engineering begins the deeper technical branch.
- Quantum is deeper/more specialist than Engineering and must reserve meaningful physical QKD space.
- Advanced Compute is parallel to Quantum.
- Secure Core is the deepest high-trust destination and is not a through-route.
- Technical/service spine exists for engineering/quantum equipment movement.
- Fixed raised-oblique world orientation; cutaway walls rather than free camera rotation.
- Player capability/access is role + zone + mission + action-authority based, not one numeric clearance level.
- Characters move because of role. Alice is operational/source-oriented; Bob is remote; Eve is authorised security support; Red Team operates primarily SOC ↔ Red Team.
- Rooms have distinct gameplay verbs: Reception identify, Central Ops operate, Foundations reason, Crypto protect, Communications transmit, SOC investigate, Red Team engage, Engineering build, Quantum measure, Advanced Compute simulate.

## Campaign continuity locks
The current campaign remains a continuous operational arc, not isolated tutorials. Build 02 does not rewrite campaign narrative. It builds the persistent world that will later host the Prologue and Incidents 01–06.

## Unity target baseline
- Unity Editor: `6000.5.9f1`
- Unity changeset: `b57deb96f08d`
- `com.unity.ai.navigation`: `2.0.14`
- `com.unity.cinemachine`: `3.1.7`
- `com.unity.inputsystem`: `1.20.0`
- `com.unity.probuilder`: `6.1.2`
- `com.unity.render-pipelines.universal`: `17.5.0`

This baseline came from the user's locally working Build 01 import and supersedes the original Build 01 package versions.

## Reuse-first engineering rule
For commodity functionality/assets:
1. Check Unity built-in capability.
2. Check mature/open-source/commercial library.
3. Check inspectable reference implementation.
4. Build custom only when Phantom Q genuinely needs custom behaviour/identity.

Every external dependency/resource must be checked for licence, source, maintenance, Unity compatibility, performance, WebGL/IL2CPP/mobile risk and whether it actually saves effort.

## Continuous loop
A stage being passed means **current validated baseline**, not frozen forever.

`research → compare → reuse/adapt → build → play/test → profile → research again → improve → revalidate → continue`

If a later build reveals a materially better solution, update the earlier decision and rerun downstream checks. Do not change locked work casually; change it because evidence justifies the change.

## Build 02 scope
- Preserve Build 01 canonical geometry.
- Whole-HQ L1 architectural/visual pass.
- URP-safe material generation (no magenta fallback accepted).
- Split lower/upper walls + camera cutaway system.
- Security doors/readers at T0/T1/T2/T3/T4/T5.
- Room detection + room camera profiles.
- Representative interaction framework and four representative interactions.
- Initial room dressing for every major room.
- Initial ambient staff presence and Alice prototype.
- Navigation surface.
- Resource replacement slots so procedural dressing can be swapped for vetted production assets without changing gameplay IDs/geometry.
- Static and Unity-side validators.

## What Build 02 intentionally does not claim
- Final characters/animations.
- Final room art.
- Final QKD apparatus asset quality.
- Complete campaign/prologue logic.
- Final multiplayer/backend integration.
- Final performance certification on target hardware.

Those are later builds. Build 02 is the stable production foundation they plug into.
