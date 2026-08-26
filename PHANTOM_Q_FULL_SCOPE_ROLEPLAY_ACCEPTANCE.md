# Phantom Q — Full-Scope Role-Play and Acceptance Review

**Purpose:** Evaluate each build by playing through the product from every important human/system perspective, not only by checking whether the Unity scene opens.

This document is an acceptance lens. Build 02 does not need to implement every future feature listed here, but it must not architecturally block them.

## 1. New trainee / first-time player

### Journey
`Exterior → Reception → Identity → T0 → Central Ops → WS04`

### Must feel
- entering a real engineering/security organisation;
- clear orientation without a mandatory minimap;
- future capability visible but protected;
- WS04 is a real operational anchor;
- prompts are short and contextual.

### Failure signs
- HQ reads as a collection of labelled cubes;
- player needs large paragraphs to understand every room;
- all departments look identical;
- restricted spaces are invisible until magically unlocked;
- camera fights the player.

## 2. Player during the current campaign

### Campaign route test
- Prologue: Reception → Central Ops.
- I01: Central Ops → Foundations.
- I02/I03: Crypto ↔ Communications → Central Ops.
- I04: Central Ops → Communications → SOC.
- I05: SOC ↔ Crypto/Communications → Red Team threshold.
- I06: SOC ↔ Red Team → Central Ops restoration.

### Acceptance
Movement should occur because operational purpose changed, not because every scene requires a new room. Central Ops is an anchor, not a mission lobby.

## 3. Alice — sender/protector/origin

### Live QKD role
`prepare → choose/lock source state → transmit → later compare permitted public information → decide what can be kept`

### Must know
- her own prepared state/basis/bit;
- her own source and transmission state;
- public information only when protocol permits it.

### Must not know live
- Eve’s hidden choice/result;
- Bob’s unrevealed basis/result.

### Environment implication
Alice requires a genuine source/preparation station, not a generic terminal. Her physical route through HQ should primarily use Central Ops, Crypto and Communications before later Quantum work.

## 4. Bob — receiver/verifier

### Live QKD role
`signal arrives → choose measurement basis → measure → build raw results → compare public bases → inspect disturbance → accept/abort`

### Must know
- his selected basis;
- detector/measurement result;
- public comparison data after reveal.

### Must not know live
- Alice’s unrevealed source state;
- Eve’s hidden intervention.

### Environment implication
Bob is physically remote in the current campaign but becomes a real receiver station in QKD. The game must support remote presence without pretending Bob is standing in every HQ room.

## 5. Eve — authorised adversarial/security-test role

### Live QKD role
`unknown signal → choose pass/intercept → choose basis → measure → resend → attempt to remain undetected`

### Must know
- her own intervention choice;
- her own measurement;
- her own resend state.

### Must not know live
- Alice’s true unrevealed state;
- Bob’s secret basis/result.

### Narrative rule
Eve is not automatically the campaign culprit. Her authorised security work must remain visibly legitimate.

## 6. Instructor / observer / classroom host

### Needs
- create/join room;
- assign Alice/Eve/Bob;
- view readiness without secret state leakage;
- start/pause/recover a session;
- observe room health;
- handle reconnection;
- inspect sealed replay after the round;
- manage several classroom rooms later.

### Must not see live
private bits/bases/measurements/attacks unless the mode explicitly authorises a teaching demonstration that changes the rules before the round begins.

## 7. Solo learner

Automated roles may act on behalf of missing players, but hidden information must remain hidden from the human learner. Solo mode must use the same authoritative protocol state, not a special fake sequence.

## 8. SOC analyst perspective

### Verbs
`investigate → filter → correlate → trace → preserve → assess → contain`

### Acceptance
SOC must feel like evidence work, not a wall of decorative monitors. The learner should manipulate case/timeline/trace/evidence systems and understand why a conclusion follows.

## 9. Red Team operator perspective

### Verbs
`validate target → request authority → verify signed scope → engage controlled action → search → preserve evidence → report`

### Acceptance
- access to Red Team is not attack authority;
- target/service/action authority must be explicit;
- offensive presentation remains professional and fictional;
- the room must physically support target case, authorisation and operation as separate concepts.

