# Changelog

**English** · [Español (México)](es/CHANGELOG.md)

Every RelayPad release that reaches the public
[RelayPad releases](https://github.com/ElegantCatterpillar/RelayPad/releases) repository.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and versions
follow [Semantic Versioning](https://semver.org/) (while RelayPad is 0.x, a minor version may
change behavior).

Each version's section is also the body of its GitHub release, so it is written for players,
not for developers.

## [0.3.0] - 2026-11-19

The editor and NFC release: profiles you name yourself, NFC and amiibo on the Switch 2 Pro
Controller, the right Joy-Con 2 and the Switch Pro Controller, and a battery reading that is
the same everywhere you see it.

### Added

#### NFC on Switch 2 controllers

- **The Switch 2 Pro Controller reads and writes NFC,** over Bluetooth and over a USB cable,
  in the same NFC screen.
- **The right Joy-Con 2 does too,** on its own or joined with a left one: hold the tag over
  its right stick. The left Joy-Con 2 has no NFC reader, and the NFC screen says so.
- **Back up your own amiibo** and write that backup on a blank NTAG215, sealed like an
  original, with your own keys file. See [Back up your amiibo](amiibo-backup.md).

#### NFC (Switch Pro Controller, Switch 1)

- **NFC screen,** opened from a button on the main screen. The button is enabled when the
  connected controller has an NFC reader; otherwise it tells you why not.
- **Read amiibo and tags:** tap one on the controller to see what it is and, for an amiibo,
  the character's name.
- **Tap one after another:** the reader keeps going after each read, and a history lists
  everything you read, with export to CSV.
- **Write on blank NTAG tags:** a short text, or the ID of an amiibo
  you read earlier. RelayPad shows that text or character when it reads the tag again. The tag
  is not an amiibo: a Switch or a game will not recognize it.
- **Your tags are safe:** RelayPad refuses to write over an amiibo, a locked tag or a tag it
  cannot write safely, and it never locks a tag.
- **Works over Bluetooth.** With the cable plugged in, the controller also needs its Bluetooth
  connection to this PC; the screen tells you what to connect.

#### Controller editor

- **Named profiles per controller type,** with a redesigned profile menu and a controller
  picker in the header. Profiles saved by 0.2.0 open in a read-only view.
- **Sticks:** interactive deadzones on a live view of the stick, a response-curve preview,
  and X and Y inversion for each stick separately.
- **Buttons:** a compact layout next to a picture of the physical controller.
- **Turbo** and **Macros** tabs, each with a short guide on how to create one.
- **Output:** a clearer layout with help text, and **rumble preview**: try unsaved rumble
  settings on the controller you choose before saving.
- Tooltips on every editor tab.

#### Main screen and status

- **Four players, down from eight:** one controller per player, as on a console. A fifth
  controller stays connected and waits for a free player.
- Joy-Con 2 join with a gesture.
- **Disconnect** button for a connected controller.
- **Bluetooth listening switch:** stop RelayPad from looking for Bluetooth controllers while
  you do not need it.
- **Activity log** button on the main screen; pressing it again closes the window.
- **Waiting screen pairing steps per controller,** with Joy-Con 2 cards and a guide that lists
  the USB and Bluetooth steps of each model.
- Home and back buttons in the top bar replace the back button of each view.

#### Install and setup

- **First-run setup offers HidHide** next to ViGEmBus and says what each one is for. ViGEmBus is
  required; HidHide is recommended, so games see only the virtual pad and never read a press
  twice. Both install from their official, checksum-verified releases.
- **Uninstalling RelayPad shows any controller it left hidden** and removes RelayPad from
  HidHide's allowed programs. HidHide itself stays installed, and updates keep the setup as it is.
- **The uninstaller says what it removes:** the app, its shortcuts and its start-with-Windows
  entry; the drivers stay. Its "Delete the application data" box also deletes settings, logs,
  profiles and amiibo backups and keys kept in RelayPad's own folders.
- The installer and uninstaller are in Spanish when Windows is.

#### Other

- The Switch Pro Controller's player LEDs are corrected when they do not match its player.
- Every warning the app shows is translated (English and Spanish).
- Activity log entries keep the name of their controller after it disconnects.
- Optional diagnostic reports also record Bluetooth connection times.
- **License:** RelayPad is free for personal use. The license and the third-party notices come
  with the installer and are linked from About.
- **Report on GitHub:** after a crash, the next start offers to report it; the errors log has
  the button too, for the whole log or for one line. It opens a prefilled issue with the
  diagnostics report, with serial numbers and Bluetooth addresses hidden.
- **Controllers in the tray menu:** click a controller to open RelayPad on it, or its gear to
  open its settings.
- **Support RelayPad** in About opens the support page. Support is optional and unlocks
  nothing.

### Changed

- **Battery:** the percent is worked out once for each controller, so the tray and every line
  of the activity log show the same number.
- **Updates** come from the renamed public repository `ElegantCatterpillar/RelayPad`. If 0.2.0
  does not offer this update on its own, download the installer from Releases once; later
  versions update from the new name.
- **Settings → Drivers** lists only the drivers you can install today (ViGEmBus and HidHide).
- NFC moved out of the profile editor into its own view, because it belongs to the controller,
  not to a profile.
- The Appearance tab is gone from the editor.
- Each release lists the installer's SHA-256 and a link to its VirusTotal scan.

### Fixed

- A full battery reads 100 % while charging, instead of sticking at 99 % or flapping every
  second.
- The player slot strip no longer flashes "pending" while a connected controller looks for its
  other link (USB or Bluetooth) in the background.
- Starting NFC with only the cable connected no longer disconnects the Switch Pro Controller.

## [0.2.0] - 2026-10-21

The first public build, for friends: a Windows installer with automatic updates. Updates are
signed and the app checks that signature before installing one; the installer itself is not
code-signed yet.

### Added

- **Controllers:** Nintendo Switch 2 Pro Controller over Bluetooth LE and USB; Nintendo Switch
  Pro Controller (Switch 1) over USB and Bluetooth; Joy-Con 2 over Bluetooth LE, single
  (sideways) or a left and a right joined into one pad.
- **Virtual pads:** Xbox 360 or DualShock 4 through ViGEmBus, one per controller, up to eight
  controllers at once, each on a stable player slot. Players past the fourth Xbox user become a
  DualShock 4.
- **USB and Bluetooth handoff:** plugging in or unplugging the cable keeps the same virtual pad.
  Plugging a Switch 2 Pro Controller in over USB also pairs it, so Bluetooth reconnects later
  without the sync button.
- **Profiles (`.repad`):** button remapping, deadzones and response curves, turbo, macros, gyro
  aim and gyro mouse, rumble and player LEDs, with import and export. Stick calibration is
  stored per controller.
- **Tray app:** status with battery, player LEDs, nickname, identify (buzz), live stick values
  and a diagnostics window; tray popup, notifications and start with Windows.
- **Player position:** move a controller to a free player or swap it with the one there.
- **Drivers page:** install, check and remove ViGEmBus and HidHide. HidHide hides the real
  controller so games only see the virtual pad.
- **Switch 1 Pro pairing:** the status view opens Windows "Add device" and shows the sync
  button steps.
- **Joy-Con 2:** join and separate from the status view; joined pairs are remembered and
  rejoined.
- **Battery** percent from curves fitted to measured discharges for each model.
- **Activity log** split into events, power and errors, each in its own tab, tagged and
  filterable per controller.
- **Diagnostic reports:** optional and local only, asked for on first run.
- **Language:** English and Spanish, chosen from the top bar.
- **Automatic updates** from the public releases repository, installed when no controller is
  in use.
