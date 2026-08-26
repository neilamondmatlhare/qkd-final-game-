# Codex Runbook — Production IV Visual Compiler

## Goal

Do not redesign the canonical HQ. Translate the approved visual references and `ROOM_PRODUCTION_RECIPES_2026-08-25.json` into reusable Unity prefabs/variants and room compositions at scale.

## Implementation priority

1. Keep Build 01/A1–A10 geometry and stable IDs intact.
2. Convert repeated architecture into reusable base prefabs + variants instead of more procedural `CreateBox` calls.
3. Promote approved commodity assets into exact prefab mappings.
4. Preserve/custom-build hero systems.
5. Build Unity AI Navigation from the dressed geometry; repair obstacles/links rather than writing a custom pathfinder.
6. Integrate Cinemachine for production damping/framing while PQ state remains the authority deciding camera mode.
7. Keep cutaway tags on upper architecture and high services.
8. Populate the room recipes across all 11 rooms in one pass.
9. Capture the investor evidence manifest from the actual scene.
10. Do not reduce the large room scope to fix ordinary compile/import errors; repair the implementation.

## Lesson plug-in contract

Use `LESSON_MODULE_CONTRACT_2026-08-25.json` as the data boundary. Future lessons attach to persistent zone/anchor/service IDs. They must not clone the HQ, duplicate protocol truth or expose hidden role state.
