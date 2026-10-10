<p align="right"><b>English</b> · <a href="overview.es.md">Español</a></p>

[STV OS](../../README.md) › [TrimUI Smart Pro S](README.md) · **Overview** · [Download and install](releases.md) · [Manual](manual.md)

# Overview

## What STV OS is

STV OS is a custom firmware based on Android 13, made for the TrimUI Smart Pro S. It starts from the Android
build for the Radxa Cubie A5E, a board with the same chip (Allwinner A523), and adds a custom Linux kernel,
its own apps for the console and a PSP emulator optimized for this console.

It installs on the internal memory or on a microSD card:
[which one to choose](releases.md#which-installation-to-choose).

## PSP performance

The PSP is the most demanding system this console runs well. Each change is measured scene by scene in the
heaviest games, with the same settings before and after.

| Game and scene | Before the STV changes | With STV OS | Resolution |
|---|---|---|---|
| *Dante's Inferno*, a fight with nine characters | 58–69% of full speed | **99.5%** | Same before and after |
| *God of War: Ghost of Sparta*, the fight with Callisto | 33.7 fps | **60 fps** | 2× PSP |
| *God of War: Ghost of Sparta*, a fight with several enemies | 46.4 fps | **59.5 fps** (median) | *Panel 1:1 (STV)* |

All results are without overclocking and without lowering resolution or quality. They come from
**PPSSPP - STV**, a version of PPSSPP optimized for the console's GPU (Mali-G57) and memory. The official
PPSSPP is also installed.

## What else changes

- **Kernel.** Display, power, battery and temperature drivers adjusted for this console: a true 60 Hz
  refresh rate, the screen fully off during sleep, a battery percentage that does not drop right after
  charging, and automatic fan control.
- **Memory.** Android without the parts a handheld does not need, so games get more of the 1 GB of RAM.
- **STV apps.** Android's interface is made for touch screens. STV OS replaces it with its own: control
  center (HOME), open apps (MENU), notices, lock screen, volume indicator and screenshots.
- **Games menu.** Pegasus with the STV theme. *Manage Systems* adds systems, installs emulator cores, finds
  box art and backs up saves, all from the console.
- **Other systems.** RetroArch for GBA, PS1, NES, SNES, Game Boy and more; Mupen64Plus FZ for Nintendo 64.
- **Updates.** Signed packages installed from the console, with a way back to the previous version.

## Status

**Beta**, tested on one console. It is not an official TrimUI system, and it does not include games or BIOS
files. Read the [known issues](releases.md#known-issues) before installing.

## Credits

STV OS is built on the work of these projects:

- **Radxa**: the Android 13 base for the Allwinner A523 (Cubie A5E).
- **Orange Pi**: the Linux 5.15 kernel tree for the A523.
- **KNULLI**: the bootloader of the microSD installation.
- **TrimUI**: the console, the bootloader of the internal memory installation and the controller service.
- **PPSSPP**, **RetroArch** and the **libretro** cores, **Mupen64Plus FZ**, **Pegasus Frontend**,
  **Aurora Store** and **LeanKeyboard**.
- The **IBM Plex** fonts.

The full list, with each license, is in `NOTICE.txt` and in **STV Settings › About this console › Licenses**.
