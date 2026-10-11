# Round in Review — Windows downloads

This repository is the **public, binaries-only distribution location** for [Round in Review](https://roundinreview.com) and its Windows desktop app, **CS2 Demo Library**. Application source code and development infrastructure remain in separate private repositories.

## Download status

**Public beta installer published:** [CS2 Demo Library v1.5.1](https://github.com/kvzoo/roundinreview-downloads/releases/tag/v1.5.1). The installer and checksum are uploaded. Independent signed-out download and file hashing remain launch acceptance checks.

The publicly published v1.5.1 installer metadata is:

| Field | Value |
| --- | --- |
| Version | `1.5.1` |
| Installer asset name | `CS2.Demo.Library.Setup.1.5.1.exe` |
| Size | `113851952` bytes |
| SHA-256 reported by the original GitHub release asset | `034953be1fdbe9a9fa10070e9c280712a1cb71eaf65e46a6676d540327b9a5a2` |

**Verification:** GitHub reports the same installer size and SHA-256 in the private and public releases. Independent download and byte-level hashing have not yet been performed.

## Release verification (maintainers)

1. Obtain the exact approved installer binary from the private `kvzoo/cs2-demo-library` v1.5.1 release, using authenticated access.
2. Confirm its SHA-256 is exactly `034953be1fdbe9a9fa10070e9c280712a1cb71eaf65e46a6676d540327b9a5a2`. Confirm there are no bundled credentials or private files.
3. Create a GitHub Release in **this** public repository with tag `v1.5.1`. Upload the installer as a **release asset**, not as a Git-tracked file or source tree. Upload a checksum text file listing the exact filename and digest.
4. Open the public download in a signed-out browser; retrieve it and recheck the SHA-256 of the downloaded file. Confirm the release remains public.
5. Only after these checks, configure the reviewed public HTTPS asset URL **and** SHA-256 together in the website's `dist/download-config.js` through a feature PR and normal release approvals.

Do not mirror the private source repository, demo files, logs, access tokens or development artifacts here. Keep public release notes factual, and do not claim Windows versions or Steam onboarding paths that have not been tested.

## Verify a download on Windows

After downloading the release installer, open PowerShell in its folder and run:

```powershell
Get-FileHash -Algorithm SHA256 ".\CS2.Demo.Library.Setup.1.5.1.exe"
```

Compare the resulting digest with the corresponding public release checksum. If the values differ, **do not run the installer**.

**Publisher notice:** The current Windows installer is unsigned. Windows may display an unknown-publisher or SmartScreen warning. Verify the source and checksum; do not bypass protections for an unverified file.

## Getting started and help

- Website: https://roundinreview.com
- Beta support: https://discord.gg/S93zkagJDy
- Full setup and privacy explanations will be available on the official website after its reviewed V1 update is published.
