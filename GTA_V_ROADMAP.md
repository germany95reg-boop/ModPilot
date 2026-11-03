# GTA V development roadmap

## Implemented in 1.3.0-beta

- Full setups across plugins, cars, RPF and bounded configuration/trainer snapshots; previous-state undo and scoped legacy migration.
- Package preflight, read-only recovery inspection/export/retry, byte progress and cancellable copy/extraction/download work.
- Separate installations/editions, bilingual trainers and a ten-language WPF interface.
- ASI/script preparation, integrity checks, original backups and durable file transactions.
- Legacy add-on cars, replacement overlays, supported existing-file update.rpf/OIV mods, catalog, crash diagnostics, save backups, map/handling trainer tools.
- Durable recovery for add-on installs/reinstalls, enable/disable/removal and RPF mod operations. Archive rollback restores entries and leaves unused appended data intact.
- Cyclic/deep RPF rejection and linked-path rejection at the game-path boundary.
- Launch preparation blocks known external loaders/scripts and enabled add-ons/RPF mods; it does not certify original archives as clean or guarantee Online safety.

## 1.4.0-beta follow-up

- User confirmed GTA V and GTA IV gameplay checks on 2026-11-02. This is user evidence, not an automated reproduction of every trainer scenario.
- OIV folder additions supported for existing update.rpf entries; duplicate/path checks reject the entire package.
- Shared updater, compact layouts and initial RDR2 native-plugin adapter implemented. RDR2 LML/RPF/.NET and real gameplay remain outstanding.

## Remaining validation and development

1. Real Legacy regression: install, launch, spawn, disable, profile changes, recovery and repeated sessions after the 1.2.3 fixes.
2. Trainer gameplay matrix: maps and attachments, invalid coordinates, handling changes and recreated vehicles.
3. Broader OIV/nested archive workflows and compatibility/dependency diagnostics; broader author-supplied dependency/version metadata.
4. Installer/update tests in an isolated VM, real DPI/keyboard/accessibility checks and native component compatibility by game build.
5. Enhanced installation and gameplay validation separately; no claim of Legacy add-on compatibility with Enhanced.
6. RDR 2 after the shared data/recovery model is validated for GTA V.

Primary references: [Script Hook V](https://www.dev-c.com/gtav/scripthookv/), [SHVDN installation](https://github.com/scripthookvdotnet/scripthookvdotnet/wiki/User-Guides), [SHVDN Enhanced](https://github.com/Chiheb-Bacha/ScriptHookVDotNetEnhanced).
