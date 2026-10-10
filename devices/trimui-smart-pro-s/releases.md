<p align="right"><b>English</b> · <a href="releases.es.md">Español</a></p>

[STV OS](../../README.md) › [TrimUI Smart Pro S](README.md) · [Overview](overview.md) · **Download and install** · [Manual](manual.md)

# Download and install

- [Which installation to choose](#which-installation-to-choose)
- [Install on the internal memory](#install-on-the-internal-memory)
- [Install on a microSD card](#install-on-a-microsd-card)
- [After installing](#after-installing)
- [Available versions](#available-versions)
- [Known issues](#known-issues)
- [Verify a download](#verify-a-download)

## Which installation to choose

| | Internal memory | microSD card |
|---|---|---|
| Factory firmware | Replaced (TrimUI's official file brings it back) | Untouched: without the card, the console starts it as before |
| The microSD card | A FAT32 card for games and saves, readable on any computer | The system disk, with games and saves inside |
| Start-up time | About 1 minute | 1 to 4 minutes, depending on the card |
| Space for apps and data | About 5.5 GB | The whole card, after *Expand to the whole card* |
| Install with | A file on a FAT32 card and a button combination | Raspberry Pi Imager on a computer |

If in doubt, start with the microSD card: the console does not change, and you can move to the internal
memory later.

## Install on the internal memory

This replaces the factory firmware.

> [!WARNING]
> **The console's internal data is erased**, including the apps and saves of the factory firmware
> (*Apps/ports*). Games and saves on the microSD card are not touched.

**Requirements:** a microSD card formatted as FAT32 with 1.5 GB free (it can be your games card) and the
console's charger.

> [!WARNING]
> **Do not use a card that was an STV OS system card (microSD installation).** If the card has a boot
> area, the console starts from it, and formatting does not remove it. Use another card, or erase it
> completely first (for example, with *SD Card Formatter* and its *Overwrite format* option).

> [!NOTE]
> Cards of 64 GB or more usually come formatted as exFAT. Reformat them as FAT32: on macOS, with Disk
> Utility (*MS-DOS (FAT)*); on Windows, cards over 32 GB need a third-party FAT32 formatting tool.

1. Download `stv-os-<version>-trimui-smart-pro-s-internal-memory.zip` from
   [Available versions](#available-versions) and unzip it. It contains `trimui_tg5050.awimg` (about
   1.3 GB). **Do not rename it**: the console looks for that exact name.
2. Copy `trimui_tg5050.awimg` to the root of the card, not inside a folder.
3. Turn the console fully off. If unsure, hold POWER for 20 seconds.
4. Insert the card and connect the charger.
5. Hold Volume −. Without releasing it, press POWER for 3 seconds. Release POWER, but **keep holding
   Volume −** until a green progress bar appears. Then release Volume −.
6. Wait. When the bar finishes, the console restarts by itself and starts STV OS. The first start takes a
   few minutes longer.
7. Delete `trimui_tg5050.awimg` from the card.

If the console starts normally without showing the bar, it did not detect the combination. Turn it off and
repeat from step 3, holding Volume − until you see the bar.

**Going back to the factory firmware:** use TrimUI's official `trimui_tg5050.awimg` (firmware v1.0.1) and
repeat steps 2 to 7.

## Install on a microSD card

The card becomes the console's system disk. The internal memory is not touched.

**Requirements:** a microSD card of 16 GB or more (everything on it is erased) and a computer with
[Raspberry Pi Imager](https://www.raspberrypi.com/software/). A fast card (A1/A2 or U3) shortens the first
start.

1. Download `stv-os-<version>-trimui-smart-pro-s-microsd.img.xz` from
   [Available versions](#available-versions). There is no need to uncompress it.
2. Open Raspberry Pi Imager. Under *Operating System*, choose **Use custom** (at the end of the list) and
   select the downloaded file.
3. Under *Storage*, choose the microSD card. Check its size so you do not choose another disk.
4. If it offers OS customisation, skip it. Confirm and wait while it writes and verifies.
5. If the computer then says it cannot read the disk, close the message without formatting: **Ignore** or
   **Eject** on macOS, **Cancel** on Windows.
6. Insert the card in the console and turn it on.

> [!WARNING]
> The **first start** prepares the apps and installs the emulators. On a slow card it can take more than
> 10 minutes, with a black screen for several of them. Do not turn the console off.

> [!TIP]
> To use the whole card, open **STV Settings › Storage › Expand to the whole card** and restart.

**Going back to the factory firmware:** turn the console off and remove the card.

## After installing

- The console starts in English and in UTC. Change them in **STV Settings › System language** and
  **STV Settings › Date and time**.
- Connect to a Wi-Fi network in **STV Settings › Wi-Fi**. The clock sets itself, and *Manage Systems* can
  download emulator cores and box art.
- USB debugging and root access are off. Turn them on in **STV Settings › Developer** only if you need them.
- Copy your games to `Roms/<system>/` (for example, `Roms/psp/`):
  - **Internal memory installation:** at the root of the microSD card.
  - **microSD installation:** in the console's internal storage.

  The [manual](manual.md#games-and-the-roms-folder) explains how.

## Available versions

### 0.0.1-beta · 2026-10-10

First public release. [Release notes](https://github.com/stv-os-android/stv-android-releases/releases/tag/trimui-smart-pro-s-v0.0.1-beta).

| File | Contents | Size |
|---|---|---|
| [stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip) | Install on the internal memory | 974 MB |
| [stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-trimui-smart-pro-s-microsd.img.xz) | Install on a microSD card | 845 MB |
| [stv-os-0.0.1-beta-gpl-source.tar](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/stv-os-0.0.1-beta-gpl-source.tar) | GPL source code: the kernel of this version, with its patches and configuration, and the other GPL source | 206 MB |
| [NOTICE.txt](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/NOTICE.txt) | Third-party components and licenses | |
| [SHA256SUMS](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS) · [SHA256SUMS.sig](https://github.com/stv-os-android/stv-android-releases/releases/download/trimui-smart-pro-s-v0.0.1-beta/SHA256SUMS.sig) | Checksums and their signature | |

From the next version on, each release will also include update packages, which install from the console
without losing data. The [manual](manual.md#updates) explains how.

## Known issues

- Tested on one console; other production batches may behave differently.
- microSD cards formatted as exFAT have not been tested with the internal memory installation: use FAT32.
- Going back to the factory firmware with TrimUI's official file has not been tested end to end with STV OS
  installed.
- The system is signed with Android's public test keys and SELinux runs in permissive mode. Install apps
  only from sources you trust.
- balenaEtcher 2.1.7 does not list any disk on macOS 26: use Raspberry Pi Imager.

## Verify a download

Each release publishes `SHA256SUMS`, signed with the key in [`keys/`](../../keys/).

On macOS and Linux:

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

On Windows (PowerShell), compute the checksum and compare it with the file's line in `SHA256SUMS`:

```powershell
Get-FileHash .\stv-os-0.0.1-beta-trimui-smart-pro-s-internal-memory.zip -Algorithm SHA256
```

To check the signature, use OpenSSL 3:

```bash
openssl pkeyutl -verify -pubin -inkey stv-release-ed25519.pub.pem -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig
```

The `openssl` that ships with macOS cannot check Ed25519 signatures; the Homebrew one can.
