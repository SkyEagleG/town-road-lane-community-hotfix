# Release 2.5.0.2 — evidence and limits

Prepared 2026-11-16 for Windows Cities: Skylines II 1.6.4f1. This file supersedes the pending-gameplay status in the preserved candidate reports. Publication status is tracked separately in the release receipt; this document does not itself prove an upload succeeded.

## Exact tested artifact

- Implementation/source candidate: `1544e22f1cb03a8eed72c487376f052e3d622dcd`, based on the prior genuine 2.5.0.1 hotfix and the recorded upstream snapshot.
- Assembly: TownRoadLane, version 2.5.0.2.
- Managed DLL SHA256: `2E620C27263642DA99981209FD493B98D9DADEEED9F2F4D02D0943679CBFC0A9`.
- Target Game.dll SHA256: `F076DF4B70AA0F21A80345E03A052CA2273BC6754F41DAB7E63D837837A43745`.
- Target Unity.Entities.dll SHA256: `7E6D9ED7DF5295652FCCDB609D3D092CABB5A3FDB91336702D77381A1D42ED86`.

Release preparation changes documentation and listing metadata only. The compiled DLL, native libraries and frontend being uploaded are the tested candidate bytes, not a fresh rebuild after testing. Its startup banner and compatibility-success reason retain historical test-candidate/pending-validation wording from build time. Those strings are not a report of the later test result. No C# behavior or save format was changed after the reported test.

## Automated and source checks

31 focused tests passed, including five new area-warning lifecycle and rapid-input cases. Frontend type checking/bundling and the official Release/IL/Burst build passed. Nine serializable component identities, public field sequences/types, legacy aliases and writer versions match the cached published 2.5.0.1 assembly. Seven relevant installed-game types matched the preserved baseline's complete decompiled text. These checks are scoped as explained in COMPATIBILITY_1.6.4_REVIEW.md and INDEPENDENT_AUDIT_RECONCILIATION.md.

## Gameplay statement and log evidence

The maintainer states that the revised installed candidate worked during testing, including saving and restarting. This is user-reported gameplay coverage; the assistant did not perform or independently observe the in-game operations. Individual save names, camera positions, settings combinations and an exhaustive per-step result sheet were not supplied.

The flushed current session's TownRoadLane log contains 23 lines, zero errors and one warning. It records version 2.5.0.2 from the local testing folder, registration of the replacement in Modification4B, resolved hotkeys, UI bindings, successful vanilla-generator takeover, edge/parking clone application and registration of the seven vanilla-surface clones. Modding.log confirms the matching native Burst library and UI module loaded.

One warning reports that custom ear clipping failed for a 10-node area and vanilla triangles were retained. It is not repeated in that log. The precise triggering shape and visual impact were not established by the log; the maintainer reports no functional problem. This is a known triangulation-fallback limitation, not a claimed fix or proof that every polygon renders correctly. The current Player.log records normal game termination and no matching hotfix exception/system-update error. Other missing-prefab and engine warnings exist; this is not a claim that the whole game log is warning-free.

Player-prev.log belongs to the earlier inactive-build session and contains the old gate refusal, missing custom-prefab and unhandled-binding warnings. Those are not attributed to the successful current session. Available log rotation independently demonstrates one successful candidate boot, not two separately logged candidate boots; full-restart success is maintainer-reported.

Observed required pack versions in the active test playset: G87 Road Markings 1.4 (97828), Stripes and Chevrons 1.1 (98624), Vanilla Curb 1.1 (99062). Supporting enabled mods included ExtraAssetsImporter 1.7.6, G87 Vanilla Asphalt 1.5.0, ExtraLib 1.4.13, ExtraDetailingTools 1.2.5.2, Anarchy 1.8.0, Better Bulldozer 1.3.19, Unified Icon Library 1.0.15 and Write Everywhere 2.0.0.15. This does not establish every possible combination or dependency revision.

## Release decision

The verified activation, retained binary/API protections, automated results and maintainer-reported gameplay support releasing this bounded 1.6.4f1 update with the above limitation disclosed. No universal older-save migration, theme/traffic-handedness coverage, broad mod compatibility, measured performance improvement, future-patch compatibility or general crash fix is claimed. Unreviewed game/ECS fingerprints continue to leave vanilla enabled and the hotfix inactive. Keep the original mod and duplicate local test copies disabled when using the published replacement.

The Paradox description retains original author mxerf, asset credits, GPL-3.0, AI-development disclosure, GitHub/source links, requirements and the update log as its last section. Raw game logs, account/cache information, authentication helpers and proprietary reference/decompiled game files are not part of the public source archive.
