# ModPilot

[Русский](README.md) · **English**

**Mod manager for GTA IV, GTA V, Cyberpunk 2077 and RDR 2 — with its own in-game trainers.**

Drop a mod in. ModPilot works out what it is, tells you what else it needs, shows exactly what will change, installs it without touching the game's original files — and takes it back out with one click.

> Version **1.15.1-beta** · Windows 10 / 11 (64-bit) · 10 languages · free
>
> New: soft interface motion; bug reports through a protected relay (reports from 1.15.0 don't reach the author — please update). In 1.15: any mod installs in GTA V and Cyberpunk 2077 with a plain-words review, update a mod over itself, top lists in every catalog, Cyberpunk save copies. Full list: [CHANGELOG.md](CHANGELOG.md).

**[Download the latest release](https://github.com/germany95reg-boop/ModPilot/releases)**

## What it does

- **See before you install.** The review says what the mod is, what it still needs and where to get it, lists every file it will add or replace, and anything left out with the reason. Nothing changes until you press Install.
- **Everything can be undone.** Switch mods off and on, change priority, update a mod over itself, remove it — the replaced files come back.
- **Setups.** Save the set of enabled mods under a name and switch between setups; "Original" turns every managed mod off.
- **Catalogs with top lists:** 54 mods for GTA IV, 25 for GTA V, 92 for Cyberpunk 2077. GitHub mods install in one click from the author's release; for other sites ModPilot opens the author's page and picks the archive up from your Downloads folder. Nothing is re-hosted.
- **Save copies** before each launch from ModPilot, restore in one click.
- **Crash help:** reads what the game and the mod frameworks left behind and names the mod that failed; "Find the culprit" narrows it down by halves.
- **Own trainers** (F7) for GTA IV, GTA V and Cyberpunk 2077.
- **🐞 Report a bug** from any window: you see exactly what is sent; user name, personal folders and e-mail are hidden.

## Games

### Cyberpunk 2077
- Any mod installs the way you would unpack it into the game folder (archive, bin/x64, engine, r6, red4ext, mods). Only what would break the game is left out — programs, files the game makes itself, the base game's own archives, damaged archives — each with the reason.
- "What this mod is" in plain words: archives, ArchiveXL, TweakXL, redscript, CET, RED4ext, sounds, REDmod, ReShade — and where its settings are.
- Requirements from Nexus Mods (only mod ids are sent) and from the mods' own scripts and patch files; missing ones are listed on Home.
- Installation options chooser (Option A / B, FOMOD folders), archive load order (modlist.txt), resource conflicts between archives.
- Components: CET, RED4ext, redscript, ArchiveXL, TweakXL, Codeware — installed, versions, updates.
- Log doctor for TweakXL, ArchiveXL, RED4ext, redscript and CET; "New in Downloads"; drag and drop.
- Trainer (needs Cyber Engine Tweaks; spawning and weather need Codeware): player, money, time, teleport, vehicles and mod vehicles, weapons, cyberware, world, police, nearby enemies, progression, items, mode profiles.

### GTA V (Legacy)
- Script Hook V, ASI Loader and Script Hook V .NET in one click from their authors, with a game-build check.
- Any script or plugin mod installs; what can't go into the game is left out with the reason.
- Add-on cars without OpenIV: a copy of update.rpf in the mods folder, raised DLC vehicle limits, repair of common broken packs, renumbered tuning and light IDs. Replacement cars in an overlay you can switch off.
- .oiv packages and update.rpf replacements (graphics, weather).
- Crash doctor (Windows reports, game dumps, Script Hook V / SHVDN / ASI Loader / RageOpenV logs), "Online without mods".
- Trainer: map editor (Menyoo Spooner XML), handling editor, spawner with add-ons, tuning, player, weapons, teleport with collectible locations read from your own game, world, drift mode. Story mode only.
- GTA V Enhanced: scripts and plugins only.

### GTA IV: Complete Edition
- Replacement and add-on cars with a 3D preview; add-ons get their own spawn name, appear in traffic and keep the donor's sound.
- Models, textures, skins, graphics (ENB, ReShade, DXVK), .asi and .net scripts, map mods, data mods; .oiv packages without OpenIV.
- Reads the mod's readme; fixes typical author mistakes such as misnamed textures.
- "Take my game apart": finds mods installed by hand and takes them under management or into quarantine.
- FusionFix, ASI Loader, ScriptHookDotNet in one click; FusionFix graphics presets; vehicle limits.
- Trainer: car spawner with add-ons by name, garage, people, god mode, weapons, teleport, weather, traffic, speedometer.

### Red Dead Redemption 2 (experimental)
- Script Hook RDR2 and native .asi plugins with their settings: install, switch off, update, setups. LML and RPF mods aren't supported yet.

## How it keeps your game safe

- The games' own archives are never edited; mods live in ModPilot's own copies and folders.
- Every file a mod replaces is backed up and restored when the mod is removed.
- Installs are transactional: a failed or interrupted install is rolled back; a file changed by another program is not overwritten.
- Saves are only copied; they are written back only when you press Restore.
- Mod archives are only unpacked and inspected — nothing from them is run. Frameworks are downloaded only from their authors.

## Getting started

1. Download `ModPilot-…-setup.zip` and run the installer inside, or unzip `ModPilot-…-win-x64.zip` anywhere and run `ModPilot.exe`. .NET is built in.
2. Choose your game in "My games". Steam installs are found by themselves.
3. Drag a mod archive onto the window, read the review, press Install.
4. Start the game with Play.

**"Windows protected your PC" / unknown publisher?** ModPilot isn't signed with a paid certificate. Click "More info" → "Run anyway".

ModPilot finds new versions by itself and updates without touching your mods, settings or saves.

## Beta notes

- Tested on one install of each game. The trainers and some install types are lightly tested in game — make a separate save first.
- Don't use mods in GTA Online. "Online without mods" switches managed mods off, but playing online with modified files is at your own risk.

## Languages

English, Russian, Ukrainian, German, French, Spanish, Portuguese, Polish, Turkish, Arabic (right-to-left layout). The in-game trainers are in English and Russian.

## Bugs and ideas

Press **🐞 Report a bug** in the program, or open an issue here. The log is at `%AppData%\IVModManager\log.txt`.

## License

Free to use, **all rights reserved** (© 2026 BADURGOW, rpomidorow@gmail.com). Download it from the official pages and use it; do not sell, re-upload, modify or pass it off as your own — see [LICENSE](LICENSE). Third-party components: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

Not affiliated with Rockstar Games, Take-Two Interactive or CD PROJEKT RED. Grand Theft Auto, Red Dead Redemption and Cyberpunk 2077 are trademarks of their owners.
