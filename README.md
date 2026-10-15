# Town Road Lane — Community Hotfix

Unofficial maintenance of **Town Road Lane — Road Markings by mxerf**, maintained by **SkyEagle** (GitHub: SkyEagleG). This is not an official update by mxerf.

**Candidate 2.5.0.1: release preparation and compatibility investigation in progress. No Paradox release has been published.**

## Source

Download **Community-Hotfix-Source.zip** in this repository for the complete candidate source tree, original license, build instructions, repair report (HOTFIX.md), tests, and test procedure. It corresponds to candidate source commit `7df4c79584940a649a1dfbf47dcc925c40cab87c`, based on upstream `6ffd1e874ab70e60834e76ad15cae08508d991a8` (2.5.0). The archive is source, not an installer. Its embedded test-status documents describe the build-time snapshot; the newer status below takes precedence for gameplay progress. Build with the official CS2 modding toolchain and the UI lockfile dependencies as documented inside. Game/toolchain reference assemblies are not redistributed.

Original repository: https://github.com/mxerf/town-road-lane

## Purpose and changes

Repair specific reliability weaknesses: bounded diagnostics/retries, logger-failure containment, explicit game-system ordering, guarded initialization/takeover, callback lifetime, queued settings writes, strict save-layout validation, legacy migration buffer lifetime, and area bookkeeping. The large copied lane-generator core was left unchanged. Skyve's broken classification prompted review; it does not prove the original caused a particular crash.

The inherited mod provides visual manual line/area tools and automatic road-edge/parking markings. Markings do not change vehicle lane choices. Enable this replacement instead of the original, never both. Windows baseline: Cities: Skylines II 1.6.2f1 with reviewed game/ECS fingerprints. Unknown binaries leave the hotfix inactive. Required G87 packs: 97828, 98624, 99062 and their dependencies. Future updates still require review.

## Current validation

Official Release/IL/Burst processing, 26 focused tests, frontend checks, and nine saved-component metadata comparisons passed. The maintainer reports marking/line/area tools, road operations, menu save/reload, and fresh-process restart/reload working. Existing older-city markings were present on load with the replacement. This is limited observed coverage, not universal save compatibility or measured performance certification.

A localized fading observation did not repeat in the larger city; its cause remains unresolved. Repeated RoadConstructionSystem errors in a large modded configuration are being investigated: the installed Road Construction Events mod defines a matching system, but the wrapped stack does not establish the root cause or exclude interaction. A separate VehicleController missing-property-pack error is also recorded. The first short hotfix session had no warnings/errors in its own log; later booting produced one late-clone warning followed by successful clone registration. We do not claim the whole game is error-free. Private game logs are not published here.

## Credits and transparency

Original author: **mxerf**. Asset packs: **elGendo87 / G87**. Original license and notices are retained: **GPL-3.0**; see LICENSE and the source archive for existing notices and additional credits.

SkyEagle directed goals, reviewed presented results, and performed the reported gameplay checks. OpenAI Codex and AI tools were used extensively for analysis, implementation, documentation, and automated verification. No independent human code review or security certification is claimed.

This is an interim community maintenance effort. A working upstream update will prompt reassessment. We intend to honor an original-author request to withdraw the listing and explain the transition; save transfer still requires testing. This policy does not change the GPL license.

Use this repository's Issues for reproducible hotfix reports. Do not post private account details, tokens, or unreviewed complete game logs. Binary release and final support scope remain pending.
