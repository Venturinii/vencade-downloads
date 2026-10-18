# Vencade Studios — Downloads

Public download distribution for the **Vencade Studios Launcher**, separate from the private source repository. This repository contains only public download metadata, instructions and (after approval) Windows installer assets.

**STATUS: PRE-LAUNCH. NO PUBLIC INSTALLERS YET.** Please do not download unverified binaries or announce a public launch.

## Games and catalog

The public catalog is at [catalog/catalog.json](catalog/catalog.json).

- **Dojo Raiders:** separate, optional Windows client, presently **not available for public installation** (`dojoRaiders.available=false`).
- **Eleven Cup:** listed as *Em desenvolvimento / In development*; no installer (`elevenCup.available=false`).
- Users install the **launcher only** first and choose which games to install after they become available.
- The launcher checks stable GitHub Releases for its own required updates; games are updated independently using the public catalog.

## Planned Windows artifacts

When the owner approves release, two distinct GitHub Releases will be used:

| Artifact | Release tag | GitHub release setting |
| --- | --- | --- |
| Vencade Studios Launcher Setup `.exe` + `latest.yml` (+ optional blockmap) | `v0.2.0` | **Stable**, after QA |
| Dojo Raiders Client `.zip` | `dojo-raiders-client-v0.1.0` | **Pre-release** (not latest stable) |

The developer can build the files privately in [`Venturinii/vencade-launcher`](https://github.com/Venturinii/vencade-launcher), then invoke **Prepare public release drafts (manual QA only)** in the *private* repository. It requires a fine-grained token stored as a GitHub Actions secret there, authorized **only** for this public repository with Contents write permission. This creates **draft releases**, not public downloads, and does not enable the catalog.

**Do not paste access tokens into this public repository, source files, PR descriptions, release notes or ChatGPT.**

## Activation after testing

1. Test installation on Windows 10/11, Twitch OAuth login, OBS capture, install/uninstall, forced version updates, network failure and file-integrity checks.
2. Review Windows code-signing before distribution; current private test builds are **unsigned**.
3. Promote the approved launcher draft to a **stable** public release and separately publish the Dojo client as **pre-release**.
4. Verify the actual release files download anonymously and match the generated SHA-256.
5. Only then change [catalog/catalog.json](catalog/catalog.json) from `dojoRaiders.available=false` to `true` and insert the **real** version, executable name, public release URL, minimum launcher version and matching SHA-256. Never insert guessed URLs or hashes.
6. Validate that outdated versions block Play until the required update finishes. Leave Eleven Cup unavailable.

## Security and scope

- The Dojo client is an installed Windows application that uses the existing **online** Dojo Raiders service; it is **not** an offline server.
- Twitch authentication inside Electron has **not** passed end-to-end Windows validation. Do not promise compatibility yet.
- No private source code, OAuth credential, MongoDB URI, certificates or signing keys may be stored here.
- A successful GitHub Actions build is **not** equivalent to a safe public release. Review and owner's approval are required.

© Vencade Studios. All rights reserved.
