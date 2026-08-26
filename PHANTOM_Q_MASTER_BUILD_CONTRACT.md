# Phantom Q Engineers — Master Build Contract

**Status:** Canonical whole-project guardrail  
**Established:** 2026-08-25  
**Applies to:** Unity HQ, campaign, QKD simulation, multiplayer, website, video, physical QKD integration, classroom/demo deployment, and future acts.

## 1. Purpose

This document sits above build-specific notes. It exists to prevent a later build, agent, asset pack, prototype, or visual improvement from drifting away from the product already agreed.

A **lock is a validated baseline, not frozen dogma**. It may change only when testing, stronger evidence, an improved reference implementation, or an explicit product decision shows that a different solution is materially better. Any such change must trigger revalidation of the dependent design.

### Authority order

1. Current explicit user instruction and subsequently approved decisions.
2. `Docs/HQ_CANONICAL_SPEC.json` for exact HQ spatial data, stable IDs, room geometry and transitions.
3. This Master Build Contract for whole-product intent and non-negotiable experience rules.
4. `Docs/PHANTOM_Q_PROJECT_VISION.md` for consolidated experience detail.
5. Build-specific implementation/acceptance documents for the capability of that build.
6. Earlier prototypes and historic documents only when they are not superseded by later decisions.

Do not silently revive an older decision because it exists in a previous prototype.

---

## 2. Product definition

**Phantom Q Engineers is a persistent, industry-oriented cybersecurity and quantum-engineering learning/game platform.** The learner should experience why each security capability becomes necessary, operate meaningful systems, make decisions with consequences, inspect evidence, and progressively earn responsibility.

The campaign logic is:

`ordinary work → anomaly → investigation → protection → key problem → identity/trust problem → quantum threat/QKD → attack-surface shift → operational compromise → trusted recovery command → hunt → contain → recover → restore → unresolved adversary`

The current Act I playable backbone is:

1. Foundations
2. Symmetric Security
3. Asymmetric Security
4. Quantum Threat
5. QKD
6. Physical QKD / secure-link challenge

The currently locked recovery campaign remains Prologue + Incidents 01–06 and must retain its previously approved facts, PQ-001/PQ-004 continuity, A7/S1 logic, R100/R1,000 transaction continuity, and unresolved actor.

---

## 3. Four connected delivery blocks

| Block | Role |
|---|---|
| **Game / Unity HQ** | Main playable world, campaign, roles, progression, practical interaction, QKD, multiplayer. |
| **Website** | Introduction, navigation, project/media presentation, support shell, route into the game/demo. |
| **Video** | Trailer and longer demonstration using real gameplay/evidence rather than fake feature claims. |
| **Physical QKD** | Alice/Bob/Eve hardware, calibration, detector/motor telemetry, real QBER/intrusion evidence, hardware-linked gameplay. |

They must connect but must not substitute for one another.

---

## 4. Core experience laws

### 4.1 One persistent HQ

- The HQ is one operational engineering/security organisation, not a level-select menu.
- Central Operations is the spatial/narrative heart.
- Workstation 04 is persistent.
- The same rooms change operational state as the campaign evolves.
- Restricted/future spaces should often be visible before accessible.
- The building remains compact and legible; detail increases, not map sprawl.

### 4.2 Whole before sections

`design whole → validate relationships → build whole greybox → test whole system → engineer subsystems → plug them into same HQ`

Do not create one beautiful disconnected room while the rest of the HQ remains structurally or visually abandoned.

### 4.3 Object-led learning

The preferred teaching sequence is:

`Brief → Predict → Configure → Run → Inspect → Decide → Explain`

Use physical objects, equipment, movement, state change and consequence before long explanatory text. UI supports the world; it does not replace it.

### 4.4 The system owns truth

For QKD and all security-critical mechanics:

`authoritative simulation / physical truth → role-safe state → Unity presentation`

Animation never creates truth. A completed animation cannot by itself declare that a photon was sent, a detector fired, a signature verified, an attack succeeded, or a key is valid.

### 4.5 No role owns the whole truth

During active QKD/multiplayer play:

