# ModPilot for GTA IV and GTA V

[Русский](README.md) · **English**

A mod installer for **GTA IV: Complete Edition** and **GTA V Legacy**. Drop a mod archive on the window — it works out what the mod is and where it goes, shows the car in 3D and installs it without touching the game's original files. Plus problem diagnostics, a built-in in-game trainer and one-click "back to vanilla".

> Version **1.2.2-beta**: the interface in 10 languages; GTA V Legacy, with a map editor and a handling editor in the trainer. It is a beta, tested on one install of each game. If something goes wrong, "My mods → Restore original" undoes everything; the log is at `%AppData%\IVModManager\log.txt`.

**[⬇ Download ModPilot](https://github.com/germany95reg-boop/ModPilot/releases/latest)** — `ModPilot-…-setup.zip`, the installer is inside.

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
- the interface in 10 languages: English, Russian, Ukrainian, German, French, Spanish, Portuguese, Polish, Turkish and Arabic (right to left); it switches at once, no restart. The in-game trainers are in Russian and English;
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

## GTA V Legacy

- a separate window for each GTA V install; the game's original files are not changed;
- scripts and plugins: `.asi`, ScriptHookVDotNet scripts and their settings folders — install, on/off, order, remove with the old files restored;
- components in one click: ScriptHookVDotNet, the `mods` folder loader (RageOpenV); Script Hook V from its author's page;
- **add-on cars without OpenIV:** ModPilot copies `update.rpf` into `mods`, opens it with the key from your own `GTA5.exe`, installs the loader and raises the game's limits so many cars don't break loading; cars made from broken templates are fixed, Enhanced-only cars are switched off in Legacy;
- **replacement cars** (`.yft`/`.ytd` named like a game car) as ModPilot's own pack over the original, off in one click;
- **update.rpf mods** (graphics, weather): `.oiv` packages and `update.rpf` folders that replace game files, with switch-off and undo. Mods with nested archives, new files or xml edits still need OpenIV — the app says what isn't supported and changes nothing;
- a GTA V mod catalog: checked GitHub mods in one click;
- "Online without mods": every mod is off for a GTA Online session and comes back afterwards;
- the crash doctor reads the game's own dumps and tells what crashed and where;
- **built-in trainer** (F7): cars and add-ons, teleport, weather, time, favourites, teleport to collectibles — 50 spaceship parts, 50 letter scraps, 30 underwater finds, 27 peyote plants and 7 golden ones, read from your own game files and available from the start.
- **map editor** (new in 1.2.1): a free camera with a crosshair — place, move, turn and attach objects, people and vehicles; about 10,000 objects from your own game, searchable; maps are saved and loaded in Menyoo's layout, so ready-made maps from `menyooStuff\Spooner` open too;
- **handling editor** (new in 1.2.1): about 45 values of how the car drives — power, drive, gearbox, grip, brakes, steering, suspension, anti-roll, mass, centre of mass, damage; presets (drift, track, rally and more), remembered per model, back to stock, export as `handling.meta` lines.

## Requirements

- Windows 10 / 11 (64-bit);
- GTA IV: Complete Edition (**FusionFix** recommended — the app installs it for you);
- or GTA V Legacy with **Script Hook V**; GTA V Enhanced: scripts only for now, no add-on cars;
- for the trainer: ScriptHookDotNet (GTA IV) or ScriptHookVDotNet (GTA V), one click each.

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

- GTA V: replacement cars, "Online without mods" and real graphics `.oiv` packages are little tested in game yet. Always switch on "Online without mods" before GTA Online.

- **Known issue:** the trainer menu and speedometer may flicker with DXVK / FusionFix. This comes from ScriptHookDotNet drawing over the frame. A flicker-free fallback is "Settings → Drawing → game" in the trainer menu (Russian text is shown in Latin letters there).
- Without FusionFix the mode is experimental: TLAD/TBoGT mods, custom add-on names and extended limits don't work.
- Map mods and parts of the trainer are lightly tested in game.
- Encrypted `.img` files inside mods are loaded as a whole, without looking inside.
- Cyrillic in add-on names may not show if the game font lacks it.

Found a bug? Open an [issue](https://github.com/germany95reg-boop/ModPilot/issues) and attach `%AppData%\IVModManager\log.txt` and a screenshot.

## License

Free to use, **all rights reserved** (© 2026 BADURGOW, rpomidorow@gmail.com). Download it from the official page and use it; do not sell, re-upload, modify or pass it off as your own — see [LICENSE](LICENSE). Third-party components: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

Not affiliated with Rockstar Games or Take-Two Interactive. Grand Theft Auto is their trademark.
