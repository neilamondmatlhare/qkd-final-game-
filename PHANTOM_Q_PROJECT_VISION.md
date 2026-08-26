# Phantom Q — Project Vision, Experience Architecture, and Delivery Guardrails

**Status:** Persistent project memory / design guardrails  
**Consolidated:** 2026-08-24  
**Applies to:** Phantom Q Engineers, the Unity HQ project, the QKD simulation, the website, media, and eventual physical-QKD integration.

## Why this document exists

Phantom Q has already had extensive product, game, QKD, campaign, spatial, interface, and delivery discussion. New contributors and future build generators must read this document before proposing or generating work. Its purpose is to preserve the agreed direction so that the team does not repeatedly rebuild a disconnected dashboard, isolated room, or decorative prototype.

This is a concise decision record, not a raw chat transcript. It intentionally preserves the decisions that affect implementation. Exact HQ dimensions, IDs, transitions, and coordinates remain in `Docs/HQ_CANONICAL_SPEC.json`.

## Source and decision order

This document consolidates:

1. The shared **Game Development Planning** conversation and its linked QKD/product discussions, reviewed on 2026-08-24.
2. The A1–A10 Headquarters design documents and the master HQ design supplied with the project.
3. `Docs/HQ_CANONICAL_SPEC.json` and the Build 01/Build 02 lock documents.
4. The actual local Build 02 import, compile, generation, and validation results.

When sources appear to conflict, use this order:

1. Current user instruction and an explicit subsequently approved decision.
2. `HQ_CANONICAL_SPEC.json` for exact spatial data and stable IDs.
3. This document for whole-product intent and experience rules.
4. Build-specific implementation documents for the capabilities of that build.

Do not silently reinterpret a locked decision. Change it only when evidence, testing, or an explicit product decision justifies it; record the reason and revalidate dependent work.

---

## 1. The product being built

**Phantom Q is an industry-quality, playable cybersecurity and quantum-key-distribution learning experience.** It is not a static lesson, a shallow “click-to-win” simulation, or a fashionable dashboard with QKD labels.

It teaches security foundations, symmetric encryption, asymmetric encryption, and QKD through role-play, missions, practical decisions, visual evidence, and later a physical QKD demonstrator. The player should understand what they are doing, make decisions with consequences, inspect the evidence, and explain the security outcome.

The product has four connected, but distinct, delivery blocks:

| Block | Purpose |
|---|---|
| **Game** | The main playable HQ, missions, roles, progression, QKD simulation, and multiplayer experience. |
| **Website** | A responsive introduction to the game, its roles, QKD concepts, progress, media, and a route to play/test a demo. |
| **Video** | A public trailer and a longer development/investor demonstration based on real gameplay and evidence. |
| **Physical QKD integration** | Alice, Bob, and Eve hardware measurements, calibration, QBER, intrusion evidence, and the interface that makes those real events meaningful in the game. |

The website introduces the project; the video demonstrates it; the game is the core experience; and the physical bench enriches the game with genuine evidence. None is a substitute for the others.

### What success feels like

The player enters a convincing engineering/security organisation, receives a clear role and mission, operates meaningful equipment, sees a coherent physical/QKD story unfold, makes a security judgement, and can replay the resulting evidence. The system should feel like a serious training experience that happens to be engaging—not an entertainment shell hiding a worksheet.

---

## 2. Experience rules that must not be broken

- Do not present all roles as tabs or panels inside one crowded control screen.
- Do not pre-calculate the outcome and use timed animation to pretend that it is interactive.
- Do not let one role see another role’s secret state during an active round.
- Do not replace actual equipment and causal events with excessive text, metrics, or decorative UI.
- Do not call sifted bits a final secret key.
- Do not imply that a PDF or ordinary file travels inside a photon. QKD establishes key material; a later authenticated classical-channel exercise can demonstrate encrypted file transfer.
- Do not split the HQ into unrelated “levels” that lose its spatial/security meaning.
- Do not replace the full HQ foundation with a visually attractive but disconnected room prototype.
- Do not make phone presentation a shrunken version of three desktop stations.
- Do not treat a generated archive, a pretty scene, an idea, or untested code as a completed feature.

---

## 3. The live QKD experience

The central simulation must be state-driven and scientifically defensible. The real order of truth is:

```text
Simulation or physical truth
        ↓
Local Alice / Eve / Bob state
        ↓
Shared authoritative session state
        ↓
Role information policy
        ↓
Role-specific 3D scene, interface, animation, and character guidance
```

Animation can show a verified event, but its completion must never cause Alice to send, Eve to measure, or Bob to receive. The QKD engine determines the facts; presentation responds to them.

The system must accurately support the teaching path from photon states and bases through measurement, basis mismatch, intercept-resend attack, multi-round sifting, QBER sampling, accept/abort decisions, reconciliation, privacy amplification, and a secure-payload demonstration. Later engineering/sandbox work can introduce loss, detector efficiency, dark counts, misalignment, and timing.

