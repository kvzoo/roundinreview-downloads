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

1. Confirm the public release contains only the approved installer and checksum; no source code, credentials, or private materials.
2. GitHub reports identical installer size (113851952 bytes) and SHA-256 for the original private and new public v1.5.1 release assets.
3. **Still required:** retrieve the installer while signed out and independently compute the downloaded file's SHA-256. It must equal `034953be1fdbe9a9fa10070e9c280712a1cb71eaf65e46a6676d540327b9a5a2`.
4. The public HTTPS download URL and digest are configured together in website feature PR #8. Review CI and browser behavior before approving the website release.

Never mirror the private source repository, demos, logs, access tokens, or developer artifacts here.

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
