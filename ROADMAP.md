# What's next for RelayPad

**English** · [Español (México)](es/ROADMAP.md)

RelayPad's goal is simple: every Nintendo Switch controller, working with all of its features,
on every device you play on. This page says where each controller and each platform stands
today and what comes next. Priorities can change as we test on real hardware, and your
[ideas](https://github.com/ElegantCatterpillar/RelayPad/issues) help decide the order.

Already out: the [changelog](CHANGELOG.md). Want to speed this up? [Support RelayPad](README.md#support-relaypad):
it buys the controllers below and pays for Linux, macOS and RelayPad's own driver.

✅ works · 🧪 built, being tested on hardware · 🔜 next up · ⬜ planned · 🔍 being studied ·
❌ the platform does not allow it · — the controller has no such hardware

## Platforms

| Platform | Status | What to expect |
|---|---|---|
| Windows 10 and 11 | ✅ Available | Games see an Xbox 360 or DualShock 4 controller. |
| Linux | 🔜 Next | The same controllers, shown to games as a standard gamepad. |
| macOS | ⬜ Planned, after Linux | Needs a permission from Apple that we still have to obtain. |
| Android | ⬜ Planned, later | An app that connects Switch 2 controllers, which Android cannot pair on its own, and offers them to your games. It will need Shizuku, a free helper app; no root. |
| iOS and iPadOS | ⬜ Planned, as a companion app | iOS does not let an app offer a controller to other games, so RelayPad cannot make your games see the controller there. The app will look after your Switch 2 controllers instead. |

### What each platform will cover

| Feature | Windows | Linux | macOS | Android | iOS and iPadOS |
|---|---|---|---|---|---|
| Play your games with the controller | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Motion and rumble in games | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Profiles: remapping, turbo, macros, stick curves, gyro aim | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Several players at once, each with a controller | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Connect over Bluetooth | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| Connect with a USB cable | ✅ | ⬜ | ⬜ | 🔍 | ❌ iPhone · 🔍 iPad |
| Status and battery level | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| Test buttons, sticks and motion | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| Stick calibration | ✅ | ⬜ | ⬜ | ⬜ | 🔍 |
| Player LEDs | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| NFC: read amiibo with the controller | ✅ | ⬜ | ⬜ | ⬜ | 🔍 |

### What the iOS and iPadOS app will and will not do

The ❌ marks are limits of the system, not of RelayPad: only Apple decides which controllers
games can see.

**It will**, with Switch 2 controllers over Bluetooth:

- show each controller's status and battery level;
- let you test buttons, sticks and motion;
- set the player LEDs.

**It will not:**

- make your games see the controller, so there are no profiles, motion or rumble in games,
  and no players;
- connect a controller with a USB cable on an iPhone;
- add anything to Switch 1 controllers. iOS already connects them to your games on its own,
  and it gives apps no direct line to them, so features like NFC stay out of reach.

**Still being studied:** the USB cable on an iPad, reading amiibo with Switch 2 controllers on
iOS and iPadOS, and stick calibration.

The Windows column says what the app does today; which controller has each feature is listed
below. Other platforms will get their own detail as they arrive.

## Switch 2 controllers

### Switch 2 Pro Controller

| Feature | Status | Notes |
|---|---|---|
| Bluetooth | ✅ | |
| USB cable | ✅ | |
| Pair over Bluetooth by plugging in the cable | 🧪 | |
| Switch between cable and Bluetooth while playing | ✅ | The game never loses the controller. |
| Buttons, sticks and triggers | ✅ | Including GL, GR and C. |
| Motion (gyro and accelerometer) | ✅ | |
| HD rumble | ✅ | |
| Player LEDs | ✅ | |
| Battery level | ✅ | |
| Hide the real controller from games (HidHide) | 🧪 | |
| NFC: read amiibo and tags | ✅ | Over Bluetooth and USB, with the character's name. |
| NFC: write a text on a blank tag | ✅ | |
| NFC: back up an amiibo you own and write it on a blank tag | ✅ | With your own keys file. See [Back up your amiibo](amiibo-backup.md). |

### Joy-Con 2, (L) or (R) on its own

| Feature | Status | Notes |
|---|---|---|
| Bluetooth | ✅ | |
| USB cable | — | Joy-Con 2 have no USB port. |
| Buttons and stick | ✅ | Held sideways, as a small controller. |
| Motion (gyro and accelerometer) | ✅ | |
| Rumble | ✅ | |
| Player LEDs | ✅ | |
| Battery level | ✅ | |
| Hide the real controller from games (HidHide) | 🧪 | |
| Mouse mode | ⬜ | |
| NFC: read amiibo and tags | ✅ | Right Joy-Con only; the left one has no reader. Hold the tag over the right stick. |
| NFC: write a text on a blank tag | ✅ | Right Joy-Con only. |
| NFC: back up an amiibo you own and write it on a blank tag | ✅ | Right Joy-Con only, with your own keys file. |

### Joy-Con 2 pair, (L) and (R) as one controller

| Feature | Status | Notes |
|---|---|---|
| Both halves as one controller | ✅ | Hold ZL and ZR together. The pair ends when either half disconnects. |
| Buttons and both sticks | ✅ | |
| Motion (gyro and accelerometer) | ✅ | |
| Rumble | ✅ | |
| Player LEDs | ✅ | |
| Battery level of each half | ✅ | |
| Hide the real controllers from games (HidHide) | 🧪 | |
| Mouse mode | ⬜ | |
| NFC: read, write and back up amiibo | ✅ | With the right Joy-Con of the pair. |

### Nintendo GameCube Controller (Nintendo Switch Online)

| Feature | Status | Notes |
|---|---|---|
| Full support | ⬜ | Not started. |

## Switch 1 controllers

### Switch Pro Controller

| Feature | Status | Notes |
|---|---|---|
| Bluetooth | ✅ | Paired from Windows Bluetooth settings, opened from the app. |
| USB cable | ✅ | |
| Buttons, sticks and triggers | ✅ | |
| Motion (gyro and accelerometer) | ✅ | |
| HD rumble | ✅ | |
| Player LEDs | ✅ | |
| Battery level | ✅ | |
| Hide the real controller from games (HidHide) | ✅ | |
| NFC: read amiibo and tags | ✅ | With the character's name. |
| NFC: write a text or an amiibo ID on a blank tag | ✅ | The tag is not an amiibo for a Switch or a game. |
| NFC: back up an amiibo you own and write it on a blank tag | ✅ | Bluetooth only, with your own keys file. See [Back up your amiibo](amiibo-backup.md). |

### Joy-Con, (L) or (R) on its own

| Feature | Status | Notes |
|---|---|---|
| Bluetooth, buttons and stick held sideways | 🔜 | The next controller we add. |
| Battery level | 🔜 | |
| Motion, rumble and player LEDs | ⬜ | |
| NFC: read amiibo | ⬜ | Right Joy-Con only. |

### Joy-Con pair, (L) and (R) as one controller

| Feature | Status | Notes |
|---|---|---|
| Both halves as one controller | ⬜ | After each Joy-Con works on its own. |

### NES Joy-Con (Nintendo Switch Online)

| Feature | Status | Notes |
|---|---|---|
| Bluetooth and buttons | 🔜 | Arrives with the Joy-Con. |

### SNES Controller (Nintendo Switch Online)

| Feature | Status | Notes |
|---|---|---|
| Full support | ⬜ | Not started. |

### Nintendo 64 Controller (Nintendo Switch Online)

| Feature | Status | Notes |
|---|---|---|
| Full support | ⬜ | Not started. |

### SEGA Genesis Control Pad (Nintendo Switch Online)

| Feature | Status | Notes |
|---|---|---|
| Full support | ⬜ | Not started. |

## App

| Feature | Status | Notes |
|---|---|---|
| Signed installer | 🔜 | So Windows stops warning about it. Updates are already signed. |
| Tray icon per controller | 🔜 | |
| Tips for the best Bluetooth connection | 🔜 | |
| Low-battery notice | 🔜 | Before your controller dies mid-game. |
| DirectInput and GameInput output | ⬜ | Next to Xbox 360 and DualShock 4. |
| 3D controller view | ⬜ | |

## Have an idea?

[Open an issue](https://github.com/ElegantCatterpillar/RelayPad/issues) with your controller,
what you want it to do, the game you play and the device you play on.
