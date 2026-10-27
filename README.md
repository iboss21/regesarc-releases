# RegesARC for Windows

RegesARC is a local AI workstation for Windows by **LIKE A KING INC.**,
developed by iBoss / Davidio. It runs AI models on your own computer: chat,
model library, Load Lab memory planning, a local OpenAI-compatible API server and
agent tools. Website: <https://regesarc.com>

This repository hosts the **Windows installers only**. The source code is
private and is not published here.

## Download

Get the installer from the [latest release](https://github.com/iboss21/regesarc-releases/releases/latest).

| Version | File | Size | SHA-256 |
| --- | --- | --- | --- |
| 0.0.14 | `RegesARCSetup-x64-0.0.14.exe` | 1.30 GB (1,303,740,362 bytes) | `74dfc47d833ba5d7c4ae39c80001743637fe69683939bb8610b73bf4c745fdd8` |

> **Unsigned development preview.** The installer is not code-signed yet, so
> Windows SmartScreen may warn before it runs ("More info", then "Run anyway").
> Verify the SHA-256 below before you run it. Features and measured results are
> in each release's notes; speeds measured on one machine are not promises for
> other hardware.

## System requirements

- Windows 10 or Windows 11, 64-bit (x64). Installs for the current user; no
  administrator rights needed.
- An NVIDIA GPU is recommended, with a current NVIDIA driver. The bundled GPU
  engine is built for GeForce RTX 40-series cards (CUDA sm_89) and was tested on
  an RTX 4070 SUPER 12 GB. Other GPUs have not been qualified.
- About 2.2 GB of disk space for the app, plus disk space and system memory for
  the models you use.
- Models are not included. RegesARC reads GGUF model files you already have, in
  place. Each model keeps its own license.

## Verify the download

Each release includes `RegesARC-<version>-SHA256SUMS.txt`. Compare the
installer's hash with it before running the installer.

PowerShell:

```powershell
Get-FileHash .\RegesARCSetup-x64-0.0.14.exe -Algorithm SHA256
```

Command Prompt:

```
certutil -hashfile RegesARCSetup-x64-0.0.14.exe SHA256
```

The result must equal
`74dfc47d833ba5d7c4ae39c80001743637fe69683939bb8610b73bf4c745fdd8`
(letter case does not matter). If it differs, delete the file and download it
again.

## Install and uninstall

Run the installer. It installs to `%LOCALAPPDATA%\Programs\RegesARC` and keeps
settings and conversations in `%APPDATA%\RegesARC`. Uninstall from Windows
Settings > Apps. Uninstalling does not delete your model files.

## License

RegesARC is proprietary software. Copyright (c) 2026 LIKE A KING INC. All
rights reserved. See [LICENSE](LICENSE). Third-party components keep their own
licenses: see [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt) and the
notices installed with the app.

## Support and security

Questions: <https://www.likeakinginc.com/#enquiries>. Please report security
problems privately through this repository's
[security advisories](https://github.com/iboss21/regesarc-releases/security/advisories/new),
not in public issues.