## 10. Engineering / hardware operator

### Verbs
`build → connect → measure → calibrate → test → diagnose → repair`

### Acceptance
Engineering cannot look like another office. It needs benches, instrumentation, parts/storage, equipment circulation and a service route. Large hardware should not need to pass through Reception/Central Ops.

## 11. Quantum lab / physical demonstrator operator

### Must support
- Alice source/encoder;
- Eve intercept/analyser/replacement source;
- Bob selector/PBS/detectors;
- control electronics;
- physical or simulated mode;
- calibration/diagnostics;
- learner-safe presentation;
- sealed replay;
- classical-channel comparison.

### Acceptance
The room should communicate the optical path spatially before the learner reads labels. Physical telemetry drives state; Unity presentation does not fabricate it.

## 12. Mobile learner

### Acceptance
- phone UI is not a shrunk desktop layout;
- movement and one contextual action remain usable;
- role equipment stays readable;
- chat/files/notes/terminal open as focused tools;
- hidden information policy remains identical to desktop.

## 13. Multiplayer learner

### Acceptance
- one shared session, separate private workspaces/cameras/objectives;
- server-enforced hidden information;
- readiness barriers;
- reconnection without leaking state;
- chat/file transfer where relevant;
- no mid-round perspective switching that reveals secrets.

## 14. Classroom deployment / local IT operator

### Baseline
`clients → same Wi-Fi → Raspberry Pi / Flask / SQLite → authoritative room/QKD services`

### Acceptance
- explicit room records/codes;
- independent room lifecycles;
- predictable restart/recovery;
- no cloud dependency required for current baseline;
- local assets and event streaming;
- deployable to lab/classroom machines with documented launch procedure.

## 15. Website / public visitor

The website must introduce, orient and route into Phantom Q. It must not become a duplicate fake simulation that diverges from Unity truth. Media and progress claims must match actual implemented capabilities.

## 16. Video / investor/demo viewer

Video should use real gameplay/hardware evidence where possible. Do not present pre-rendered concepts as if they are already functioning systems.

## 17. Accessibility reviewer

Check:
- readable type and contrast;
- state is not communicated by colour alone;
- reduced-motion path;
- no unnecessary camera shake;
- input abstraction/rebinding path;
- captions/narration options;
- stronger navigation-assistance mode;
- interaction targets are forgiving rather than pixel-perfect.

## 18. Performance/technical reviewer

### Build 02 target
- desktop 1080p/60 target;
- stable 45 acceptable during development if profiling explains why;
- web/mobile future target ≥30 FPS;
- profile CPU/GPU/memory/draw calls/materials/lights/shadows rather than blindly reducing detail.

### Rule
Optimise measured bottlenecks; do not strip visual quality pre-emptively simply because the HQ is 3D.

## 19. Security/authority reviewer

Check every sensitive action:
- identity established?
- capability earned?
- correct zone permission?
- active mission grant?
- target/service/action authority where required?
- evidence preserved before remediation?
- financial recovery authority separate?

## 20. Learning-design reviewer

For each mission interaction ask:
1. What must the learner understand?
2. What can they predict?
3. What can they physically configure/manipulate?
4. What observable consequence follows?
5. What evidence can they inspect?
6. What decision must they make?
7. Can they explain the security outcome without parroting text?

## 21. Environment-art reviewer

For every room ask:
- can the department be recognised without a giant floating label?
- is there a hero landmark?
- does it use the full vertical composition of the room?
- are commodity assets visually unified by Phantom Q material/lighting language?
- are clutter and prop density purposeful?
- are circulation and interaction pockets clear?
- do cutaway walls remain readable from the raised camera?

## 22. Future-mode reviewer

The HQ must not block:
- Guided Learning;
- Challenge Missions;
- Sandbox/Practice;
- Multiplayer Rooms;
- Classroom Host;
- role rotation after review;
- competition formats;
- persistent skill/clearance progression;
- future acts/advanced zones.

## 23. Build 02 full-scope gate

Build 02 passes this review when the HQ foundation can plausibly host every perspective above without requiring a new unrelated architecture. Future features may be inactive, but their spatial/data/interaction needs must be respected.