The actual apparatus should be visually meaningful:

- Alice’s source, attenuator, and polarisation encoder.
- The quantum channel.
- Eve’s tap, analyser/detectors, and replacement source.
- Bob’s basis selector, polarising beam splitter, and detectors.
- A separate authenticated classical channel.
- A replay timeline that exposes the causal sequence only after it is safe to reveal it.

Buttons, physical-equipment controls, and the planned safe `pqsh` terminal must call the same validated command service. Entering `measure --basis x` must produce the same authorised action as operating Bob’s analyser in the scene.

---

## 4. Role separation, privacy, and multiplayer

One shared session is experienced through separate, full-size role environments.

| Role | Primary space and actions | Must remain hidden while live |
|---|---|---|
| **Alice** | Source laboratory; choose state/basis, prepare, lock, calibrate, and transmit. | Eve’s interception/results and Bob’s unrevealed choices. |
| **Eve** | Interception laboratory; pass/intercept, choose a basis, measure, and resend. | Alice’s original secret state and Bob’s choices. |
| **Bob** | Receiver laboratory; choose a basis, arm/measure, sift, sample QBER, and accept or abort. | Alice’s unrevealed state and Eve’s activity. |
| **Control/observer** | Assign roles, show readiness, start/pause/recover, then inspect a sealed replay. | Private bits, bases, measurements, and attacks during active play. |

Each player has a private camera, objective, equipment, contextual controls, information policy, and guide character. In solo play, unplayed roles may be automated, but their hidden data must remain hidden. Roles cannot be swapped mid-session; swapping happens after the sealed review.

Multiplayer is a core game capability, not a decorative add-on. It ultimately supports role assignment, readiness barriers, reconnection, presence, room communication, instructor/observer control, and server-enforced filtering of private information. The server must not send secret state merely because a client hides it visually.

---

## 5. Learning, assistance, and interface direction

The repeatable mission loop is:

```text
Brief → Predict → Configure → Run → Inspect → Decide → Explain
```

Every active phase should show one clear objective, one success condition, and the relevant controls. Everything else stays collapsed until it is useful.

Learners can choose narration, captions, visual explanation, hands-on manipulation, or concise notes. These are options, not permanent labels that restrict a learner to one “learning style.” Guidance must progressively reduce:

- **Guided:** explain the next action.
- **Assisted:** state the objective without giving the answer.
- **Independent:** remain quiet unless help is requested.
- **Challenge:** do not reveal secret-dependent information.

Alice, Bob, and Eve are operational guides as well as characters. When help is needed, the relevant character points to equipment, gives one short instruction, and offers **Show me**, **Why?**, or **I understand**. A guide has access only to the information permitted to that role.

The role-specific 3D station remains dominant. Notes, chat, terminal, and files are drawers on desktop; on phone they are focused, full-screen tools. The active equipment and immediate decision must never be obscured. Use a responsive composition for each device rather than simply stacking or shrinking the desktop layout.

Visual direction is object-led and human: stylised but believable Alice, Bob, and Eve; inspectable equipment; readable lighting; clear state changes; and restrained, purposeful animation. The rich visual reference is the quality target. It does **not** justify bypassing the QKD engine, role separation, or the HQ architecture.

---

## 6. The Phantom Q Headquarters

The HQ is one persistent operational engineering/security organisation, not a menu of disconnected rooms. Central Operations is its spatial and narrative heart, and Workstation 04 remains a stable anchor.

The A1–A10 work locks the headquarters’ meaning, hierarchy, adjacency, full floor plan, campaign routes, character routes, clearance logic, interactions, camera/handling, and later Unity partitioning. The canonical building contains Reception/Identity, Central Operations, Foundations, Communications, Cryptography, SOC, Red Team, Engineering, Quantum, Advanced Compute, Secure Core, and the technical/service spine.

Important world rules:

- Arrival is Exterior → Reception/Identity → T0 → Central Operations.
- Foundations is close to Central Ops; Crypto and Communications are a specialist cluster; Communications bridges operational and security areas.
- SOC is close but access-controlled; Red Team is deeper than SOC.
- Engineering starts the deeper technical branch; Quantum has meaningful physical-QKD space; Advanced Compute is parallel to it; Secure Core is the deepest destination and never a through-route.
- Access is based on **role + zone + mission + action authority**, not a simplistic numeric clearance ladder.
- Rooms have distinct verbs: identify, operate, reason, protect, transmit, investigate, engage, build, measure, simulate, and secure.
- The camera maintains the raised-oblique orientation and uses cutaway walls rather than unrestricted free rotation.

Build the whole HQ first and validate walking distance, sightlines, rooms, routes, clearance boundaries, character movement, and camera handling as one physical system. Only after the greybox/world is proven should production scene partitioning be used for loading and organisation. Scenes are implementation partitions, not separate game levels.

