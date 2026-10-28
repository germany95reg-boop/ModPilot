# ModPilot for GTA IV

[Русский](README.md) · **English**

A mod installer for **GTA IV: Complete Edition**. Drop a mod archive on the window — it works out what the mod is and where it goes, shows the car in 3D and installs it without touching the game's original files. Plus problem diagnostics, a built-in in-game trainer and one-click "back to vanilla".

> Version **1.0.0-beta** — the first public beta, tested on one game install. If something goes wrong, "My mods → Restore original" undoes everything; the log is at `%AppData%\IVModManager\log.txt`.

**[⬇ Download ModPilot for GTA IV](https://github.com/germany95reg-boop/ModPilot/releases/latest)** — `ModPilot-…-setup.zip`, the installer is inside.

## Features

**Installs any mod**
- zip / rar / 7z / folder / loose `.wft` `.wtd` files — just drag them in;
- cars: **replace** a stock car or **add a new one (add-on)** — a separate car with its own spawn name, driving in traffic;
- models, textures, skins, graphics (ENB, ReShade, DXVK), `.asi` / `.net.dll` scripts, trainers, map mods, data-only mods (e.g. handling);
- reads the readme: which car to replace, lines for `vehicles.ide` / `handling.dat`, what else the mod needs;
- fixes common author mistakes (e.g. invisible rims caused by a misnamed texture).

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
- Save games are never touched.

## Beta limitations

- **Known issue:** the trainer menu and speedometer may flicker with DXVK / FusionFix. This comes from ScriptHookDotNet drawing over the frame. A flicker-free fallback is "Settings → Drawing → game" in the trainer menu (Russian text is shown in Latin letters there).
- Without FusionFix the mode is experimental: TLAD/TBoGT mods, custom add-on names and extended limits don't work.
- Map mods and parts of the trainer are lightly tested in game.
- Encrypted `.img` files inside mods are loaded as a whole, without looking inside.
- Cyrillic in add-on names may not show if the game font lacks it.

Found a bug? Open an [issue](https://github.com/germany95reg-boop/ModPilot/issues) and attach `%AppData%\IVModManager\log.txt` and a screenshot.

## License

Free to use, **all rights reserved** (© 2026 BADURGOW, rpomidorow@gmail.com). Download it from the official page and use it; do not sell, re-upload, modify or pass it off as your own — see [LICENSE](LICENSE). Third-party components: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

Not affiliated with Rockstar Games or Take-Two Interactive. Grand Theft Auto is their trademark.
