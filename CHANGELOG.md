# Changelog

## 1.15.1-beta

- Soft motion: windows and pages fade in, Cyberpunk 2077 and RDR 2 tabs slide in a little, mod, car and catalog lists appear row by row. Nothing moves when "Show animations" is off in Windows.
- Bug reports to the author now go through a small relay instead of straight to Telegram: the bot's token is no longer inside the program, and each sender is limited (3 reports an hour, 10 a day). Reports sent from 1.15.0 don't reach the author — update to send them.
- The ModPilot logo in the Cyberpunk 2077 window and trainer is redrawn from a font by a script in the repository (tools/make-cyberpunk-wordmark.py).

## 1.15.0-beta

- GTA V: any script or plugin mod installs. What can't go into the game is left out, each file with the reason shown: programs, GTA IV files and plugins, 32-bit libraries, LSPDFR / RAGE Plugin Hook parts, loose RPF files (models, maps) outside a car or OIV package, root libraries such as ReShade. A .NET script zipped without the scripts folder goes there. A mod for another game (GTA IV, Cyberpunk 2077, RDR 2…) or a FiveM resource is named as such.
- GTA V: a missing Script Hook V, ASI Loader, Script Hook V .NET, LemonUI or NativeUI no longer stops the install. The review says what else to install and where, and so does the status line after installing.
- GTA V: the review starts with "What this mod is" — an ASI plugin, a .NET script, a menu library, a settings file, a plugin's data folder, an add-on or replacement car, an update.rpf mod — and that it is story mode only and reversible.
- GTA V: a car or update.rpf mod while the mods folder isn't ready no longer sends you to another page: ModPilot lists the steps (copy of update.rpf, game limits, Script Hook V, the RageOpenV loader), prepares the folder on request and then installs the mod. A texture (.ytd) without a model is no longer taken for a replacement car.
- GTA IV: an archive with nothing for GTA IV names the game it is for (GTA V, Cyberpunk 2077, RDR 2…) or says it is a FiveM resource.
- GTA IV and GTA V catalogs: top lists above the sections, ranked, each with a short explanation. GTA IV: Must-haves, Console look, Most interesting, Gameplay changers, Best visuals, Best for cars. GTA V: Must-haves, Gameplay changers, Most interesting, Best for cars. Built from the mods already in the catalogs; texts in all 10 interface languages.
- Bug reports go straight to the author's Telegram (one click, no account) when the build carries the bot settings (docs/bug-reports-telegram.md; the token file is git-ignored). A short caption plus the full report as a .txt; an optional "how to reach you" field; at most one report a minute and ten a day per PC; the token never reaches the log. GitHub and Copy stay as alternatives.
- "🐞 Report a bug" in every game window and in My games: describe the problem, pick what it is (bug, a mod that won't install, idea), see exactly what will be sent. ModPilot adds its version, Windows, the game and the end of its log with the user name, personal folders and e-mail addresses hidden, then opens a GitHub issue with the text filled in (the full text is also copied, for anyone without a GitHub account). After an unexpected error ModPilot offers to report it with the error attached. Nothing is sent without the user pressing Submit on GitHub.
- Cyberpunk 2077 catalog: top lists — Must-haves, Gameplay changers, Most interesting, Best visuals, Quality of life, Best for cars — ranked, each with a short explanation, above the sections. 42 more mods (92 in all), picked from the most endorsed on Nexus, kept up to date for game 2.x, no adult content; authors, requirements and dates checked against Nexus. A "Fixes" section appears.
- Cyberpunk 2077: any mod installs, the way a person would unpack it into the game folder (archive, bin/x64, engine, r6 — incl. r6/audioware and r6/storages —, red4ext, mods). Only what would break the game is left out, each file with the reason shown: programs (.exe, .bat, .ps1…), files the game makes itself (r6/cache, r6/logs), the base game's own archives, non-x64 or GTA libraries, damaged archives. A mod for another game (The Witcher 3, GTA, Skyrim/Fallout, RDR 2) is named as such.
- Cyberpunk 2077: a missing framework or base mod no longer stops the install. The review says what else to install and where (Components page, Nexus, the DLC section for REDmod), and so does the status line after installing. Switching off or removing something enabled mods rely on is still blocked. Add-ons to another plugin (AudioXL sound packs) name that plugin; r6/audioware packs name Audioware.
- Cyberpunk 2077: archives with installation options ("Option A / Option B", FOMOD folders) open a chooser — one option or several together. CET mods zipped without folders land in their own CET folder; ReShade/upscalers zipped without bin/x64 go there.
- Cyberpunk 2077: the review starts with "What this mod is" — in plain words what each part does (archives, ArchiveXL, TweakXL, redscript, CET, RED4ext plugins, sounds, keys, REDmod, ReShade, engine settings), where its settings are (Mod Settings, CET overlay), that it seems to add a car, and what frameworks themselves are. All of it in the 10 interface languages.
- The Cyberpunk trainer says plainly that it needs Cyber Engine Tweaks.
- Cyberpunk 2077: AudioXL is a known library (Nexus 33442); Mod Settings is also recognised by its ModSettingsModule module.

- Update a mod over itself (Cyberpunk 2077, GTA V, RDR 2): "Update…" next to an installed mod, or install a new version and ModPilot recognises it (same Nexus mod id in the file name, or most of the same files) and asks. The mod keeps its place in the list, on/off state and setups; files the new version no longer has go back to the originals, their stored copies are deleted.
- Cyberpunk 2077, Logs: the log doctor reads the last session's TweakXL, ArchiveXL, RED4ext, redscript and CET logs, names the mod whose file failed, says in plain words what it means and offers "Update mod", "Disable mod", "What mods need" and the log itself.
- Cyberpunk 2077, Home: "New in Downloads" — fresh mod archives for this game from the Downloads folder (recognised from the file list inside, nothing unpacked) that are not installed yet, with Install / Update and Hide. Archives and folders can also be dropped onto the window.
- Removing or updating a mod no longer leaves empty folders in ModPilot's mod store; reinstalling a component no longer keeps old file copies.
- Cyberpunk 2077, Recovery: save copies. Before each launch from ModPilot the saves (Saved Games\CD Projekt Red\Cyberpunk 2077) are copied, with the same list, restore and delete as GTA IV / V; the switch and "List of copies…" are on the Recovery page. Files unchanged since the previous copy are hard links to it, so dozens of copies of a large save folder take little extra space. The first copy runs in the background with a status line; a copy that fails is said in the status, the game still starts.
- Fixed: restoring saves from the GTA V window checked only whether GTA IV was running. Each game window now checks its own game.
- All new strings are translated into every interface language (uk, de, fr, es, pt, pl, tr, ar), including the Cyberpunk crash-hunt messages and the mod update summary. The string extractor no longer pairs text across statements (removed 11 non-texts such as JSON keys from the list).

## 1.14.0-beta

- Fixed (GTA IV): cars built from a donor (a replacement mod installed as a separate car) had no sound. GTA IV picks a car's sounds from pc/audio/config/game.dat by the game name in vehicles.ide, and the new car got a game name of its own. It now carries the donor's game name, so it sounds like the donor and shows its name in game. A replacement keeps the stock car's game name even when the mod's vehicles.ide line changes it. Cars installed earlier are corrected on the next Apply.
- GTA IV: "Sound" choice for added cars in the install wizard and the car window: the donor's sound (default), any stock car's sound, or no sound with the car's own in-game name. GTA IV ties a car's sounds to its in-game name, so a borrowed sound also shows that car's name.
- GTA IV: "Needed for your mods" on Home and at the top of the Catalog. ModPilot reads the Requirements of the installed mods from the public Nexus Mods API (domain gta4; mod ids from catalog entries or Nexus file names; only ids are sent, answers cached for a day). Components (FusionFix, ScriptHookDotNet, ASI Loader…) are recognised by name and installed as components; catalog mods from the catalog; other mods from their Nexus page with the download picked up. Optional requirements ("…but optional") are left out.
- GTA IV: vehicle limits. Home shows a "Vehicle limits" chip with the number of added cars; when FusionFix's ExtendedLimits is off a click switches it on. Diagnostics warns about 30+ added cars without FusionFix.
- GTA IV: Diagnostics reads ScriptHookDotNet.log and scripthook.log of the last launch and names the managed mod that installed the failing script.
- GTA IV catalog: updates for GitHub mods. ModPilot remembers the release tag it installed and offers newer releases ("Update" keeps the mod's place in the list and removes the old version); mods installed earlier are compared by release date.
- GTA IV: car mods that bring sounds for fastman92's vehicle audio loader are pointed out in the install wizard (ModPilot doesn't install the loader or copy its lines).

## 1.13.1-beta

- Fixed catalog directory traversal: validated mod identifiers, unique download directories, bounded cleanup and cancellation before filesystem changes.
- Catalog browser downloads must match the selected Nexus id (or a recognizable title on non-Nexus sites); unrelated archives are ignored. The selected filename is shown during review.
- Crash hunt verifies the original failure, the final candidate and the complementary set. Every selection and hunt journal transition shares one recoverable transaction; cancellation preserves the previous complete state and active setup.
- Archive order, original backup and ownership marker are committed together; save and reset require the selected game to be closed.
- Dependency notes no longer classify configuration options as optional; conditional requirements remain visible with the author notes.
- Cyberpunk filesystem analysis runs in a cancellable background task; navigation reuses the last completed snapshot. New results cannot overwrite another game workspace.
- Hand-installed mods are grouped by full name, not author prefix. A file-selection review allows separate adoption and naming.
- Restored the selected-vehicle inspection camera and height, distance and auto-orbit settings. Trainer diagnostics read the manager build version from configuration.
- Added regressions for cancellation, false crash blame, wrong downloads, unsafe paths, dependency wording and archive-order rollback. Native in-game validation of the camera and newer modes is still required.

## 1.13.0-beta

- Cyberpunk 2077 and RDR2 pages now speak all 10 interface languages, like GTA IV and GTA V (Ukrainian, German, French, Spanish, Portuguese, Polish, Turkish and Arabic added, 385 strings each, including the Cyberpunk catalog descriptions). The in-game trainer stays Russian / English. The Cyberpunk side menu is wider so long page names fit.
- Translation tables: entries that had been added straight to Resources/lang moved into tools/lang/<lang>.5.json, so tools/lang/build.py no longer drops them; extract-strings.py also reads catalog-cp2077.json.
- Cyberpunk: ModPilot knows what any Nexus mod requires. It reads the "Requirements" list of every installed mod from the public Nexus Mods API (only mod ids are sent; answers are cached for a day in %LOCALAPPDATA%\IVModManager\nexus-cyberpunk2077.json and work offline), follows the requirements of missing requirements, and leaves out the ones authors mark as optional.
- Cyberpunk: one "needed" list on Home and at the top of the Catalog merges these with the libraries and shared resources found in scripts and .xl files. Each row says which mods need it and installs it in one click: from the catalog, from Nexus (the files page opens and the download is picked up), or by switching a disabled mod back on.
- Cyberpunk: installing a mod (file or catalog) asks Nexus what it needs and lists the missing mods in the review window; afterwards ModPilot opens the catalog with them at the top.
- Cyberpunk catalog v2: Nexus ids for every entry and 18 libraries other mods need, among them SDH0's Vehicle Resources, SDH0's Vehicle Audio, AudioXL, Vehicle Core, Vehicle Turret Core, Vehicle manufacturer fix, XUtils, Virtual Atelier, Audioware and Native Interactions Framework.
- Cyberpunk: mods copied into the game folder by hand are detected (archive, redscript, TweakXL, CET, RED4ext, REDmod), grouped by name and can be taken under management without changing game files; ModPilot keeps a copy so they can be disabled, enabled and removed.
- Cyberpunk: Codeware is a listed component; installed component versions are shown, and "Check updates" reads the latest GitHub release tag (nothing is downloaded). The trainer warns when Codeware is missing.
- Cyberpunk: new Logs page with errors and warnings from CET, CET mods (including the trainer), RED4ext and its plugins, and redscript.
- Cyberpunk: "Launch game" button starts Cyberpunk2077.exe with --launcher-skip and -skipStartScreen (plus -modded when REDmod mods are installed).
- Cyberpunk: conflict check for two mods defining the same TweakDB record or replacing the same redscript method.
- Cyberpunk: new Catalog page with 32 checked mods (frameworks, gameplay, cars, UI, sound, graphics) and their requirements marked as found or missing. GitHub mods (CET, RED4ext, redscript, ArchiveXL, TweakXL, Codeware, Mod Settings, Input Loader, Let There Be Flight) download and install in one click; for Nexus mods the page opens and the archive is picked up from Downloads. Online list: catalog-cp2077.json in the repository.
- Cyberpunk: RED4ext plugins may carry their own scripts, archives, key maps and sound banks next to their DLL (Mod Settings, Input Loader, Let There Be Flight); author uninstall .bat files are skipped.
- Fixed (Cyberpunk): the trainer's "Mods" vehicle tab missed cars installed after the trainer and every car written in the older .tweak format. ModPilot now keeps ModPilotTrainer/modvehicles.txt current after every change, reading both YAML and .tweak records; the trainer rereads it on Refresh.
- Fixed (Cyberpunk): after the first game run with Input Loader, every install, switch and removal stopped with "File changed outside ModPilot: r6/cache/inputContexts.xml". Input Loader rebuilds r6/cache/inputContexts.xml and inputUserMappings.xml on every start; ModPilot now expects that, keeps the rebuilt files while Input Loader is on and removes them with it.
- Cyberpunk: missing shared resources. Resources an ArchiveXL .xl file patches must come from some archive; when none carries them (for example SDH0 cars without "SDH0's Vehicle Resources"), the Home page and the install review say so — otherwise the car has no appearance and the game freezes and crashes when it spawns.
- Cyberpunk: mod priority on the Mods page (↑↓). When two mods install the same file, the higher one is in the game; each mod shows what it overrides and what overrides it, and the conflict list names the file the game has now.
- Cyberpunk: fewer false conflicts — resources stored byte-for-byte the same in two archives, and TweakXL list operations (!append, !append-once, !prepend, !remove) from several mods, are no longer reported.
- Cyberpunk: missing script libraries. ModPilot reads every redscript file for imports of modules nobody declares and for known library classes (Vehicle Core, Vehicle Turret Core, Mod Settings, Codeware…), and reads the redscript log of the last run; the Home page names the library, the mods that need it and offers the catalog install or its Nexus page. The install review warns before a mod that needs a missing library is installed — such a mod makes redscript fail and switches off every script mod.
- Cyberpunk: archive load order on the Mods page — drag rows or use arrows, "Save order" writes archive/pc/mod/modlist.txt (the game loads listed archives in that order; the first one wins a shared resource). A list the player wrote is kept as a copy and comes back on reset; a ModPilot list is kept complete after every install and removal; archives missing from the list are pointed out.
- Cyberpunk: resource overlaps between .archive files are read from each archive's index and listed under Conflicts with the winner for the current order.
- Cyberpunk: crash hunt on the Logs page — switches the checked mods off and back on by halves while the player reports whether the game crashed; frameworks stay on, hand-installed mods are not touched, the culprit stays off at the end.
- Cyberpunk: the Home page points out a game patch (changed executable) and suggests checking component updates.
- Cyberpunk: REDmod packages (info.json) install into mods/<name>; requires the free REDmod DLC tool.
- Cyberpunk: trainer page texts list the current functions.
- Cyberpunk trainer, item spawner: category strip (weapons, clothing, cyberware, mods, consumables, collectibles, crafting, other), two-line rows with the game's localized name and a readable subtitle (kind, weapon class, rarity, iconic), a rarity bar, quest markers, an info card with the game's own item description, quantity 1/5/10/50/100 and a grant button. Same-named records are told apart (crafted, preset or ID). No pictures are used.
- The catalogue also indexes grenades and every player-named generic item (junk, collectibles, shards, crafting materials, weapon and clothing mods). Internal records without a display name stay hidden; untranslated names are cleaned of Preset/Craftable/Default.
- Vehicle spawner: two-line rows with maker, car/bike and version (player vehicle, police, corporate, gang, story, damaged, mod); player versions are listed first among equal names, remaining twins show their ID. The 3D inspection button and camera settings were removed from the menu.
- New trainer modes: no recoil, no spread, no weapon sway (multiplier modifiers on the equipped weapon that follow weapon swaps), no overheat, infinite grenades/health items, infinite RAM, Sandevistan/Berserk/optical camo charges, infinite oxygen, super jump, unlimited carry weight, invisibility to enemies, world slow motion, damage x100 and +500 of every crafting material. Mode names in messages are readable; on/off rows show a switch.
- More trainer functions: one-hit kill, always critical hit, unlimited cyberware capacity (Humanity +1000, implants stay when switched off), no fall damage (invulnerable only while dropping fast), fly/noclip driven by the game's own movement input, teleport to the tracked quest objective, removal of fast-travel locks, free respec of perks and attributes (missing attribute points are refunded), long breach timer, recharge delays cut to 1%, kill/stun/calm hostile NPCs within 40 m, upgrade the weapon in hand to maximum quality, unlock all crafting recipes, remove items, exact money amount, level and street cred entered as a number, and mode profiles (three presets plus a saved "my profile"). Undiscovered fast-travel terminals cannot be opened from CET and stay closed.
- Vehicle spawn keeps the request alive outside the streamed sector (alwaysSpawned) and logs timeouts to ModPilotTrainer.log.
- QA: `tools/qa/render_cyberpunk_trainer.py` paints the menu to PNG from recorded ImGui calls. In-game validation of the new modes is still required.

## 1.12.1-beta

- Remove the replicated player-cheat native call after a reported game crash while enabling infinite ammo on patch 2.5.
- Infinite reserve now uses bounded inventory top-ups. No-reload sends a typed ammo-count event only to an equipped firearm with a validated magazine. Both stop with the session.
- Regression fixture treats the former native call as forbidden. Live gameplay revalidation is required.

## 1.12.0-beta

- Cyberpunk trainer: player and weapon modes, vehicle repair/upright/mount/physics actions, item catalogue, weather/day clock, police and progression commands.
- Persistent favourites, spawn history, named teleport locations, camera and interface settings in CET mod-local SQLite.
- Camera height, auto orbit, zoom persistence and overlay hiding; marker teleport and session teleport history.
- Pixel-measured text wrapping, readable minimum font sizes, scrolling full selected labels/status messages and adaptive footer.
- Item indexing is incremental and cancellable. New native gameplay actions remain subject to in-game validation.

## 1.11.0-beta

- Cyberpunk trainer: larger high-contrast text, Cyrillic font setup with backup, resolved vehicle localization keys.
- Temporary vehicle spawning through Codeware with actual entity confirmation and timeout.
- Separate orbit inspection camera, zoom and cleanup on exit/session changes.
- In-game spawn/camera validation is still required.

## 1.10.2-beta

- Preserve the Lua sandbox frame when opening the Cyberpunk trainer: store the result of ImGui.Begin before returning from its protected callback.
- Apply the same non-tail-call rule to texture loading. The LuaJIT stack regression reproduces 1.10.1's native-context failure and passes with the corrected call.


## 1.10.1-beta

- Fix the independent Cyberpunk trainer window failing to open: call CET ImGui.Begin through a Lua closure so its sandbox environment is retained inside pcall.
- Apply the same caller-context rule to lifecycle registration. Includes a regression that rejects direct protected calls of native bindings.


## 1.10.0-beta

- Cyberpunk desktop workspace now uses the Night City yellow/black theme with clipped frames, scoped styles, branded sidebar and clear primary actions.
- Redesigned Home, Components, Trainer, Mods, Setups and Recovery. Added state-derived overview counters, contextual next action and compact navigation on smaller windows.
- Preserved installation review, cancellation, per-game state and file transaction backends. UI snapshots cover both languages, empty/selected copies, busy/error states and trainer key selection.


## 1.9.0-beta

- Cyberpunk Night City trainer theme: yellow/black clipped panel, branded header, vehicle tabs, search, details and summon action.
- Six vehicles per page, session favorites and optional local PNG previews. Only explicit enabled managed YAML vehicle declarations are tagged MOD; unknown records remain under All.
- The logo is installed and removed with the trainer transaction. CET bindings and other mods are preserved.

## 1.8.0-beta — independent keyboard trainer menu

- Replace the CET-console panel with a standalone right-side in-game menu, dedicated toggle and keyboard categories/navigation. Preserve vehicle/actions and add on-screen text entry.
- Draw without console or mouse capture; close on session/vehicle/console changes and bound held-key repeat.
- Add reviewed transactional default-key merge, conflicts, original backups and rollback with trainer files; shared bindings are not claimed as mod payload.
- Preserve other mods/CET overlay bindings and permit alternate toggle keys/manual binding setup. Actual gameplay validation remains outstanding.


## 1.7.0-beta — Cyberpunk vehicle summoning

- Enumerate loaded TweakDB vehicle records, including mod additions; deduplicate, search names/IDs, paginate and accept validated manual IDs.
- Resolve the selected live record through the native garage and summon system; revalidate before each summon, guard mounted state, cooldown and native refusals.
- Register only the selected missing summon entry; no whole-garage unlock. Add explicit normal/instant summon toggle and optional selected-vehicle hotkey.
- Clear vehicle selection/catalogue on session changes and avoid scanning or summoning from idle draw frames. Actual game runtime remains unverified.


## 1.6.0-beta — initial Cyberpunk CET trainer

- Embed an original RU/EN Lua trainer with one-shot health, money, time and session-local teleport/return actions.
- Add a reviewed trainer install/update page and stable component identity; reuse backups, dependency checks, setup references and removal protection.
- Use the CET overlay and user-assigned hotkeys without changing shared CET binding files.
- Test LuaJIT behaviour with mocked game/ImGui APIs and managed filesystem operations separately; actual gameplay remains unverified.


## 1.5.1-beta — ArchiveXL/TweakXL package fix

- Accept embedded RED4ext plugin Scripts/*.reds, Bundle archives and XL sidecars, Data/*.dat, and r6/config/redsUserHints/*.toml. Keep paths unchanged and retain the target boundary.
- Add full install/disable/reenable/removal regressions using official ArchiveXL and TweakXL packages with their base frameworks.


## 1.5.0-beta — initial Cyberpunk 2077 support (local build)

- Add installation detection including the nested executable, a separate workspace/library card and focused home/components/mods/setups/recovery pages.
- Support bounded legacy archive, redscript, TweakXL, CET and RED4ext package layouts; allow official framework ZIPs and reject REDmod deployment packages.
- Reuse durable reviewed file transactions with per-game target policies; validate final enabled dependencies and reject components changed since preview.
- Protect the original game executable, base archives and script cache; do not execute imported components. Validate native AMD64 rather than treating ARM64 PE64 as x64.
- Include Cyberpunk in update process guards and check its bin/x64 process directory before mutations.


## 1.4.0-beta — updates, OIV folders and experimental RDR2 (local build)

- Add shared updater UI in the library, strict download hash/size/origin checks, bounded cancellable extraction, cleanup on failure and explicit existing installation target.
- Extend supported OIV update.rpf packages with folder additions; reject case-insensitive duplicates and source/destination traversal.
- Fit windows to work areas, improve compact layouts and shared keyboard focus.
- Add separately detected RDR2 workspace with native x64 ASI/component import, dependency checks, reviewed transactions, original restoration, scoped plugin setups and recovery inspection/export/retry. No RDR2 LML/RPF/.NET or gameplay compatibility claim.
- Record GTA V/GTA IV gameplay checks as user-confirmed; new RDR2 gameplay and physical DPI/VM interruption checks remain separate.


## 1.3.0-beta — full GTA V workflows (local build, not published)

- Save plugin order/selection, cars, RPF mods and bounded configuration/trainer snapshots together. Original switches off all managed families; Previous preserves pre-switch state. Migrate plugin-only setups without changing their scope.
- Apply the combined file/archive/state changes with one recovery journal, stale-plan protection and cancellation-safe rollback.
- Add installation preflight for edition/resource formats, dependency presence/bitness, component version display, known file conflicts and optional author build metadata. State unknown compatibility explicitly.
- Add a read-only recovery page with per-file findings, backup/external-edit diagnostics, safe retry, journal-folder access and JSON export.
- Show byte/stage/speed/space progress; cancel streaming copies, extraction, downloads and archive preparation. Prepare encrypted mods-copy conversion privately before publication.
- Keep prior release assets unchanged. In-game/native trainer validation remains a separate gate.

## 1.2.3-beta — audit fixes (local build, not published)

- Reject cyclic/shared RPF directory entries and excessive depth without stack overflow.
- Reject linked game paths before reads/writes through the shared game-path resolver.
- Stage and repair replacement DLC packages before publication. Journal previous files, archive entries and companion metadata so failed or interrupted reinstalls and RPF toggles/removals recover consistently. Preserve external edits by blocking conflicted recovery.
- Block preparation for Online when unmanaged loaders/scripts or enabled add-ons/RPF mods remain; check again before starting the launcher and remove the claim of guaranteed clean Online.
- Keep large add-on and RPF actions off the UI thread. Translate new launch-preparation messages in all ten interface languages.
- Refresh packaged documentation, include the roadmap and validate local documentation links/version during packaging. Previous 1.2.2 release assets remain unchanged.

## 1.2.2-beta — ten interface languages

- The app speaks English, Russian, Ukrainian, German, French, Spanish, Portuguese, Polish, Turkish and Arabic. The language is picked in the game library, in GTA IV settings and in the GTA V sidebar; it switches at once, without a restart. Arabic mirrors the layout right to left. First start follows the Windows language.
- Every screen, tip, crash-doctor finding, catalog description and error message is translated (about 1,490 lines per language). Error messages that came only in English are now in Russian too.
- The in-game trainers stay Russian / English: the GTA IV "Menu language" list offers just those two.
- Fixes: the catalog wrote "и др." after authors in every language; the crash doctor and catalog didn't re-render after a language switch; "Package exceeds development limits" now says the package is too large (over 1000 files or 500 MB).
- Catalog descriptions from a remote catalog update that are newer than this build fall back to English.

## 1.2.1-beta — GTA V trainer: map editor and handling

- GTA V trainer: a map editor (main menu → Map editor). A free camera with a crosshair: pick up, place, move, turn and tilt objects, people and vehicles; freeze, collision, visibility, opacity, gravity; attach to you, your car or another placed thing; copy, delete. About 9,900 objects are listed by group and searchable — their names come from the player's own game archives when the trainer is installed. Maps are saved and loaded in Menyoo's SpoonerPlacements layout, so maps from menyooStuff/Spooner load too (objects, positions, attachments, vehicle colours, a person's scenario or animation). Menyoo's code isn't used, only its file layout.
- Handling: power, gearbox, drive, mass and inertia are taken by a car when it is created, so the trainer recreates the car after such a change.
- Fixes: handling pages kept working on the old car after it was recreated (changes seemed to do nothing); an update.rpf mod that failed half way is now rolled back at once, and resources of 16 MB or more are refused before anything is written.
- GTA V trainer: a handling editor (Vehicles → Handling). About 45 values in 8 groups: engine and gearbox, brakes and steering, grip, suspension, anti-roll, mass and body, damage, other. Quick lines for drive type, power, grip and brakes; presets (drift, track, rally, heavy, rocket, unbreakable); remembered per model; back to stock; export as handling.meta lines; recreate the car for gears and top speed. Derived values (rear shares, reciprocals) are kept in step only where the stock data confirms the relation.

## 1.2.0-beta — GTA V Legacy

- Add-on cars without OpenIV: ModPilot copies and decrypts update.rpf, installs the RageOpenV loader and raises the DLC vehicle table in a copy of gameconfig.xml by itself, on open and before launch. The original file is kept, and raises from older versions are redone from it.
- Broken community packs (the "NAME_Surname" template) are repaired on install. Wrong content.xml paths, enables on foreign devices and misspelled setup2 change sets are fixed, with the original kept in packfix.
- Refused or switched off: Enhanced-only cars (yft 171 / ytd 5) on Legacy, and a second car with an existing model name. Clashing tuning kit and light ids of a later car are renumbered. The page shows cars, models, size and room left.
- Replacement cars (loose .yft/.ytd named like a game car) go into ModPilot's own overlay pack in mods; the game archives are untouched.
- Online without mods: every mod is off for the session and comes back after it, with crash-safe memory.
- Crash doctor: reads the game's own dumps (module + offset), remembers where crashes happened, flags repeats, and knows the build 3889 "DLC vehicle table full" place.
- Trainer favourites can be reordered and removed in the app.
- Trainer: teleport to collectibles known from the start: 50 spaceship parts, 50 letter scraps, 30 underwater finds, 27 peyote plants and 7 golden ones. Positions are read from the player's own game scripts; each page says when an item isn't unlocked by the story yet or has been collected.
- update.rpf mods (graphics, weather): .oiv packages and "update.rpf" folders that replace existing files go into the mods copy and can be switched off or removed. Nested archives, new files, xml edits and other archives are refused with the reasons; nothing is half-installed.
- GTA V catalog: eight more mods by ikt (Manual Transmission, Glowing Brakes, Slam It and others).
- Unverified in game: replacement overlay, online mode, renumbered tuning. Enhanced is still unsupported for add-ons.

## 1.2.0-alpha.3 — GTA V workspace (local only)

- Replace the technical GTA V panel with a WPF shell using the existing ModPilot theme and stable sidebar. Add Home, My mods, Install mod, Components, My setups, Conflicts, and Game/settings pages in Russian and English.
- Home derives its next action from the selected installation and base-file presence. Show search, labelled saved setups, conflict winners, empty states, operation progress/cancellation, and errors. Preserve search and page state during refresh.
- Resolve Play through a matching installed Steam manifest or the selected game’s launcher, without adding launch arguments. Disable it when neither is available.
- Preserve prepared installation reviews, per-copy state, integrity checks and transactional restoration. No vehicle/map/RPF/OIV installation, catalog, GTA V trainer or game-save backup support is added here.
- 267 core checks pass, plus isolated presentation-state probes and actual WPF rendering of seven pages in both languages. Modded GTA V gameplay and Enhanced remain unverified.

## 1.2.0-alpha.2 — automatic GTA V modding base (local only)

- Discover separate GTA V Legacy/Enhanced installations in Steam libraries without creating game state.
- Do not treat the PlayGTAV launcher as a running game; still block changes while GTA5 or GTA5_Enhanced is running.
- Add an in-app Script Hook V + ASI Loader setup action. Read supported builds and the current archive URL from the author's HTTPS page, check game compatibility, validate x64 exports and prepare a reversible install.
- Try direct download, with size limits and restricted redirects. If the site refuses it, open the official page and pick up a matching completed browser download; waiting can be cancelled.
- Recognize plain and decorated C++ exports used by the real Script Hook V. Install exactly the hook and loader by default, without silently adding a trainer or launch-argument files. Repeated setup updates the same managed component and preserves profile references.
- 264 autonomous checks pass. Official metadata and the actual archive were downloaded by the program client. Real x64 components passed install/disable in a private file fixture; installed GTA V and anti-cheat settings were not changed. Modded in-game startup remains unverified.

## 1.2.0-alpha.1 — GTA V development (not published)

- Add a game library at startup with separate GTA IV, GTA V Legacy and GTA V Enhanced workspaces; RDR 2 is a planned, inactive card.
- Keep existing GTA IV settings and engine; add a return-to-library action.
- Preview supported GTA V ASI/script packages without an installed game.
- Install and disable supported GTA V plugins/scripts using a separate durable file batch, original backups, frozen previews and integrity checks. Recover interrupted commits before reading state.
- Add per-installation enabled-mod setups and conflict precedence. Preserve external changes by refusing to overwrite them.
- Reject GTA IV/native x86 formats, mandatory 32-bit managed scripts, executables and unsupported RPF/OIV/vehicle/map packages.
- GTA V in-game operation and component build compatibility are unverified. No GTA V installation is available in this development environment.

## 1.1.2-beta — 2026-10-31 (local test build)

- Identify Ultimate ASI Loader from x86 PE exports/product information instead of accepting a DLL filename; compare four-part component versions.
- Install, upgrade and remove managed component archives through prepared transactions. Preserve user-edited component files; clean up obsolete unchanged binaries on upgrade.
- Explain conflict winners, overwritten changes and resolution; distinguish episode-specific resources and data sections.
- Capture independent profile tuning, colors, trainer/limit flags and supported component settings, including absent optional settings. Switch profiles transactionally; report component version differences. Component binaries are not versioned by profiles.
- Validate update versions and filenames, compare numeric prereleases, require an exact unambiguous checksum filename and one installer per archive.
- Reject unsafe archive paths/links; bound IMG/RPF tables and stream extracted IMG entries.
- Atomically persist trainer data; reject non-finite/overflowing saved coordinates. Rebuild the embedded trainer against ScriptHookDotNet.
- Preserve existing vehicle objects after a transaction so the selected add-on is not rejected as a duplicate of itself.
- Integration-tested on a separate GTA IV 1.2.0.59 copy: real archive/model checks, replacement and add-on preparation, trainer startup, profile roundtrip and original-game preservation. Manual menu/spawn confirmation supplements automation; the full trainer gameplay matrix is still pending.

- Harden PE header, section and import parsing; limit executable reads to 256 MiB.
- Diagnose x64 managed plugins as incompatible with the x86 game as well.
- Refresh dependency status against the prepared configuration, including components installed from the wizard.
- Parse game versions structurally; a FusionFix mention alone no longer establishes Complete Edition support.

- Prepare final mod files in a private workspace; confirmation commits those same bytes.
- Show actual generated archive names and before/after fragments for small text data files.
- Durable snapshots restore previous files and state on a failed or interrupted commit. Incomplete rollback keeps snapshots and blocks launch.
- Reject stale previews and preserve unexpected external edits during rollback.
- Stage adoption/quarantine changes together with installation.
- Preserve timestamps for generated payloads and restore previous file timestamps/attributes on rollback.
- Local test build only; not published. The 1.1.1-beta distributables remain available as the previous version.

## 1.1.1-beta — 2026-10-31

- Durable recovery journal for interrupted managed mod applies; space checks and original ownership saved before writes.
- Single application instance per user session, a cross-process game write lease, and closing blocked during operations.
- Installation plan with file targets, overlaps, dependencies and space estimate.
- Diagnostic impact labels, next steps and a recovery action.
- Editable local support report with path redaction.
- Fix build manifest path validation, vanilla restore while the game is running, retaining tuning on vanilla restore, and save backup pruning during restore.
- Automated release gates; isolated installer test mode. Manual GTA IV gameplay validation remains pending.

## 1.1.0-beta — 2026-10-28

- Fixes: an OpenIV package for GTA V can no longer be installed (the button was active); "Take my game apart" never offers the game's own files (GTAIV.exe, steam_api.dll…) for quarantine even after a Steam update re-dates them; mods from the catalog keep the catalog's name; Nexus file names ("Pack v3.1-357-3-1-2026-09-07T01-38Z-…") become clean mod names; catalog categories follow the language; the "waiting for download" banner closes after 30 minutes; downloaded catalog archives are removed after install.
- **Mod catalog** (new "Catalog" page): 44 checked mods that work with the Complete Edition and FusionFix — Console Visuals parts, Xbox Rain Droplets, Radio Restoration, Vehicle Pack, LibertyCityPlates, Fidelity Popcycle, Liberty Loadout and more. Mods released on GitHub download and install in one click (through the usual wizard); for other sites ModPilot opens the author's page and picks the archive up from Downloads. Files are never re-hosted. The list is read from the ModPilot repository, so it can grow without a new version.
- **Graphics in one click** (Game page): "Low-end PC / Balanced / Maximum" presets for FusionFix — antialiasing, shadow filter and resolution, volumetric fog, sun shafts, ambient occlusion, depth of field. Your previous settings are saved first; "As it was" brings them back. The game's own settings file isn't touched.
- **Save copies**: before every launch from ModPilot the game's saves are copied (only when they changed; the newest 15 are kept). Settings → Saves → "Save copies…" lists them; "Restore" puts one back after copying the current saves first, so nothing is lost.
- **OpenIV packages (.oiv)** install like any other mod — no OpenIV needed: files for game archives, data-file edits and plugins become a normal managed mod you can switch off and remove. The package's "delete game file" commands are never run; GTA V / Max Payne 3 packages are refused.
- **Take my game apart** (Home and Diagnostics): lists everything in the game that wasn't installed with ModPilot — mods copied into update, ASI plugins, scripts, the modding base (FusionFix, ASI Loader, ScriptHook, DXVK…) and original files changed by OpenIV — grouped by what came in together. One click adopts a mod (it goes through the install wizard and joins your list) or moves it to quarantine.

## 1.0.1-beta — 2026-10-28

- **Auto-update**: ModPilot checks GitHub for a new version at start, shows a banner on the home page and installs the update in one click (the download is checked against SHA256). Settings → Updates: check now, turn the check off.
- Car names from mod titles read properly ("Imponte Arbiter X", "VAZ 2172" instead of "imponte-arbiter-x- -moving-steering").
- ZolikaPatch asked for by a readme is shown as "not needed" on the Complete Edition (was "installed").

## 1.0.0-beta — 2026-10-28

First public beta. New name: **ModPilot** (formerly IV Mod Manager), new logo, installer, proprietary freeware license.
- Trainer weapons: by category with ammo, ready-made and own loadouts, no reload, keep weapons after death, drop weapon, arm bodyguards.
- Installs car replacements and add-ons, models, textures, skins, graphics mods, scripts, trainers, map mods and data-only mods from zip / rar / 7z / folders / loose files.
- Add-ons as separate cars: own spawn name, wheel and stance data from the car the model was made for, traffic, in-game name.
- Textured 3D preview of mod cars and stock cars; "before / after" in the install wizard.
- Mod list with priorities, conflicts, profiles, `.ivmmpack` sharing, "Restore original".
- Game cars page with handling and colour tweaks.
- Diagnostics with one-click fixes, crash analysis, "Find the culprit".
- One-click components: FusionFix, Ultimate ASI Loader, ScriptHookDotNet, IV-SDK .NET, VC++ and DirectX.
- Built-in trainer (ScriptHookDotNet): car spawner with add-ons, garage, people, player, weapons, teleport, world, fun (free flight, autopilot, drift counter, chaos), dashboard speedometer, customisable HUD.
- Fixes mod authors' texture-name mistakes automatically (e.g. invisible rims).
- Map mods: `gta.dat` lines merged with other mods instead of replacing the file.
- Experimental mode without FusionFix (archives registered in `images.txt`).
- Russian and English interface; new home page, dark title bar, animations.

### Known issues
- The trainer menu and speedometer may flicker with DXVK / FusionFix (ScriptHookDotNet overlay). Fallback: trainer "Settings → Drawing → game".
