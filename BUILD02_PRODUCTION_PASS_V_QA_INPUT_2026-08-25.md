# Build 02 Production Pass V — Load and QA Report

Date: 2026-08-25  
Status: **technical compile PASS; visual production gate NOT PASSED**

## What was loaded

- Source archive: `C:\Users\ooknm\Downloads\PhantomQ_Unity6_Build02_ProductionPassV_WholeHQ_VisualCompile_CodexReady_20260825.zip`
- Source SHA-256: `AB0B13A5B7701F214E977364F9AC40B681B22CE94D2BBE824681FEFCFCB4FC25`
- Extracted project: `PhantomQ_Unity6_Build02_ProductionPassV_WholeHQ_20260825_152655`
- Unity used: `6000.5.9f1` (`C:\Program Files\Unity\Hub\Editor\6000.5.9f1\Editor\Unity.exe`)
- Archive safety inspection: 6,966 entries; one project root; no unsafe archive paths.

## Technical validation passed

- `python .\Tools\validate_spec.py` — PASS (11 rooms, 14 transitions, 26 adjacency edges, A1–A10).
- `python .\Tools\validate_build02_static.py` — PASS.
- `python .\Tools\validate_build02_production_v_static.py` — PASS.
- All 3,425 Unity asset `.meta` files were structurally valid.
- A clean second Unity batch run of `ProductionPassV` exited with return code 0.
- Unity reported the base Build 02 validation PASS and Production V validation PASS.
- Generated count reported by Unity: 52 reusable prefabs, 850 static production renderers, one NavMesh surface.

The first run rebuilt Unity's local Library cache and showed transient PackageCache import messages. The clean repeat completed without those first-import failures; the clean batch log is the authoritative technical run.

## Visual QA result — failed, do not promote yet

Production V generated all 18 deterministic 1920×1080 views in `Docs/VisualEvidence/Build02_ProductionV/`. They prove that the canonical scene, rooms and room props are present, but they do **not** meet the approved production vision.

Observed across the overview, arrival, reception, Central Operations, WS04, Foundations, Cryptography, SOC, Engineering, Quantum, Advanced Compute and Secure Core views:

- lighting pools are severely clipped/overexposed while the rest of each room is nearly black;
- the exterior/reception does not read as a believable arrival sequence;
- the camera is a high, blockout-style survey rather than an investor/player-quality architectural composition;
- the spaces still visually read as primitive layout and prop markers, not the dense, material-rich, human/equipment-led HQ in the approved reference;
- this is a visual quality failure, not a shader-magenta failure.

The visual capture log also contains a URP global-settings editor error about a Probe Volume `.urtshader`. Capture still completed and Unity exited with return code 0, but it should be resolved or shown benign before a production visual sign-off.

**Decision:** retain this as a reproducible technical/QA handoff only. Do not label it investor-ready, use it as final evidence, start Build 03, or treat the whole-HQ visual gate as complete.

## Memory preserved

The incoming Build V project already contains its current project memory and the Production V reference deck. To prevent loss of prior approved direction, the following existing memory files were added without replacing Build V's own documents:

- `Docs/PHANTOM_Q_CAMPAIGN_VISION_MEMORY_2026-08-25.md`
- `Docs/BUILD02_PRODUCTION_VISUAL_TARGET_2026-08-25.md`
- `Docs/ReferenceImages/BUILD02_PRODUCTION_VISION_2026-08-25.png`

## Required next production pass

1. Correct the lighting/exposure and capture pipeline against the approved visual target; verify the result in rendered captures and a visible Unity/Play Mode walkthrough.
2. Replace the survey/blockout presentation with room-specific architectural composition, real materials, fixtures, operational equipment and characters appropriate to the approved visual language.
3. Resolve or explain the URP Probe Volume global-settings error.
4. Re-run the static validators, clean Unity production pass, evidence capture, whole-HQ walkthrough, access/interactions and performance checks.
5. Promote only after the visual evidence is comparable to the approved target and the Build 02 full-HQ acceptance gate is explicitly passed.

## Logs and evidence

- Clean compiler log: `Logs/production-pass-v-build02-rerun.log`
- Evidence capture log: `Logs/visual-evidence-v-build02.log`
- Rendered evidence: `Docs/VisualEvidence/Build02_ProductionV/`

