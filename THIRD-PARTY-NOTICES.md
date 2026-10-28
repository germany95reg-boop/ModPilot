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

The built-in trainer (`IVMMTrainer.net.dll`) is ModPilot's own code; it runs on ScriptHookDotNet but does not contain it.

## Game data

No game files are included. Encrypted game archives are read with a key taken from the user's own `GTAIV.exe` at run time; the key is not stored in the app.

Grand Theft Auto IV is © Rockstar Games / Take-Two Interactive. ModPilot is not affiliated with them.
