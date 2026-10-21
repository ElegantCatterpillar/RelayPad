# RelayPad

<p align="center">
  <img src="media/app-icon.png" alt="RelayPad icon" width="128" height="128" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="media/lockup-dark.svg" />
    <img src="media/lockup-light.svg" alt="RelayPad" height="32" />
  </picture>
</p>

RelayPad is a Windows tray app that turns Nintendo controllers into a virtual Xbox 360
or DualShock 4 gamepad, so PC games see a normal controller.

This repository holds **public releases only** (installers and update manifests). The
source code lives in a separate private repository. A product website is planned; until
then, this README is the place to learn what RelayPad does and how to install it.

**Not affiliated with Nintendo, Microsoft, or Sony.** All trademarks belong to their owners.

<p align="center">
  <img src="media/switch2-pro-front.svg" alt="Nintendo Switch 2 Pro Controller (status art)" width="480" />
</p>

## What it does

- Connects a supported Nintendo controller over **Bluetooth** or **USB**
- Presents it to games as an **Xbox 360** or **DualShock 4** pad (via ViGEmBus)
- Keeps the same virtual pad when you plug in or unplug USB (handoff)
- Profiles for remapping, stick deadzones and response, rumble, motion, and more
- Tray app with status, battery, identify (buzz), diagnostics, and settings
- Optional **HidHide** so games only see the virtual pad, not the real controller
- **Automatic updates** from this repository once you have installed a signed build

## Controllers today

| Controller | Status |
| --- | --- |
| Nintendo Switch 2 Pro Controller | Supported (Bluetooth LE and USB) |
| Nintendo Switch Pro Controller (Switch 1) | Supported (Bluetooth and USB) |
| Joy-Con 2 (single / pair) | In progress — not the focus of early friend builds |
| Switch 1 Joy-Con | Planned |

## Requirements

- **Windows 10 or 11** (x64)
- A **Bluetooth** adapter for wireless use, or a **USB** cable
- **[ViGEmBus](https://github.com/nefarius/ViGEmBus)** — RelayPad can install the pinned
  build from **Settings → Drivers**
- **[HidHide](https://github.com/nefarius/HidHide)** — optional; same Drivers page

WebView2 is used by the desktop shell (usually already on Windows 11).

## Install

1. Open the latest [Release](https://github.com/ElegantCatterpillar/RelayPad/releases/latest).
2. Download the Windows installer (NSIS `.exe`) and run it.
3. Start **RelayPad** from the Start menu (it also lives in the system tray).
4. Open **Settings → Drivers** and install **ViGEmBus** if the app asks for it.
5. Connect your controller (USB cable, or sync / pair over Bluetooth as the status
   screen describes for your model).

To remove RelayPad, use **Apps → Installed apps** in Windows settings (the installer
registers an uninstaller). Drivers you installed from Settings are separate and can be
removed from the same Drivers page.

## Updates

Builds published here are signed for the in-app updater.

- With **Install updates automatically** on (default), RelayPad checks every few hours
  and installs when no controller is in use.
- With it off, About → **Check for updates** only notifies you.
- You can always download a newer installer from [Releases](https://github.com/ElegantCatterpillar/RelayPad/releases).

## Privacy

RelayPad can keep an **optional**, local diagnostic report (opt-in on first run) to help
track connection and battery issues. Reports stay on your PC unless you choose to share
them. Nothing is uploaded without that consent.

## Feedback

For early friend builds, open an [issue](https://github.com/ElegantCatterpillar/RelayPad/issues)
on this repository. Say which controller, Windows version, and whether you used USB or
Bluetooth. If something fails, the Activity log in the app (and the log files under
`%LOCALAPPDATA%\dev.relaypad.tray\logs\`) help a lot.

## License

RelayPad is **freeware** (not open source): free for personal, non-commercial use.
You may not sell it, modify it, or redistribute builds without permission. See
[LICENSE](LICENSE) for the full terms.

Rust dependency license texts: [THIRD_PARTY_LICENSES](THIRD_PARTY_LICENSES).
ViGEmBus and HidHide (optional, from Drivers) keep their own licenses. Protocol
research used as reference only (reimplemented): ndeadly/switch2_controller_research,
SDL (`SDL_hidapi_switch2.c`), switch2controllerpc.

## Website

A dedicated product page is planned. This README will feed that page so the story stays
the same in the installer repo and on the site.

## Disclaimer

RelayPad is an independent project. It is not affiliated with, endorsed by, or sponsored
by Nintendo, Microsoft, or Sony. Nintendo Switch is a trademark of Nintendo. Xbox is a
trademark of Microsoft. DualShock is a trademark of Sony Interactive Entertainment.
