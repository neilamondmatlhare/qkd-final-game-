# Codex Runbook — Build 02 Production Pass II

Use this when loading the package on the Windows/Unity workstation. The purpose is to **execute and prove the same Build 02**, not to redesign it.

## 1. Safe load

- Extract to a new folder, e.g. `PhantomQ_Unity6_Build02_ProductionPassII_20260825`.
- Do not overwrite Build 01 or the previous Production Pass.
- Confirm Unity `6000.5.9f1` and the pinned package lock before changing anything.

## 2. Pre-Unity checks

From project root:

```powershell
python .\Tools\validate_spec.py
python .\Tools\validate_build02_static.py
python .\Tools\validate_build02_production_ii_static.py
```

All three must pass.

## 3. Execute the pass

Recommended:

```powershell
.\Tools\Unity.ps1 ProductionPassII
```

This may attempt the official Kenney CC0 intake. A failed asset download is not a Build 02 failure; the authored Production Layer II is deterministic and must still generate.

Expected Unity evidence:

- no compiler errors;
- rendering recovery reports valid URP shaders;
- `02_HQ_PLAYABLE_FOUNDATION.unity` regenerated;
- `BUILD02_PRODUCTION_LAYER_II` exists;
- base Build 02 validator PASS;
- Production II validator PASS;
- batch return code `0`.

If compilation fails, fix the exact compiler/API issue in Build 02 and rerun. Do not remove the Production II architecture simply to make the validator pass.

## 4. Generate visual evidence

```powershell
.\Tools\Unity.ps1 CaptureEvidence
```

Expected output:

`Docs/VisualEvidence/Build02_ProductionII/`

with 12 PNGs:
- exterior;
- Reception;
- Central Ops;
- Foundations;
- Crypto;
- Communications;
- SOC;
- Red Team;
- Engineering;
- Quantum;
- Advanced Compute;
- Secure Core.

Review those as a single set. The rule is **whole HQ first**, not “one impressive room”.

## 5. Human Play Mode acceptance

Open the same generated scene and walk:

`Exterior → Reception → Central Ops → Foundations → Crypto → Communications → SOC → Red Team → Engineering → Quantum → Advanced Compute → Secure Core threshold`

Record:
- whether any magenta remains;
- camera/cutaway problems;
- door/access problems;
- collision/circulation problems;
- unreadable room identity;
- interaction/HUD problems;
- FPS/frame-time/performance observations.

## 6. Asset curation — do not auto-fill blindly

If Kenney assets imported successfully:

```powershell
.\Tools\Unity.ps1 CatalogAssets
```

Then inspect `Docs/ASSET_INTAKE_CATALOG.csv` and populate **exact paths only** in:

`Assets/PhantomQ/Production/AssetManifest/PRODUCTION_ASSET_MAP.json`

Do not reintroduce keyword-first auto-replacement. Hero-lock systems remain custom.

## 7. Loop

Any real issue loops back into Build 02:

`observe → diagnose → research mature solution → improve → rerun validators → recapture whole HQ → replay full route`

Do not start Build 03 until the Build 02 gate in the Master Build Contract and Full-Scope Role-Play Acceptance is satisfied.
