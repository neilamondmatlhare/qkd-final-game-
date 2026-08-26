# Phantom Q Resource Registry — 24 August 2026

The registry is deliberately conservative. `USE` means suitable now; `EVALUATE` means promising but should not be inserted into the production dependency graph until tested against Unity 6000.5.9f1 and the actual Phantom Q scene.

| Resource | Type | Verified information | Licence | Phantom Q role | Decision |
|---|---|---|---|---|---|
| Unity 6000.5.9f1 | Engine | Released 19 Aug 2026; changeset b57deb96f08d | Unity terms | Target editor | LOCK |
| URP 17.5.0 | Rendering | User-local working package baseline | Unity package | HQ rendering | USE |
| Cinemachine 3.1.7 | Camera | User-local working package baseline | Unity package | Contextual camera later | USE |
| Input System 1.20.0 | Input | User-local working package baseline | Unity package | Desktop/controller/mobile abstraction | USE |
| AI Navigation 2.0.14 | Navigation | User-local working package baseline | Unity package | Player/NPC navigation | USE |
| ProBuilder 6.1.2 | Greybox/modular geometry | User-local working package baseline | Unity package | Greybox/reference geometry | USE |
| Quaternius Modular Sci-Fi MegaKit | 3D environment | 277 models; grid based; free portion available; Source edition includes Unity URP implementation + custom shaders + optimised collisions | CC0 | Candidate architecture/doors/props | EVALUATE PRIMARY |
| Kenney Furniture Kit | 3D furniture | 140 files | CC0 | Commodity chairs/tables/furniture | USE/CURATE via optional intake |
| Kenney Factory Kit | 3D industrial | 140 files; variation/animation | CC0 | Engineering/service props | USE/CURATE via optional intake |
| Kenney Modular Space Kit | 3D modular technical | 40 assets; current 2026 pack | CC0 | Selective technical/interior props, not HQ identity | USE SELECTIVELY |
| Kenney Space Station Kit | 3D sci-fi interior | 90 files | CC0 | Selective technical/lab interior props; do not define HQ identity | EVALUATE SELECTIVELY |
| Kenney Building Kit | 3D structure | 80 files | CC0 | Secondary generic structural/utility pieces where compatible | EVALUATE SELECTIVELY |
| Kenney UI Pack | UI | 430 files | CC0 | Generic UI building blocks/reference | EVALUATE/CURATE |
| Phantom Q Q emblem (recovered from prior Phantom Q project) | Internal brand asset | Existing project-owned 256×256 emblem recovered from earlier Phantom Quantum package | Internal project asset | Reception/Central Ops branding | USE |
| BB84 Spatial Lab reference (recovered from prior Phantom Q project) | Internal visual reference | Existing 1200×630 Alice/Eve/Bob QKD lab reference recovered from earlier project | Internal project reference | Build 02/Quantum visual-density and spatial reference only | STUDY / DO NOT COPY LITERALLY |
| Poly Haven | Textures/HDRI/3D | Site-wide assets licensed CC0 | CC0 | PBR material sources/HDRI | USE/CURATE |
| NativeWebSocket 2.0.4 | Networking code | Latest listed release; Unity 6 Web support lineage | Apache-2.0 | Unity ↔ Flask/WebSocket candidate | EVALUATE WHEN INTEGRATION STARTS |
| UniTask 2.5.11 | Async code | Latest listed release; Unity 6.2+ editor deprecation fix | MIT | Async backend/hardware calls candidate | EVALUATE WHEN ASYNC COMPLEXITY WARRANTS |
| LitMotion 2.0.2 | Tween/motion code | Latest listed release; active 2026 development | MIT | UI/door/display motion candidate | EVALUATE |
| Unity Boss Room sample | Reference project | Server-authority and multiplayer patterns | Unity sample licence | Architecture reference, not drop-in dependency | STUDY |
| Unity Megacity Metro sample | Reference project | Large-scale Unity multiplayer/streaming reference | Unity sample licence | Profiling/partition reference only | STUDY SELECTIVELY |

## Source pages reviewed
- Unity 6000.5.9f1: https://activation.unity3d.com/releases/editor/whats-new/6000.5.9f1
- Quaternius Modular Sci-Fi MegaKit: https://quaternius.com/packs/modularscifimegakit.html
- Kenney Furniture Kit: https://kenney.nl/assets/furniture-kit
- Kenney Factory Kit: https://kenney.nl/assets/factory-kit
- Kenney Modular Space Kit: https://kenney.nl/assets/modular-space-kit
- Kenney Space Station Kit: https://kenney.nl/assets/space-station-kit
- Kenney Building Kit: https://kenney.nl/assets/building-kit
- Kenney UI Pack: https://kenney.nl/assets/ui-pack
- Poly Haven licence: https://polyhaven.com/license
- NativeWebSocket releases: https://github.com/endel/NativeWebSocket/releases
- UniTask releases: https://github.com/Cysharp/UniTask/releases
- LitMotion releases: https://github.com/annulusgames/LitMotion/releases

## Integration rule
Do not import all candidates simply because they exist. Each asset/package must first prove that it improves production speed or quality without creating a stronger compatibility/maintenance problem than the one it solves.

Build 02 therefore includes `PQAssetSlot` markers on procedural dressing. Those slots preserve semantic intent while allowing later replacement with curated Quaternius/Kenney/Poly Haven/custom assets without moving canonical room geometry or rewriting gameplay logic.


## Build 02 production-pass intake
`Tools/Fetch-CC0Assets.ps1` provides an optional reproducible intake for the Kenney commodity pool. `PQAssetSlotProductionResolver` only replaces semantic commodity slots when a matching model is found; it no longer uses an unrelated first-model fallback. Hero/security/QKD systems stay custom/manual. See `Docs/THIRD_PARTY_ASSET_INTAKE.md`.

## Internal Phantom Q reuse recovered during Build 02
The production pass also searches the user's existing Phantom Q work before creating replacements. Two useful internal assets were recovered from the earlier whole-game package and carried forward:

- `Assets/PhantomQ/Art/Brand/PhantomQ_Q_Emblem.png` — used as an actual in-world brand element at Reception and Central Operations.
- `Docs/ReferenceImages/BB84_SPATIAL_LAB_REFERENCE.png` — retained as a quality/spatial reference for the eventual Alice → Eve → Bob QKD experience. It is a reference, not the final character or laboratory style.

This is part of the reuse-first rule: internal approved work is checked before external libraries or new custom production.
