# ModPilot — GTA IV and GTA V Legacy


## Cyberpunk Trainer 1.13.1-beta

Independent F7 menu: player, weapons, vehicles/inspection, items, teleport, world, police, progression and settings. Spawning and weather require Codeware. Temporary modes reset with the session; granted items, money and progression remain in the game save. Favourites, vehicle history, named locations and settings use the mod-local CET database, preserved when updating managed scripts.

Inspection: arrows orbit/zoom, Enter hides the overlay, Backspace exits. Camera height and auto orbit are in Settings. Assign repair/boost/brake and navigation hotkeys in CET > Bindings > ModPilotTrainer. Open the menu on foot; vehicle actions also have hotkeys.

New native actions need in-game validation on the installed patch. Lua/file-transaction checks do not replace gameplay. A marker without elevation needs loaded collision geometry; missing ground causes a refusal. Vehicles spawn ahead of the player: use an open area. Keep the trainer CET database to retain preferences.

## Cyberpunk: Night City desktop workspace

The Cyberpunk workspace now shares the trainer's visual direction: yellow/black surfaces, cyan labels, clipped cards and dedicated navigation. Home shows the selected copy, a contextual next step, installed/enabled mod counts and component-file presence. File presence does not certify patch compatibility.

Components, trainer setup, mod management, setups and recovery use the same scoped theme. Navigation becomes more compact in smaller windows. Change-plan review, operation cancellation and game-specific state remain in place.


## Cyberpunk: Night City theme

The independent trainer uses the selected yellow/black design: branded header, clipped corners, search, six vehicles per page and a summon card. F7 (or the chosen key) opens the menu; arrows select, Enter acts and Backspace returns. On the vehicle category's first row, Left/Right switches All / Modded / Favorites. Right on a vehicle toggles its star; favorites last until game restart.

The Modded tab uses explicit `Vehicle.ID` declarations from enabled managed YAML mods at trainer update time. Unknown/external records stay under All. Update the trainer after adding mods to regenerate these tags. A catalogue record does not certify that all mod dependencies loaded successfully.

Optional photos can be placed at `bin/x64/plugins/cyber_engine_tweaks/mods/ModPilotTrainer/previews/Vehicle.ID.png`, using the exact record ID. PNG limits: 1024×1024, 8 MiB; up to 16 photos cached per run. Missing photos show a labeled schematic rather than an invented model image. These user images are not managed trainer payloads. Actual gameplay appearance and controls still need verification; mocked Lua checks do not replace an in-game run.



[Русский](README.md) · **English**

> Version **1.13.1-beta**. Cyberpunk 2077: ModPilot finds which mods other mods need (Nexus requirements, script libraries, shared resources) and installs them in one click; 50-mod catalog; interface in 10 languages.

Fix official ArchiveXL/TweakXL installation: embedded Scripts, Bundle, Data and TOML hints retain their author-provided paths.

## Independent trainer menu — 1.13.1-beta

Cyberpunk → Trainer → Install / update now installs a standalone in-game menu toggled by F7. The CET console need not be open during use; CET remains its renderer/script runtime. Arrows select rows/pages, Enter activates and Backspace returns. Existing actions and vehicles remain available; search/Vehicle.ID use an arrow-driven on-screen keyboard.

Use the menu on foot; vehicle entry, a session change or the CET console closes it. It does not impose a global modal game-input lock. Reviewed automatic setup modifies only ModPilotTrainer in bindings.json, preserves other sections and retains an original backup. Old conflicting ModPilot shortcuts are cleared; another mod's conflict stops automatic setup. Choose F6/F9/Insert or disable automatic setup and assign keys once in CET Bindings.


## Cyberpunk trainer vehicles — 1.7.0-beta

In the CET overlay, expand Vehicles and mod vehicles and refresh after loading a save. The catalogue reads live TweakDB Vehicle records, including successfully loaded mods. Includes name/ID search, pagination, car/bike type selection and manual Vehicle IDs. Replacement mods use the original vehicle record. It does not attribute records to individual archives or infer vehicles from archive filenames.

Summoning uses the native vehicle system: a vehicle may appear near a road and the active vehicle may change. The same ID does not create unlimited duplicates. Normal/instant summon mode has a separate toggle. The entire garage is not automatically unlocked; only the selected record is added to the summon list if needed. Actual gameplay remains unverified; use a separate save for testing.


## Cyberpunk 2077 trainer in 1.6.0-beta

My games → Cyberpunk 2077 → Trainer installs ModPilot's own CET Lua mod: health restoration, money, time of day, a remembered location and teleport return. RU/EN menu. Requires Cyber Engine Tweaks; the trainer itself does not require RED4ext/Codeware.

