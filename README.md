# Vencade Studios — Downloads

Official public **beta** builds for **Vencade Studios Launcher**, with an optional Dojo Raiders Windows client. The source code stays in the private `Venturinii/vencade-launcher` repository.

## Download for Windows 10/11 x64

**[Download Vencade Studios Launcher v0.2.2](https://github.com/Venturinii/vencade-downloads/releases/download/v0.2.2/Vencade-Studios-Launcher-Setup-0.2.2.exe)** (approximately 93 MB)

New in v0.2.2: game ZIP extraction now uses a streaming extractor (fixes the previously reported ENOENT/chmod error on resources/app.asar). The default Dojo Raiders folder is now `Games/Dojo Raiders` inside the launcher installation directory (normally on the Windows C: drive), unless the user chooses another folder. Future launcher updates include game-folder preservation.\n\nIntroduced in v0.2.1: select a game from the left menu to open its details on the right. Install Dojo Raiders to the default folder or choose another Windows folder. A progress bar now reports download and extraction; the launcher stays responsive and installation errors remain visible. Once installed, **Install** switches to **Play**.

After installing:
1. Start **Vencade Studios Launcher**.
2. Choose **Português (BR)** or **English (US)**.
3. Select **Dojo Raiders** in the left menu and click **Instalar / Install**. Choose the default folder or another directory. It downloads only the Dojo Raiders client (approximately 357 MB).
4. Click **Jogar / Play**. The Dojo Raiders client opens as a separate Windows application, using the existing online website/server.
5. **Eleven Cup** is visible as *Em desenvolvimento / In development*, but cannot yet be installed.

**[Releases and versions](https://github.com/Venturinii/vencade-downloads/releases)**

## Public beta notice

These are **unsigned Windows builds**. Windows SmartScreen and antivirus products may display warnings. Install only from this official release and inspect the publisher information and download integrity; if uncertain, do not proceed. Twitch login inside the desktop client and OBS capture have not yet passed end-to-end Windows testing. Players are testing these capabilities through the public beta.

Please report login, installation or update issues to Vencade Studios. Do not use this early beta as your sole setup for an important live stream.

Dojo Raiders is **online-only**, and requires access to `dojoraiders.com` and Twitch. It does not install the game backend or Twitch credentials onto your computer.

## Updates

The launcher checks the **latest stable** GitHub Release for mandatory launcher updates. Until those are installed it blocks the game. Each game checks [catalog/catalog.json](catalog/catalog.json) separately:
- `dojoRaiders.available=true`: public beta downloadable separately.
- `elevenCup.available=false`: in development.

When a new Dojo Raiders version is released, the client installed on your PC will display **Atualizar / Update** and cannot be launched through the launcher before updating. No need to reinstall every game.

Current initial versions: **Launcher v0.2.2** and **Dojo Raiders Client v0.1.0**.

## Release files and security

Dojo Raiders game ZIP: [Dojo Raiders Client v0.1.0](https://github.com/Venturinii/vencade-downloads/releases/tag/dojo-raiders-client-v0.1.0)

Game ZIP SHA-256: `800ab97cda7c7a0d9b1de022bb98e35a5a2b51737185d8b3ea92ef98df50c4eb`

Launcher installer SHA-256: `fc25a6f280e822f9a00771f276d989acbcc72f48012527cdccef72e5dbe93493`

The public repo contains only release binaries, manifests and documentation — no private source code, Twitch secrets, signing keys, personal access tokens or MongoDB data.

© Vencade Studios. All rights reserved.
