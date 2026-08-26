# Phantom Q Build 02 Production Pass VI - Codex QA Handoff Package

Purpose: this package is a ready-to-open Unity source project for Build 02 Production Pass VI. It preserves the whole-HQ Production VI environment compile, generated playable foundation scene, documentation, project settings, package lock, Unity metadata, evidence, durable project memory and helper tooling so the next chat or agent does not need to repeat the loading work.

**Quality status:** the source is technically reproducible and materially improved over Production V, but its final visual production gate is **not passed**. See `Docs\BUILD02_PRODUCTION_PASS_VI_LOAD_REPORT_2026-08-25.md` before treating it as an investor, final-art or Build 03 handoff.

## Open Target

- Unity Editor: `6000.5.9f1`
- Unity executable used: `C:\Program Files\Unity\Hub\Editor\6000.5.9f1\Editor\Unity.exe`
- Project folder after extraction: `PhantomQ_Unity6_Build02_ProductionPassVI_HighGradeEnvironment_*`
- Recommended open helper: `Tools\Unity.ps1`

Example from PowerShell:

```powershell
cd "C:\path\to\PhantomQ_Unity6_Build02_ProductionPassVI_HighGradeEnvironment_20260825"
.\Tools\Unity.ps1 Open
```

To rerun the Build 02 Production Pass VI in batch mode:

```powershell
.\Tools\Unity.ps1 ProductionPassVI
```

## Included Fixes

- Unity version locked to `6000.5.9f1`.
- Package versions locked in `Packages\manifest.json` and `Packages\packages-lock.json`.
- Build 02 overlay flattened into the real Unity project folder.
- `PQAccessReaderVisual.cs` fixed so `MaterialPropertyBlock` is created lazily instead of inside a `MonoBehaviour` field initializer.
- Empty Unity folder metadata files under `Assets\PhantomQ` repaired with valid GUIDs.
- Generated scenes included:
  - `Assets\PhantomQ\Scenes\01_HQ_MASTER_GREYBOX.unity`
  - `Assets\PhantomQ\Scenes\02_HQ_PLAYABLE_FOUNDATION.unity`
- Build 02 documentation and project vision included under `Docs`.
- Production VI architectural material palette, reusable architecture kit, whole-HQ room skin, authored environment composition, revised lighting and Navigation mesh.
- Durable current project memory at `Docs\PHANTOM_Q_CURRENT_PROJECT_MEMORY.md`, campaign memory at `Docs\PHANTOM_Q_CAMPAIGN_VISION_MEMORY_2026-08-25.md`, and source guardrails under `Docs\ProjectMemory_2026-08-25`.
- Production VI target/deck reference images and deterministic rendered evidence under `Docs\VisualEvidence\Build02_ProductionVI`.

## Validation

The project passed:

- `python .\Tools\validate_spec.py`
- `python .\Tools\validate_build02_static.py`
- Unity 6000.5.9f1 Production Pass VI clean generation produced base, Production V and Production VI PASS lines for active URP, the A1-A10 HQ, camera/cutaway, access, representative interactions, architectural skin, lighting and Navigation.
- The exact load and visual QA record is in `Docs\BUILD02_PRODUCTION_PASS_VI_LOAD_REPORT_2026-08-25.md`.
- Visual evidence is review support and this pass remains below the supplied high-grade production target. Play Mode, profiler, visual remediation and final exposure sign-off remain required before promotion.

## Excluded From Zip

The zip intentionally excludes Unity-local/generated cache folders such as:

- `Library`
- `Temp`
- `Logs`
- `UserSettings`

Unity may re-import the project the first time it is opened after extraction, but no source patching should be needed.