Close the game before installation. Load a save and open the CET overlay to see ModPilot Trainer. Assign the overlay key (e.g. F7), health and return shortcuts in CET → Bindings. Shared CET bindings are not overwritten.

Initial release: the game APIs still need actual gameplay validation. Make a separate save first. Money/time changes may persist; uninstalling does not undo gameplay changes. Teleport is on foot only; locations are held in memory until a session change. Vehicle summoning is added in 1.7.0; god mode and noclip are not included. The trainer updates as one managed mod and can be disabled/removed with original file restoration.


## Cyberpunk 2077 in 1.5.0-beta

Separate workspace per installation, Steam discovery and selection through `bin/x64/Cyberpunk2077.exe`. Supports legacy `.archive`/ArchiveXL files in `archive/pc/mod`, redscript in `r6/scripts`, TweakXL in `r6/tweaks`, CET and RED4ext, and reviewed import of the official CET, RED4ext and redscript ZIP packages. Download frameworks from their author pages; third-party DLLs are not bundled.

Disable/removal restores original files or their absence. Includes enabled-mod setups, known same-path conflicts, component preflight, cancellation, rollback and recovery. A framework required by another enabled managed mod cannot be disabled alone. Original game archives, the game executable and script cache are not writable targets. Setups do not snapshot configuration or saves independently. Priority applies to identical file paths, not resources across different archives.

REDmod deployment is not supported and its packages are rejected before installation. Internal archive content, every author's dependencies, game patch/API compatibility and actual gameplay remain unverified. Runtime-generated caches and saves are not rolled back by disabling mods.

