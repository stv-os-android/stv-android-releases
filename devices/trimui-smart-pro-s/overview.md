<p align="right"><b>English</b> · <a href="overview.es.md">Español</a></p>

[STV OS](../../README.md) › [TrimUI Smart Pro S](README.md) › **Overview**

**Overview** · [Releases](releases.md) · [Manual](manual.md)

# Overview

## What STV OS is

STV OS is an Android 13 system made for the TrimUI Smart Pro S. It starts from the Android of a
board with the same chip (Allwinner A523) and rebuilds what the console needs: its own Linux kernel,
a system trimmed to fit in 1 GB of RAM, its own apps for everything the console does outside a game,
and a PSP emulator tuned for this hardware.

It installs in one of two ways, and both are maintained:

- **On a microSD card.** The card is the system disk. The internal memory is not touched: without
  the card, the console starts its factory firmware as before.
- **On the internal memory.** STV OS replaces the factory firmware. It starts faster, and the
  microSD becomes a plain FAT32 card for games and saves.

## The goal: PSP

The PSP is the most demanding system this console can run well, and it is the reason for the
project. The work is measured scene by scene in the heaviest games, with the same build and the
same settings, before and after each change.

| Game and scene | Before | With STV OS | Conditions |
|---|---|---|---|
| *Dante's Inferno*, a fight with nine characters | 58-69 % of full speed | **99.5 %** | same resolution and image, no overclock |
| *God of War: Ghost of Sparta*, the fight with Callisto | about 56 % | **60 fps** | 2× PSP resolution |
| *God of War: Ghost of Sparta*, a fight with several enemies | 46.4 fps | **59.5 fps** (median) | 1271×720, the screen at 1:1 |

These results come from **PPSSPP - STV**, a version of PPSSPP adjusted for the console's GPU (Mali-G57)
and memory: cheaper shadows, fewer wasted draws, texture copies limited to what is used, and a
graphics thread that no longer waits on locks. The official PPSSPP is also installed, as an
alternative.

## What else changes

- **Kernel.** Display, power, battery and temperature drivers adjusted for this console: real
  60 Hz, the panel fully off while sleeping, a battery percentage that does not drop right after
  charging, and the fan driven by the chip's small RISC-V core.
- **Memory.** Android without the parts a handheld does not use (SystemUI among them), so that
  games have more of the 1 GB.
- **STV apps.** A control center (HOME button), an open-apps view (MENU button), notices, a lock
  screen with the gamepad, the volume indicator and screenshots: everything the console does
  outside a game, designed for the gamepad.
- **Games menu.** Pegasus with the STV theme. *Manage Systems* adds systems, installs emulator
  cores, finds box art without a computer and backs up the saves of all emulators in one file.
- **Other systems.** RetroArch for GBA, PS1, NES, SNES, Game Boy, Neo Geo and more;
  Mupen64Plus FZ for Nintendo 64.
- **Updates.** Signed packages installed from the console, with a way back to the previous
  version.

## Status

This is a **beta**. It has been used daily for weeks on one console. Things to know before
installing:

- It is not an official TrimUI system. On the internal memory, it replaces the factory firmware
  (TrimUI's official firmware file, installed the same way, is the way back).
- The system is signed with Android's public test keys and SELinux runs in permissive mode.
  Install apps only from sources you trust.
- STV OS does not include games or BIOS files.