- Alice knows what she prepared and sent.
- Bob knows what he selected/measured.
- Eve knows her intercept/measurement/resend actions.
- Control/observer knows readiness and authorised operational status.
- Hidden states remain hidden until the protocol permits disclosure or sealed review.

The server must not transmit secret data simply because a client UI hides it.

### 4.6 Capability can be shared; live information remains role-specific

Universal mechanics may exist across roles, but current-round information is filtered by role and authority.

### 4.7 High-risk actions require narrow authority

Room access is not equivalent to unrestricted action authority.

`identity + role + capability + zone permission + mission grant + target/action-specific authority`

Red Team entry does not mean “attack anything”. Financial recovery authority is separate from cyber authority.

### 4.8 Cyber offence remains fictional and authorised

The game may teach attack/defence thinking, but current campaign operations use fictional systems, scoped targets, explicit authority and safe abstractions. Do not turn Incident 06 into real exploit instruction.

---

## 5. Roles and organisation

Persistent narrative/technical roles:

- **Alice** — sender/protector/origin.
- **Bob** — receiver/verifier.
- **Eve** — authorised adversarial/security-test perspective; not presumed culprit.
- **Player/Trainee** — progressing Phantom Q member; not automatically HQ Command.
- **SOC** — monitor, investigate, correlate, preserve, contain.
- **Red Team** — authorised active response after verified authority.
- **Engineering** — hardware, electronics, instrumentation, integration.
- **Quantum** — optical/QKD practical capability.
- **Instructor/Observer** — room/role orchestration, readiness, sealed review, classroom supervision.

Eve must never be framed as guilty merely because she is the adversarial role.

---

## 6. Headquarters locks

The exact spatial specification remains in `HQ_CANONICAL_SPEC.json`. Conceptually the HQ must preserve:

- Entrance / Reception / Identity
- Central Operations
- Training & Foundations
- Cryptography Lab
- Communications
- SOC
- Red Team Operations
- Engineering
- Quantum Wing
- Advanced Compute
- Secure Core

Security depth and capability are communicated through physical boundaries, visibility, doors/readers, room state and access policy rather than only numeric levels.

Camera remains raised oblique / 2.5D, fixed world orientation, Sims-style cutaway logic, direct movement plus contextual auto-align/pathing.

---

## 7. Game modes and future capability

The product should support the following without requiring a second unrelated game:

- Guided Learning
- Challenge Missions
- Sandbox / Practice Lab
- Multiplayer Room
- Classroom / Host mode
- Mission/Campaign mode
- Competition formats including A+B+E vs A+B+E and possible Red-vs-Blue variants
- Solo play with automated hidden-information-safe roles
- Role rotation after sealed review
- Cross-role proficiency and capability progression

Future capability may include persistent adversary/final-boss structures, but current campaign facts must not be rewritten to force them early.

---

## 8. Multiplayer and local deployment

Current deployment baseline:

`Unity / web clients → local Raspberry Pi → Flask authoritative services → SQLite → QKD engine / physical hardware`

- Same-Wi-Fi classroom operation is the current baseline.
- One Alice, Eve and Bob seat per room/session when using the three-role mode.
- Independent room lifecycles, reconnects, chat/files/reviews and teacher multi-room view remain product requirements.
- Do not introduce Cloudflare/hosted infrastructure at this stage unless a later explicit decision changes the deployment model.
- React/TypeScript remains appropriate for web/dashboard/support surfaces; Unity is the main real-time 3D game world.

---

## 9. Physical QKD integration

The physical system must remain an engineering truth source, not a decorative prop.

Required conceptual apparatus:

`Alice source/encoder → quantum channel → Eve intercept/analyser/resend → Bob basis selector/PBS/detectors`

plus a separate authenticated classical channel and a safe review/replay layer.

Physical and simulated modes should share the same command/state contracts where practical. Real motor/detector/calibration telemetry may be exposed in Engineering/Diagnostics views without overwhelming the learner-facing experience.

---

## 10. Interface and learning support

- Minimise reading during active play.
- One clear objective and success condition at a time.
- Terminal, files, notes and chat are tools/drawers, not the whole game.
- Maintain a Linux-like safe `pqsh` terminal where it strengthens understanding; the terminal and physical controls must call the same validated services.
- Guidance can operate as Guided, Assisted, Independent and Challenge modes.
- Help must respect role-specific information.
- Desktop and phone layouts are separately composed; phone is not a shrunken desktop.
- Accessibility must include readable text, reduced motion options, input abstraction, strong navigation assistance and appropriate colour/state redundancy.

