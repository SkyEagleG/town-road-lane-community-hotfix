# Town Road Lane — Community Hotfix

Unofficial maintenance of **Town Road Lane — Road Markings by mxerf**, maintained by **SkyEagle** (GitHub: SkyEagleG). This is not an official mxerf update.

**2.5.0.2 for Windows Cities: Skylines II 1.6.4f1 is prepared; the Paradox upload is pending the publisher account switch.** The existing [Paradox Mods listing](https://mods.paradoxplaza.com/mods/163405/Windows) belongs to **Sky Eagle**. Enable one replacement only: do not load the original, published hotfix and local test copy together.

## Source downloads

- [Complete current source ZIP](https://github.com/SkyEagleG/town-road-lane-community-hotfix/raw/refs/heads/main/Community-Hotfix-Source.zip).
- [Version-specific 2.5.0.2 source](TownRoadLane-2.5.0.2-Source.zip).
- [Preserved 2.5.0.1 source](TownRoadLane-2.5.0.1-Source.zip), for the earlier 1.6.2f1 release.

The current archive includes the complete corresponding source, frontend lockfile, build/configuration files, GPL license, source manifest, audits, 31-test regression suite and release validation notes. It is source code, not an installer. Build with the official CS2 modding toolchain and the documented frontend dependencies. Game assemblies and proprietary reference/decompiled files are not included. Four duplicate full-resolution promotional PNGs are omitted from this web distribution; their JPEG publication previews, all code, build files and runtime assets are retained.

The 2.5.0.2 release source snapshot is `cf48ed095c4a7e7ad404df0bdad96493d99af7ae` in the local reviewed source history, with implementation revision `1544e22f1cb03a8eed72c487376f052e3d622dcd`. Its source archive SHA256 is `EB09374E76D4B2BAEC3BF271A09CE23DEB47700D7D2585BE78733F4B8E429D02`. `RELEASE_SOURCE_MANIFEST.json` identifies every source file by hash. Those local source revision IDs are provenance records, not claims that the expanded source commits exist in this repository's Git history. Upstream baseline: `6ffd1e874ab70e60834e76ad15cae08508d991a8` (2.5.0).

## Compatibility and validation

Read [RELEASE_2.5.0.2.md](RELEASE_2.5.0.2.md) for exact tested hashes, evidence and limits. The exact reviewed Game/ECS fingerprints remain mandatory; future builds require review. Required asset packs are 97828, 98624 and 99062 plus their dependencies.

Official Release/IL/Burst processing, frontend checks, 31 focused tests and nine saved-component identity/layout comparisons passed. The maintainer reports successful gameplay checks, including saving and restarting. The reviewed current session confirms 2.5.0.2 startup, UI bindings, prefab clones and vanilla-generator takeover. Its hotfix log has zero errors and one non-repeating warning: custom triangulation failed for a 10-node area and vanilla triangles were retained. The game exited normally. No general crash fix, every-polygon guarantee, universal older-save migration, broad mod compatibility or measured performance gain is claimed.

The exact tested managed DLL SHA256 is `2E620C27263642DA99981209FD493B98D9DADEEED9F2F4D02D0943679CBFC0A9`. Release preparation changes documentation and listing metadata only; tested executable/UI bytes are retained. Historical candidate banners/reports saying validation was pending describe build-time status; the release notes record the subsequent evidence. Raw personal game logs are not published.

## Credits and transparency

Original author: **mxerf**. Asset packs: **elGendo87 / G87**. Original notices and **GPL-3.0** license are retained; see LICENSE and the complete source archive for additional credits.

SkyEagle directed goals, reviewed presented results and performed the reported gameplay checks. OpenAI Codex and AI tools were used extensively for analysis, implementation, documentation and automated verification. No independent human code review or security certification is claimed. The separately supplied audit was reconciled with genuine source and current installed game types; its suggestions were not blindly merged.

This is interim community maintenance. A working upstream update will prompt reassessment. We intend to honor an original-author request to withdraw the listing and explain the transition; save transfer still requires testing. This policy does not change the GPL license.

Use Issues for reproducible reports, including the game/mod version, triggering steps and relevant warning/error text. Avoid posting private account details, tokens or unreviewed complete game logs.

## Update log

**2.5.0.2 — 2026-11-16**

- Reviewed and pinned the installed 1.6.4f1 Game/ECS pair; retained unknown-build refusal.
- Added revision-sensitive area diagnostics with rapid-edit throttling and state cleanup, without changing geometry, retry behavior or saved layouts.
- Reconciled the separate audit; retained verified scheduler/component-dependency handling.
- Passed 31 focused tests, frontend and official build checks; documented maintainer gameplay/save/restart results and the single triangulation fallback.
- Updated the corresponding public source and Paradox description draft; publication status is stated above.