---

## 7. Campaign and progression intent

The campaign is a continuous operational arc, not a series of isolated tutorials. Security foundations, symmetric encryption, asymmetric encryption, and QKD should build on each other. The Prologue and Incidents 01–06 are the narrative/mission framework; future work converts the approved story into actual objectives, dialogue, equipment states, consequences, and replayable evidence.

Capability and equipment unlocks can broaden what a player can do, but they must never replace learning, security judgement, or meaningful role action. A player should be able to fail, identify why, recover, and understand the result.

---

## 8. Current Unity reality — Build 02

**Build 02 is a whole-HQ playable production foundation, not the completed Phantom Q game.** It is the structural building block that later QKD roles, missions, art, characters, hardware, and multiplayer must plug into.

What is currently established in the local workspace:

- The Build 01 canonical 11-room HQ and its A1–A10 spatial validation baseline are preserved.
- Build 02 adds whole-HQ L1 dressing, split walls/cutaway handling, room camera profiles, T0–T5 readers/doors, room detection, representative interactions, navigation, staff presence, Alice prototype, and resource replacement slots.
- The Build 02 source was reconciled with **Unity 6000.5.9f1** and the compatible package set, then compiled and generated successfully in the installed local Unity editor.
- The generated `01_HQ_MASTER_GREYBOX.unity` and `02_HQ_PLAYABLE_FOUNDATION.unity` scenes exist.
- A real Unity bug in `PQAccessReaderVisual` was corrected: `MaterialPropertyBlock` is now created lazily rather than in a MonoBehaviour field initializer.

What Build 02 does **not** claim yet:

- Final character models, animation, room art, or final QKD apparatus assets.
- A complete Prologue/Incidents campaign.
- The authoritative QKD role simulation described above.
- Final multiplayer/backend or physical-QKD integration.
- Target-device performance certification or final visual-quality approval.

Do not present Build 02 as the final game. Present it honestly as the validated HQ/world base for the next vertical slice.

---

## 9. Recommended delivery order from here

The master roadmap is **whole-world foundation before narrative vertical slice**. A QKD slice must not be used to bypass unfinished Build 02 world production.

1. **Finish Build 02 — Whole HQ Playable Production Foundation.** Activate/validate URP, eliminate magenta/error materials, complete the whole-HQ L1 architecture/material/lighting/dressing pass, refine camera/cutaway/input/presentation, run the full HQ walkthrough, profile, and rerun A1–A10.
2. **Build 03 — Complete Prologue vertical slice.** Exterior arrival → Reception/Identity → credential workflow/Eve authorised check → T0 → Central Ops/Workstation 04 → Alice/USB/files → Bob remote → anomaly → PQ-001 → Foundations unlock. This becomes the first complete narrative slice in the finished HQ foundation.
3. Build Incidents 01–03 through the reusable interaction/campaign systems, preserving the locked campaign continuity.
4. Build Incidents 04–06 and trusted-command/recovery systems through the same HQ, SOC and Red Team architecture.
5. Build the deeper role-specific QKD/physical-QKD experience in the Quantum Wing using the authoritative state/role-separation rules defined above; do not substitute decorative animation for simulation truth.
6. Strengthen multiplayer rooms, persistence/replay, server role filtering, chat/files/terminal and physical hardware integration through proven interfaces.
7. Use real gameplay, test evidence and hardware evidence for the responsive website, trailer and investor demonstration.

Research/reuse continues during every step. A passed stage remains the current validated baseline and can be improved when new evidence or a materially better implementation justifies the change; downstream checks must then be rerun.

---

## 10. Implementation and packaging discipline

- Target the installed Unity version: **6000.5.9f1**. Keep `ProjectVersion.txt`, `manifest.json`, and the matching `packages-lock.json` together.
- Include generated scenes and all Unity `.meta` files when packaging source. Do not package `Library`, `Temp`, `Logs`, `UserSettings`, or IDE-generated files.
- Retain canonical IDs and `HQ_CANONICAL_SPEC.json`; do not move gameplay-critical objects merely to make dressing easier.
- Use the existing resource-slot approach for vetted external/custom assets, checking licence, maintenance, Unity compatibility, mobile/WebGL/IL2CPP risk, and performance before adoption.
- Never instantiate Unity native objects such as `MaterialPropertyBlock` in a MonoBehaviour field initializer or constructor; initialise them in `Awake`, `Start`, or lazily in a runtime method.
- Validate after every meaningful change: specification/static checks, Unity compile/scene validation, Play Mode walkthrough, interaction checks, and profiling where relevant.
- “Done” means the result exists, works in the shared build, has evidence, has been reviewed/reproduced by someone else where possible, documents limitations, and does not depend on its creator being present to repair it.

## 11. Change log

| Date | Change |
|---|---|
| 2026-08-24 | Initial consolidated project-vision record created from shared planning, canonical HQ sources, and Build 02 validation work. |

