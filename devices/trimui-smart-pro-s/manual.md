<p align="right"><b>English</b> · <a href="manual.es.md">Español</a></p>

[STV OS](../../README.md) › [TrimUI Smart Pro S](README.md) › **Manual**

[Overview](overview.md) · [Releases](releases.md) · **Manual**

# Manual

Everything STV OS adds to the console, screen by screen. It applies to version **0.0.1-beta** and to
both installations (internal memory and microSD); where they differ, it says so.

- [Buttons and shortcuts](#buttons-and-shortcuts)
- [The home screen](#the-home-screen)
- [Control center (HOME)](#control-center-home)
- [Open apps (MENU)](#open-apps-menu)
- [Notices](#notices)
- [Lock screen](#lock-screen)
- [STV Settings](#stv-settings)
- [Manage Systems](#manage-systems)
- [Emulators](#emulators)
- [Games and the Roms folder](#games-and-the-roms-folder)
- [Saves](#saves)
- [Updates](#updates)
- [Problems and answers](#problems-and-answers)

## Buttons and shortcuts

These work everywhere, also inside a game:

| Button | What it does |
|---|---|
| **HOME** (top button) | Opens and closes the [control center](#control-center-home) |
| **MENU** | Opens and closes [open apps](#open-apps-menu): switch between apps or close them |
| **Volume + / −** | Changes the volume with the STV indicator; holding the button keeps changing it |
| **POWER**, short press | Turns the screen off and puts the console to sleep; press again to wake it |
| **POWER**, 20 seconds | Forces the console off (only if it does not respond) |
| **L1 + R1** together | Unlocks the [lock screen](#lock-screen) |
| **FN switch** | Does what is chosen in [STV Settings › FN switch](#stv-settings): pointer mode (default), high performance for PSP, silence, lock HOME and MENU while playing, or nothing |

And inside each emulator:

| Emulator | Its menu | Other |
|---|---|---|
| PSP (PPSSPP - STV) | **L2** (pause menu) | **R2**: fast-forward. The buttons follow the position of the PSP's: Cross bottom, Circle right, Square left, Triangle top |
| Nintendo 64 (Mupen64Plus FZ) | **START + SELECT** | Use *Exit* in that menu to leave a game: that is when the saves are copied to the card |
| Everything else (RetroArch) | **START + SELECT** | Bezel and screen filter per system, already set up |

![Volume indicator](images/en/volume.png)

## The home screen

The console starts in **Pegasus** with the STV theme: one screen per system, and the box art of
each game.

![Home screen](images/en/home.png)

| Button | What it does |
|---|---|
| **L1 / R1** | Previous / next system |
| **D-pad** | Moves between games |
| **A** | Plays the game with its default emulator |
| **X** | Options of the game (below) |
| **Y** | Search by name |
| **START** | Refreshes the library (after adding or removing games) |
| **SELECT** | Pegasus menu (its own settings, help, quit) |

**X, options of the game:** choose the emulator to open it with (for PSP, *PPSSPP - STV*, tuned
for this console and the default, or the official *PPSSPP*), switch the system view between grid
and list, or delete the game and its artwork from the console.

![Game options](images/en/game-options.png)

The **Android** system lists the installed apps: *Manage Systems*, *STV Settings*, the emulators,
the Aurora Store and any app you install.

![Android apps](images/en/android-apps.png)

## Control center (HOME)

**HOME** opens a panel on the right, over whatever is on screen, also in a game.

![Control center](images/en/control-center-display.png)

| Row | What it does |
|---|---|
| **Wi-Fi**, **Bluetooth** | Turn the radio on or off |
| **Pointer** | Mouse mode: the right stick moves a cursor and the left one scrolls (for apps made for touch) |
| **Stick LEDs** | Turns the rings around the sticks on or off |
| **Cooler** | Fan: *auto* (the default), *low*, *medium*, *max* or *off* |
| **CPU** | Performance profile: *powersave*, *normal*, *high*, *high · psp* (the default) or *max* |
| **GPU** | Graphics profile, same idea |
| **Brightness** | Left and right adjust it |

Under the profiles, the current CPU and GPU clocks. **A** changes the selected row, **B** closes the
panel, **X** takes a screenshot (saved in `Pictures/Screenshots`) and **START** opens the
[notices](#notices).

**Y** on the CPU or GPU row opens the **performance monitor**: the clock of each core over the last
15 minutes, next to the cap of the current profile. Left and right expand one core.

![Performance monitor](images/en/performance-graph.png)

## Open apps (MENU)

**MENU** lists the open apps and what each one is doing (playing, in use, in the background).

![Open apps](images/en/open-apps.png)

**A** opens the selected app, **X** closes it, **Y** goes to the home screen, **B** returns and
**SELECT** restarts Pegasus. The free memory is shown at the top.

## Notices

Low battery, high temperature, a USB cable connected, a screenshot saved, or notifications from
apps. **START** in the control center opens them: **A** opens one, **X** dismisses it and **Y**
clears them all. With *Vibration on alerts* enabled, the console vibrates once for each new notice.

![Notices](images/en/notices.png)

## Lock screen

When it wakes up, the console shows the clock, the date and the battery. **L1 + R1** at the same
time unlock it.

![Lock screen](images/en/lock-screen.png)

It is chosen in **STV Settings › Security**: *None*, *L1 + R1* (the default) or a *PIN* of 4 to 16
digits, typed with the gamepad (D-pad moves, A types, B deletes, START confirms).

## STV Settings

The console's own settings app, made for the gamepad: **A** chooses, **B** goes back, left and right
adjust.

![STV Settings](images/en/settings.png)

| Section | What is there |
|---|---|
| **USB transfer** | Turns the console into a drive for a computer, to copy games. While it is active the console cannot be used |
| **Display** | Brightness, screen timeout, color temperature, text size and theme (light or dark; it changes Android, the STV apps and Pegasus together) |
| **Sound and vibration** | Vibration on button press and on notices, headphone gain and the microphone for games |
| **Wi-Fi** | Android's Wi-Fi screen |
| **Stick LEDs** | Color and brightness of each ring, with a custom RGB color |
| **Pointer (mouse mode)** | On or off, and the cursor speed |
| **FN switch** | What the FN switch does when set to on |
| **Security** | The [lock screen](#lock-screen) |
| **Developer** | USB debugging (adb) and root access. **Off** on a clean install: turn them on only if you need them |
| **Storage** | Space used on the internal memory and on the ROM card, and, in the microSD installation, *Expand to the whole card* |
| **System** | Restart, power off, and the full Android settings (Bluetooth pairing, keyboard, app permissions) |
| **System language** | Android's language list. STV OS is in English and Spanish; the STV apps and Pegasus follow it |
| **Date and time** | Time zone: *Coordinated Universal Time (UTC)* or a region and a city. The time sets itself over Wi-Fi |
| **System update** | Install a new version, or go back to the previous one ([updates](#updates)) |
| **Support the project** | A QR code to the support page |
| **About this console** | Version, kernel, memory, storage, installation type and the [licenses](#problems-and-answers) of the third-party software |

<table>
<tr><td><img src="images/en/settings-display.png" alt="Display"></td><td><img src="images/en/settings-sound.png" alt="Sound and vibration"></td></tr>
<tr><td><img src="images/en/settings-leds.png" alt="Stick LEDs"></td><td><img src="images/en/settings-fn-switch.png" alt="FN switch"></td></tr>
<tr><td><img src="images/en/settings-developer.png" alt="Developer"></td><td><img src="images/en/settings-storage.png" alt="Storage"></td></tr>
<tr><td><img src="images/en/settings-date-time.png" alt="Date and time"></td><td><img src="images/en/settings-about.png" alt="About this console"></td></tr>
</table>

## Manage Systems

*Manage Systems* (in the Android system of the home screen) does without a computer what otherwise
needs one: add systems, install emulator cores, find box art and back up saves.

![Manage Systems](images/en/systems.png)

- **A on a system** lists its games, with a dot on those that already have box art and details.
  *Get what is missing* looks them up online (it needs Wi-Fi and takes a few seconds per game);
  *Get everything again* repeats it for all.
- **Y inside a system** shows its emulator core: which one is in use, and *Update core* to download
  the latest one.
- **START** opens the catalog of systems: choosing one creates its `Roms/<system>` folder, sets up
  its emulator and, if needed, downloads the core.
- **Y on the list** opens [saves](#saves): *Back up* and *Restore*.

<table>
<tr><td><img src="images/en/systems-psp.png" alt="A system and its games"></td><td><img src="images/en/systems-new.png" alt="New system"></td></tr>
<tr><td><img src="images/en/systems-core.png" alt="Emulator core"></td><td><img src="images/en/systems-saves.png" alt="Saves"></td></tr>
</table>

## Emulators

| System | Emulator | Notes |
|---|---|---|
| PSP | **PPSSPP - STV** (default) and the official PPSSPP | Tuned for this console. Extra resolutions *2.25x PSP (STV)* and *Panel 1:1 (STV)* in Graphics › Rendering resolution. Settings can be saved per game |
| Nintendo 64 | Mupen64Plus FZ | GLideN64, the fastest renderer on this console |
| PlayStation | RetroArch (PCSX-ReARMed) | Works without a BIOS file for most games (STV OS does not include BIOS files) |
| Game Boy Advance | RetroArch (mGBA) | |
| Game Boy, Game Boy Color, NES, SNES | RetroArch (Gambatte, FCEUmm, Snes9x 2010) | Included: they work without Wi-Fi |
| Neo Geo, arcade, CPS-1, CPS-2 | RetroArch (FinalBurn Neo) | **Not included** (its license allows only non-commercial use): the first time you open one of these games, *Manage Systems* offers *Install core* (needs Wi-Fi, about 70 MB) |
| Others | RetroArch | Added from the catalog in *Manage Systems* |

The CPU profile **high · psp** (the default) is the one tuned for PSP. *max* raises the limits
further, with more heat and battery use.

## Games and the Roms folder

Games live in a `Roms` folder, with one subfolder per system named in lower case: `Roms/psp`,
`Roms/n64`, `Roms/gba`, `Roms/ps1`, `Roms/neogeo`, `Roms/nes`, `Roms/snes`…

- **Internal memory installation:** `Roms` is at the root of the **microSD card** (FAT32). Copy the
  games with a card reader, or over USB (*USB transfer* shows the card as a second drive). The card
  can be inserted and removed with the console on: the library updates by itself.
- **microSD installation:** `Roms` is in the console's **internal storage** (inside the card). Copy
  the games with **STV Settings › USB transfer**.

Rules: the games go directly inside the system folder (not in subfolders), and their file names
cannot have more than three dots, counting the extension. *Manage Systems* creates the folders and
the `metadata.pegasus.txt` file that describes each system; after copying games, **START** on the
home screen refreshes the library.

## Saves

| Emulator | Internal memory installation | microSD installation |
|---|---|---|
| PSP | On the card: `Android/data/org.ppsspp.ppsspp.stv/files/PSP/` | Internal storage, same path |
| RetroArch | On the card: `Android/data/com.retroarch.aarch64/files/` | Internal storage: `RetroArch/saves` and `RetroArch/states` |
| Nintendo 64 | On the card: `STV/saves/n64/` | Internal storage: `M64Plus/GameData/` |

**Back up:** *Manage Systems* › **Y** › *Back up* puts the saves of the three emulators in one file,
`STV/backups/saves-<date>.zip` (on the card in the internal memory installation). Copy it to a
computer: reinstalling erases the internal storage. **Restore** lists the backups and can keep a
copy of the current saves before restoring.

In the internal memory installation the saves live on the card: without a card the emulators cannot
save, and the console warns about it. Do not remove the card while a game is open.

## Updates

1. Copy the update package (`STV-TSPS-update-<build>.zip`) to the `STV/update` or `Download`
   folder of the internal storage, or, in the internal memory installation, to `STV/update` on the
   card.
2. **STV Settings › System update** finds it, shows its notes and asks to confirm. It prepares the
   update in about two minutes while the console stays usable, then restarts and installs it in 3 to
   4 minutes. Do not turn it off.
3. Games, saves, apps and settings stay. The previous version is kept: **Go back to <build>** returns
   to it.

It needs 40 % battery or the charger. A package made for the other installation type is rejected
before writing anything, and only signed packages are accepted.

## Problems and answers

**The console does not start.** microSD installation: without the card it starts the factory
firmware, so the problem is the card; write it again (this erases what is on it). Internal memory
installation: install again with the `trimui_tg5050.awimg` file and Volume − + POWER; the data on
the internal memory is erased, games and saves on the card stay.

**The screen stays black after a system restart.** Press POWER once to turn it off and again to turn
it on.

**Both stick rings turned red.** The internal storage switched to read-only after a file system
error (for example after a power cut): nothing is being saved. Turn the console off from **STV
Settings › System › Power off** and on again; it checks and repairs the storage while starting.

**I forgot the PIN.** There is no way to recover it from the console.

**A game does not appear.** Check that it is directly in `Roms/<system>/`, that the system folder
has its `metadata.pegasus.txt` (created by *Manage Systems*), that the extension is listed in it,
and that the name has no more than three dots. Then press **START** on the home screen.

**Opening a Neo Geo or arcade game shows the core screen.** FinalBurn Neo is not included: press A on
*Install core* (with Wi-Fi) and then B to go back; the game opens.

**Licenses.** **STV Settings › About this console › Licenses** lists every third-party component,
its license, its source and whether STV OS modified it. STV OS is free and is not sold; it does not
include games or BIOS files.
