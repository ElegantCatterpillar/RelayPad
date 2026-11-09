# Changelog

**English** · [Español (México)](es/CHANGELOG.md)

Every RelayPad release that reaches the public
[RelayPad releases](https://github.com/ElegantCatterpillar/RelayPad/releases) repository.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and versions
follow [Semantic Versioning](https://semver.org/) (while RelayPad is 0.x, a minor version may
change behavior).

Each version's section is also the body of its GitHub release, so it is written for players,
not for developers.

## [0.3.0] - Unreleased

The editor and NFC release: profiles are rebuilt around names you choose, the Switch 1 Pro
Controller reads and writes NFC tags, and battery readings agree everywhere they are shown.

### Added

#### NFC (Switch 1 Pro Controller)

- **NFC view** opened from a button on the main screen, like Settings. The button is only
  enabled when the connected controller has an NFC reader; otherwise its tooltip says why.
- **Read tags:** tag type, UID and, for amiibo, the amiibo ID and the character's name. Names
  come from a database shipped with the app, merged with amiiboapi.org.
- **Continuous reading:** the reader restarts after each finished read, so you can tap tag
  after tag.
- **History:** every tag read in the session, with how many times it was seen, CSV export and
  a clear button.
- **Write blank NTAG tags:** a short text, or an amiibo ID you read earlier (stored with the
  character's name). The written tag is a plain, unlocked NDEF tag: RelayPad shows the text or
  the character when it reads it back, but it is not an amiibo for a Switch or a game.
- **Safe writes:** RelayPad refuses to write onto an amiibo, a read-only or locked tag, or a
  tag that is not NDEF-formatted. It never sets lock bits and never touches the tag's
  identity pages.
- **Link guidance:** the view says, for the current connection, whether NFC works and what to
  connect. Over Bluetooth it works on its own; over USB the controller also needs its
  Bluetooth link to this PC, so RelayPad asks for it instead of starting a read that would
  drop the cable.

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

- **Four players** on the slot strip, and Joy-Con 2 join with a gesture.
- **Disconnect** button for a connected controller.
- **Bluetooth listening switch:** stop RelayPad from looking for Bluetooth controllers while
  you do not need it.
- **Activity log** button on the main screen; pressing it again closes the window.
- **Waiting screen pairing steps per controller,** with Joy-Con 2 cards and a guide that lists
  the USB and Bluetooth steps of each model.
- Home and back buttons in the top bar replace the back button of each view.

#### Other

- The Switch 1 Pro Controller's player LEDs are read back and rewritten when they do not match
  its player.
- Every warning from the bridge is translated (English and Spanish).
- Activity log entries keep the name of their controller after it disconnects.
- Optional diagnostic reports also record Bluetooth connection times.
- **License:** RelayPad is freeware for personal use. The license and the notices of every
  bundled Rust dependency (`THIRD_PARTY_LICENSES`) ship with the installer and are linked from
  About.

### Changed

- **Battery:** the percent is computed once, on each controller's own curve, and sent with its
  firmware level. The connect line, the periodic line, the tray and the power log now show the
  same number in the same shape.
- **Updates** come from the renamed public repository `ElegantCatterpillar/RelayPad`. If 0.2.0
  does not offer this update on its own, download the installer from Releases once; later
  versions update from the new name.
- **Settings → Drivers** lists only the drivers you can install today (ViGEmBus and HidHide).
- NFC moved out of the profile editor into its own view, because it belongs to the controller,
  not to a profile.
- The Appearance tab is gone from the editor.

### Fixed

- A full battery reads 100 % while charging, instead of sticking at 99 % or flapping every
  second.
- The player slot strip no longer flashes "pending" while a connected controller looks for its
  other link (USB or Bluetooth) in the background.
- Starting NFC over USB alone no longer makes the Switch 1 Pro Controller drop the cable and
  search for its host.

## [0.2.0] - 2026-10-21

The first public build, for friends: a signed Windows installer with automatic updates.

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
