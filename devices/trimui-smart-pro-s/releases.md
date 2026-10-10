<p align="right"><b>English</b> · <a href="releases.es.md">Español</a></p>

[STV OS](../../README.md) › [TrimUI Smart Pro S](README.md) › **Releases**

[Overview](overview.md) · **Releases** · [Manual](manual.md)

# Releases

- [Which installation to choose](#which-installation-to-choose)
- [Install on the internal memory](#install-on-the-internal-memory)
- [Install on a microSD card](#install-on-a-microsd-card)
- [After installing](#after-installing)
- [Available versions](#available-versions)
- [Verify a download](#verify-a-download)

## Which installation to choose

STV OS installs in one of two ways. Both are maintained and get the same versions.

| | Internal memory | microSD card |
|---|---|---|
| Factory firmware | Replaced (it comes back with TrimUI's official file) | Untouched: remove the card and the console starts it as before |
| The microSD card | A plain FAT32 card for games and saves, readable on any computer | It is the system disk (games and saves live inside it) |
| Start-up time | About 1 minute | 1 to 4 minutes, depending on the card |
| Space for apps and data | About 5.5 GB | The whole card |
| Install with | A file on a FAT32 card and a button combination | Raspberry Pi Imager on a computer |

If in doubt, start with the **microSD card**: nothing in the console changes, and moving to the
internal memory later is just another installation.

## Install on the internal memory

This replaces the factory firmware with the same mechanism TrimUI uses for its own updates. The
internal data partition is erased (on the factory firmware that includes *Apps/ports* and their
saves). Games and saves on the microSD card are not touched.

**You need:** a microSD card formatted as **FAT32** with 1.5 GB free (it can be the card you will
use for games), and the console's charger.

1. Download `stv-os-<version>-trimui-smart-pro-s-internal-memory.zip` from
   [Available versions](#available-versions) and unzip it. You get `trimui_tg5050.awimg`
   (about 1.3 GB). **Do not rename it**: the console only looks for that exact name.
2. Copy `trimui_tg5050.awimg` to the **root** of the card (not inside a folder).
3. Turn the console **fully off**. If unsure, hold POWER for 20 seconds.
4. Insert the card and **connect the charger**.
5. Hold **Volume −**. Without releasing it, press **POWER for 3 seconds**. Release POWER but
   **keep Volume − pressed** until a **green progress bar** appears. Then release Volume −.
6. Wait. When the bar ends, the console **restarts by itself** and starts STV OS. The first start
   takes a few minutes longer than the next ones.
7. Delete `trimui_tg5050.awimg` from the card, or move it into a folder. A normal start does not
   install it again, but it is safer not to leave it at the root.

If no bar appears and the console starts normally, the combination was not caught: turn it off
and repeat from step 3, keeping Volume − pressed until you see the bar.

> **The card must not be an old STV OS microSD system card.** The console always starts from the
> card first when the card has a boot area, and formatting does not remove it. Use another card,
> or erase it completely first (for example with *SD Card Formatter* and its *Overwrite format*
> option).
>
> **Cards of 64 GB or more** usually come formatted as exFAT. Reformat them as FAT32 (on macOS:
> Disk Utility, *MS-DOS (FAT)*; on Windows, cards over 32 GB need a FAT32 formatting tool).
> exFAT has not been tested.

**Going back to the factory firmware:** put TrimUI's official `trimui_tg5050.awimg` (firmware
v1.0.1) at the root of the card and repeat the same steps. This is the manufacturer's own
procedure; with STV OS installed it has not been tested end to end yet.

## Install on a microSD card

The card becomes the console's system disk. The internal memory is not touched.

**You need:** a microSD card of **16 GB or more** (everything on it is erased) and a computer with
[Raspberry Pi Imager](https://www.raspberrypi.com/software/). A fast card (A1/A2 or U3) makes the
first start much shorter.

1. Download `stv-os-<version>-trimui-smart-pro-s-microsd.img.xz` from
   [Available versions](#available-versions). There is no need to uncompress it.
2. Open Raspberry Pi Imager. In the operating system choose **Use custom** (at the end of the list)
   and select the downloaded file.
3. In the storage, choose the microSD card. Check its size: do not choose another disk.
4. If it asks about *OS customisation*, answer **No**. Confirm, and wait while it writes and
   verifies.
5. If the computer then says it cannot read the disk, choose **Ignore** or **Eject**, never
   *Initialize* or *Format*.
6. Insert the card in the console and turn it on normally.

The **first start** prepares the apps and installs the emulators. On a slow card it can take more
than 10 minutes, with a black screen for several of them: wait without turning it off.

To use the whole card: **STV Settings › Storage › Expand to the whole card**, then restart.

**Going back to the factory firmware:** turn the console off and remove the card.

> balenaEtcher 2.1.7 does not list any disk on macOS 26; Raspberry Pi Imager works.

## After installing

- The console starts in **English** and in **UTC** time. Change them in **STV Settings › System
  language** and **STV Settings › Date and time**.
- Connect to Wi-Fi from **STV Settings › Wi-Fi**: the clock sets itself and *Manage Systems* can
  download emulator cores and box art.
- **USB debugging and root access are off.** Turn them on only if you need them, in **STV
  Settings › Developer**.
- Games go in `Roms/<system>/` (for example `Roms/psp/`): on the root of the card for the internal
  memory installation, and in the console's internal storage for the microSD installation. See
  the [manual](manual.md#games-and-the-roms-folder).

## Available versions

### 0.0.1-beta · 2026-10-10

First public release. Build f195 · kernel STV #122 (Linux 5.15.147).

| File | What it is | Size |
|---|---|---|
| [stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip) | Install on the internal memory | 974 MB |
| [stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz) | Install on a microSD card | 845 MB |
| [stv-os-0.0.1-beta-gpl-source.tar](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-gpl-source.tar) | **Kernel source code used by this version** (STV #122), its patches and config, and the other GPL source | 206 MB |
| [NOTICE.txt](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/NOTICE.txt) | Third-party software and licenses | |
| [SHA256SUMS](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS) · [SHA256SUMS.sig](https://github.com/littlewild47/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS.sig) | Checksums and their signature | |

**What's in it:** the system as described in the [overview](overview.md), with English and UTC as
factory settings, USB debugging and root access off on a clean install, and Wi-Fi in the worldwide
regulatory domain. Full release notes: [on GitHub](https://github.com/littlewild47/stv-android-releases/releases/tag/trimui-smart-pro-s-v0.0.1-beta).

**Updates:** from the next version on, each release also includes the update packages that install
from the console without losing data (STV Settings › System update). The manual explains how.

## Verify a download

Each release publishes `SHA256SUMS`, signed with the key in [`keys/`](../../keys/).

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

```bash
openssl pkeyutl -verify -pubin -inkey stv-release-ed25519.pub.pem -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

The second command needs OpenSSL 3 (the `openssl` that ships with macOS cannot check Ed25519
signatures; the Homebrew one can).
