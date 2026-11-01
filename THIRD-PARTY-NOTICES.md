# Third-party notices

ModPilot itself is proprietary software (see LICENSE). It includes the open-source components below, which stay under their own licenses.

## Included in ModPilot.exe

### SharpCompress
Archive reading (zip, rar, 7z). https://github.com/adamhathcock/sharpcompress

    The MIT License (MIT)
    Copyright (c) 2014 Adam Hathcock

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.

### .NET Runtime and Windows Desktop (WPF)
https://github.com/dotnet/runtime · https://github.com/dotnet/wpf

    The MIT License (MIT)
    Copyright (c) .NET Foundation and Contributors

    (Same permission notice and disclaimer as above.)

## Downloaded only when the user asks (not included)

ModPilot downloads these from their official release pages when the user presses "Install" on the Components page. They belong to their authors and keep their own licenses:

- **GTAIV.EFLC.FusionFix** — ThirteenAG and contributors. https://github.com/ThirteenAG/GTAIV.EFLC.FusionFix
- **Ultimate ASI Loader** — ThirteenAG. https://github.com/ThirteenAG/Ultimate-ASI-Loader
- **ScriptHookDotNet** (Complete Edition fork) — Hazard, Tomasak. https://github.com/Tomasak/gta4_scripthookdotnet
- **IV-SDK .NET** — ClonkAndre. https://github.com/ClonkAndre/IV-SDK-DotNet
- Microsoft Visual C++ Redistributable and DirectX End-User Runtime — Microsoft.
- **ScriptHookVDotNet** — crosire and contributors (GTA V Enhanced build: Chiheb-Bacha). https://github.com/scripthookvdotnet/scripthookvdotnet
- **Script Hook V** — Alexander Blade. Not downloaded by ModPilot: the app opens http://www.dev-c.com/gtav/scripthookv/.
- **RageOpenV** (GTA V mods-folder loader, GPL-3.0) — martonp96, Chiheb-Bacha. https://github.com/Chiheb-Bacha/RageOpenV
- **CodeWalker key data** (`magic.dat`, GTA V) — dexyfex. Downloaded from https://github.com/dexyfex/CodeWalker (fixed commit, checked by hash) to the user's PC when they prepare add-on cars; it is useless without the user's own game.

### CodeWalker — GTA V NG decryption method
https://github.com/dexyfex/CodeWalker

    The MIT License (MIT)
    Copyright (c) 2015 Neodymium; CodeWalker (c) dexyfex

    (Same permission notice and disclaimer as above.) ModPilot's code is its own following the method
    of CodeWalker's GTACrypto/GTAKeys (key selection, round structure, magic data layout).

The built-in trainer (`IVMMTrainer.net.dll`) is ModPilot's own code; it runs on ScriptHookDotNet but does not contain it.

## Game data

No game files are included. Encrypted game archives are read with a key taken from the user's own `GTAIV.exe` at run time; the key is not stored in the app. The same goes for GTA V: the AES key is found in the user's own `GTA5.exe`; NG keys come from the downloaded CodeWalker data, unlocked with that key on the user's PC.

Grand Theft Auto IV and Grand Theft Auto V are © Rockstar Games / Take-Two Interactive. ModPilot is not affiliated with them.