Package layout follows [CET](https://wiki.redmodding.org/cyber-engine-tweaks/getting-started/installing), [RED4ext](https://docs.red4ext.com/getting-started/installing-red4ext) and [redscript](https://github.com/jac3km4/redscript). REDmod is a separate workflow described by [CD Projekt Red](https://www.cyberpunk.net/en/modding-support).


## New in 1.4.0-beta

- Updates are available directly in the game library. Downloads validate SHA256/length, support cancellation and remove incomplete files. The installer targets the running application directory.
- GTA V: OIV folder additions expand to existing update.rpf entries. Duplicate destinations, traversal and unsupported commands block the entire package. Nested RPF, deletion and arbitrary XML edits remain unsupported.
- Smaller work areas, wrapping mod actions and visible keyboard focus throughout the shared controls.
- RDR2: experimental separate workspace for native x64 ASI plugins, Script Hook RDR2 and related configuration/data. Reviewed installation, disable/removal, enabled-plugin setups, original backups and recovery share the file transaction engine. RDR2 setups do not snapshot configuration separately. LML, RPF and .NET scripts remain unsupported.
- Choose RDR2.exe, download the archive from the [Script Hook RDR2 author](https://www.dev-c.com/scripthookrdr2/), import it, then import an ASI mod. Third-party DLLs are not bundled. Game patch compatibility is not certified. Story mode only.


## GTA V Legacy

### New in 1.3

- My setups capture plugin selection/order, enabled cars and RPF mods, plugin configuration and trainer menu/user/handling settings. Limits: 2 MiB per configuration file, 32 MiB per setup. Mod binary versions, editor map files and game saves are not versioned by setups.
- Original disables every managed mod family. Previous state is saved before switching. Legacy setups are marked plugins only and leave cars/RPF unchanged. A combined switch uses one durable transaction and rejects stale previews.
- Package preflight checks supported formats/edition, detected dependencies and bitness, known conflicts and, when author metadata is available, Script Hook V game-build support. Unknown metadata and unconfirmed compatibility are stated explicitly; DLL presence does not prove that a mod works.
- Recovery shows affected files, external edits and damaged backups, with retry, journal folder and JSON export actions. There is no force overwrite or discard-journal action.
- Long operations show stage, file, bytes, speed and stage-space reservation. Copying, extraction and downloads can be cancelled; interrupted publication is rolled back. Recovery itself cannot be interrupted by cancelling again.


Separate state for each installation: plugins and scripts, components, add-on cars, replacement overlays, supported existing-file update.rpf/OIV replacements, catalog, plugin setups, crash diagnostics, save backups and a trainer. The interface has ten languages; trainers use Russian and English.

Add-on reinstalls and RPF toggles/removals use a durable recovery journal. Reopening recovers interrupted operations. Unexpected external edits block recovery and are preserved for review. Rollback leaves unused appended RPF data in place rather than truncating the archive.

Online without mods disables managed plugins and checks known loaders. Enabled add-ons/RPF mods, external loaders and scripts block preparation. This does not verify original game archive integrity or guarantee a safe Online session. Use a verified clean installation for Online.

Enhanced gameplay is not validated; Legacy add-ons are not automatically transferred to it. OIV support is limited to supported replacements of existing files in update.rpf, without nested archive edits or arbitrary XML modifications. [GTA V roadmap](GTA_V_ROADMAP.md).

## GTA IV features

A mod installer for **GTA IV: Complete Edition**. Drop a mod archive on the window — it works out what the mod is and where it goes, shows the car in 3D and installs it without touching the game's original files. Plus problem diagnostics, a built-in in-game trainer and one-click "back to vanilla".


## Features

**Installs any mod**
- zip / rar / 7z / folder / loose `.wft` `.wtd` files — just drag them in;
- cars: **replace** a stock car or **add a new one (add-on)** — a separate car with its own spawn name, driving in traffic;
- models, textures, skins, graphics (ENB, ReShade, DXVK), `.asi` / `.net.dll` scripts, trainers, map mods, data-only mods (e.g. handling);
- reads the readme: which car to replace, lines for `vehicles.ide` / `handling.dat`, what else the mod needs;
- fixes common author mistakes (e.g. invisible rims caused by a misnamed texture).

**Mod catalog and game clean-up**
- catalog: 44 checked mods for the Complete Edition + FusionFix; GitHub mods install in one click, for the rest ModPilot opens the author's page and picks the archive up from Downloads;
- "Take my game apart": finds everything installed by hand (mods in `update`, plugins, scripts, files changed with OpenIV) and adopts it or moves it to quarantine;
- OpenIV `.oiv` packages install without OpenIV — and can be undone;
- save copies before every game launch, restore in one click;
- graphics in one click: "Low-end PC / Balanced / Maximum" for FusionFix, with your old settings kept.

**Convenience**
- textured 3D preview: "before / after" right in the install wizard;
- mod list: on/off, priority order, conflicts;
- game cars: what is replaced, what is added; handling and colour tweaks;
- profiles and "share your setup" as a single `.ivmmpack` file;
- one-click components: FusionFix, Ultimate ASI Loader, ScriptHookDotNet and more.

**Diagnostics**
- finds why the game or a mod doesn't work: misplaced files, missing plugins, incompatible versions, limits, crashes (Windows event log) — and fixes what it can with one click;
- "Find the culprit": finds the crashing mod step by step.

**Built-in trainer** (F7 in game)
- spawn any car — stock or your add-ons by name, search, a garage of your own cars;
- any person from the game as a friend, an enemy or your character; bodyguards;
- god mode, weapons, teleport, weather, time, traffic, free flight, autopilot, drift counter, chaos mode;
- on-screen dashboard speedometer, customisable menu (colour, size, side).

## Requirements

- Windows 10 / 11 (64-bit);
- GTA IV: Complete Edition (**FusionFix** recommended — the app installs it for you);
- ScriptHookDotNet for the trainer (also one click).

No .NET install needed — it is built into `ModPilot.exe`.

## Getting started

1. Run the installer `ModPilot-…-setup.exe` (or unzip anywhere) and open ModPilot.
2. It finds the game (Steam, registry, drives) or asks for the folder.
3. Drag a mod archive onto the window → check what the wizard suggests → "Install".
4. Press "Play".

**Windows says "Unknown publisher"?** The app is not signed with a paid certificate. Click "More info" → "Run anyway".

## How it works (safety)

- The game's original archives and files are **not modified**: mods are built into separate archives in the `update` folder, loaded by FusionFix and Ultimate ASI Loader.
- Car data (`vehicles.ide`, `handling.dat`, `carcols.dat`, `cargrp.dat`, `gta.dat`) is the original plus the lines of every enabled mod, also in `update`.
- Anything replaced outside `update` is backed up and restored when the mod is removed.
- Mod copies, backups and state live in the game folder: `IVModManager\`. Don't delete it while mods are installed.
- Save games are only copied (before each launch); they are written back only when you press "Restore".

## Beta limitations

- **Known issue:** the trainer menu and speedometer may flicker with DXVK / FusionFix. This comes from ScriptHookDotNet drawing over the frame. A flicker-free fallback is "Settings → Drawing → game" in the trainer menu (Russian text is shown in Latin letters there).
- Without FusionFix the mode is experimental: TLAD/TBoGT mods, custom add-on names and extended limits don't work.
- Map mods and parts of the trainer are lightly tested in game.
- Encrypted `.img` files inside mods are loaded as a whole, without looking inside.
- Cyrillic in add-on names may not show if the game font lacks it.

Found a bug? Attach `%AppData%\IVModManager\log.txt` and a screenshot.

## Building

.NET 8 SDK:

```bash
dotnet build IVModManager.sln
dotnet run --project tests/IVModManager.Tests          # IVMM_REALGAME=<game folder> adds checks on real data
powershell -File tools/release.ps1                      # release: self-contained exe + zip in dist/
```

The trainer is built separately (.NET Framework 4 for ScriptHookDotNet) and embedded as a resource:

```bash
GAME="<game folder with ScriptHookDotNet.asi>" sh tools/build-trainer.sh
```

## License

Free to use, **all rights reserved** (© 2026 BADURGOW, rpomidorow@gmail.com). Download it from the official page and use it; do not sell, re-upload, modify or pass it off as your own — see [LICENSE](LICENSE). Third-party components: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

Not affiliated with Rockstar Games or Take-Two Interactive. Grand Theft Auto is their trademark.


## New in 1.1.1-beta

- Installation preview: file targets, overlaps with enabled mods, missing dependencies and estimated free space. Archive paths are templates; generated data depends on vehicle choices and merging.
- Interrupted applies are journaled and resumed on reopening the game folder. Launch from ModPilot is blocked until recovery succeeds. Recovery resumes the selected setup; it is not a full installation rollback.
- Closing is blocked during work, and a second instance in the same user session is refused.
- Diagnostics show impact and suggested next steps.
- Settings → Support report: editable preview and local export. Nothing is uploaded. Known private paths are redacted; review before sharing.
- Fixes for build import, vanilla restoration and restoring old save backups. The previous setup is retained in a profile before switching to vanilla.

Do not manually change mods while an interrupted apply is being recovered. Recovery covers managed mod applies; external component installers follow their own behavior. Manual validation in GTA IV is still required for this beta.

## In development: exact preparation and rollback

Normal installs and adoption of manually installed mods are prepared in a private temporary game workspace. Preview lists real final paths, generated archive names, sizes and before/after fragments for small text files. Long fragments are explicitly truncated.

Confirmation commits those prepared bytes. Changes to game inputs, settings or existing mod payloads invalidate the preview. Failed writes roll back previous files and state; reopening a game with an interrupted commit completes rollback. Locked files or unexpected external edits retain snapshots and stop automatic rollback with an explanation. Use Reapply after resolving the cause.

Preparation requires temporary disk space as well as space for snapshots on the game drive. Operations through symbolic links/junctions are refused. External component installers and repairs already performed by other tools before applying are outside this transaction.

These changes are included in the local 1.1.2-beta test build. Previous 1.1.1-beta archives do not contain them. An integration pass on a separate GTA IV 1.2.0.59 copy has been performed; the complete manual gameplay matrix remains pending.

The same mechanism covers .ivmmpack imports: files, mods and the selected profile are prepared and confirmed together.


## In development: components, conflicts and profiles

Managed component archives use prepared transactions for install, upgrade and removal. Edited files are retained during removal. ASI Loader detection inspects x86 exports/product information rather than trusting a DLL name.

Conflicts explain the active resource and how to change priority, with separate episode/section rules. Profiles capture independent tuning/colors, trainer and extended-limit flags, plus known FusionFix/trainer and tracked component ini/cfg/toml settings. Optional settings absent at capture are removed on return. Limits are 1 MiB per file and 8 MiB total; saving reports an error instead of omitting oversized files. Older profiles remain readable. Component version differences are reported; profiles do not archive or reinstall component binaries.

These changes are included in the local 1.1.2-beta test build; this build has not been published. Current game support remains GTA IV; other games are not implemented yet.


## 1.2.0-alpha.1 — GTA V development

The development build opens a game library first. GTA IV retains its existing engine. GTA V Legacy and Enhanced each use a separate workspace per installation and a new file-only adapter. ASI/script package previews work without a game. With a selected game, supported packages can be installed, disabled and grouped into saved enabled-mod setups; original files and interrupted operations are recoverable.

This is an initial implementation, not full GTA V support. Vehicles, maps, RPF/OIV editing, save-game backup, a GTA V trainer, full component/version diagnosis and in-game execution are not implemented or verified. Setup profiles store enabled mod order, not independent snapshots of arbitrary runtime configuration files. Edited installed files block subsequent operations to avoid losing changes. RDR 2 is a disabled planned card. Existing 1.1.2-beta archives and their checksums are unchanged.