---

## 11. Art, character and world direction

- Stylised-realistic 3D: believable proportions, simplified faces/materials, not hyper-photoreal and not childish cartoon.
- South African diversity appears naturally in staff/characters without stereotypes.
- Once hero characters are approved, Alice/Bob/Eve/trainee silhouettes, clothing/badges and proportions remain persistent.
- Commodity environment assets may be reused; Phantom Q identity is established through scale, materials, lighting, composition, branding, hero equipment and interaction design.
- The compact HQ should use its size advantage to achieve high environmental density and quality.

---

## 12. Reuse-first production rule

For every commodity problem:

`Unity built-in → mature/open-source/commercial resource → inspectable reference implementation → custom only where Phantom Q genuinely benefits`

Custom effort is prioritised for:

- Workstation 04
- Phantom Q access/security hero systems
- Foundations evidence interactions
- Crypto workbenches
- Communications network systems
- SOC trace/correlation systems
- Red Team authority/operation systems
- Persistent Alice/Bob/Eve characters
- QKD apparatus and hardware-linked behaviour
- Campaign-specific evidence and narrative assets

Do not confuse “reuse-first” with “install everything”. Every dependency must pass licence, compatibility, maintenance, performance, platform and Phantom Q fit review.

---

## 13. Continuous external-reference loop

Research is not a one-off pre-production task.

For each meaningful feature:

1. Search current Unity capability.
2. Search mature reusable/open-source/commercial solutions.
3. Study successful games and industrial simulations for the same production problem.
4. Build the smallest correct implementation.
5. Test it in Phantom Q.
6. Compare the real result to the reference patterns.
7. Profile and observe learners/users.
8. Improve or replace weak implementation.
9. Re-run affected locks and acceptance tests.

A passed stage may be revisited if evidence shows a materially better solution.

---

## 14. Current build roadmap

1. **Build 01 — Canonical whole-HQ greybox** — complete baseline.
2. **Build 02 — Whole HQ Playable Production Foundation** — current build; must reach whole-HQ visual/handling/interaction acceptance.
3. **Build 03 — Complete Prologue vertical slice** — starts only after Build 02 passes.
4. Incidents 01–06 integrated through the same HQ foundation.
5. Deeper QKD, multiplayer, physical-hardware integration and future acts extend the same architecture.

Do not redirect Build 02 into an isolated QKD demo.

---

## 15. Build 02 completion gate

Build 02 is not complete until all are evidenced in Unity:

- zero compiler errors;
- active compatible URP and zero error/magenta shaders;
- whole HQ has production-level L1 architecture/material/lighting identity;
- room identities are visually distinct without relying on floating labels;
- full exterior → Secure Core threshold walkthrough works;
- camera/cutaway/doors/access/representative interactions work;
- WS04 remains canonical;
- Engineering and Quantum read as real technical spaces;
- representative NPC/staff life exists;
- performance is captured on target hardware;
- A1–A10 are rerun against the dressed geometry;
- full-scope role-play acceptance is reviewed;
- any changed lock is documented with reason.

---

## 16. Superseded decisions

These remain historical context but are not current authority:

- Cloudflare D1/R2/Durable Objects as the current deployment baseline.
- React Three Fiber as the main 3D QKD/HQ engine.
- Single-player-only or same-screen role tabs as the final multiplayer design.
- CSS/precomputed “3D” as the final QKD simulation.
- A single linear numeric clearance level as the core access model.
- Treating Eve as the assumed culprit.
- Using a beautiful isolated room/QKD prototype as a substitute for the whole HQ.

---

## 17. Definition of “better”

A new approach is better only if it materially improves one or more of:

- learning clarity;
- player agency;
- scientific/security correctness;
- role privacy;
- visual/readability quality;
- implementation speed;
- maintainability;
- device/platform support;
- classroom reliability;
- physical-hardware integration;
- measurable performance;

without unacceptable regression elsewhere.

