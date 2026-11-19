# Back up your amiibo

**English** · [Español (México)](es/amiibo-backup.md)

RelayPad can read an amiibo you own with your controller and keep a backup of it on your PC. If
the figure or card gets lost or damaged, you can write that backup on a blank tag and keep
using it.

This works on the Switch 2 Pro Controller and the right Joy-Con 2. On the Switch Pro Controller
(Switch 1) it is built and still being tested on hardware.

## Personal use only

- Back up only amiibo that you own, for your own use.
- Do not share, sell or distribute backup files or tags written from them.
- RelayPad does not include amiibo data or Nintendo keys, does not download them and does not
  link to places that offer them. Everything comes from your own amiibo, your own console and
  your own PC.
- Backups and keys stay on your PC. RelayPad never uploads them and never writes them to its
  logs or diagnostic reports.

Laws about backup copies differ between countries. Check what applies where you live.

## What you need

- A controller with an NFC reader:
  - a **Switch 2 Pro Controller**, over Bluetooth or a USB cable;
  - a **right Joy-Con 2**, on its own or joined with a left one. Hold the tag flat over its
    right stick. The left Joy-Con 2 has no reader;
  - a **Switch Pro Controller** (the Switch 1 model) over **Bluetooth**, with its USB cable
    unplugged. It keeps its NFC reader off while the cable is plugged in, even if Bluetooth is
    connected too.
- The amiibo you want to back up.
- To write a backup on a tag: a blank **NTAG215** tag and **your keys file** (see below).

## Make a backup

1. Open the **NFC** view from the main screen.
2. Hold the amiibo on the controller and keep it still.
3. RelayPad shows the character's name and picture. Press **Save backup**.
4. The backup is saved as a `.bin` file in your amiibo backups folder. **Open folder** shows
   it. You can change the folder, or have every amiibo you read saved by itself, in
   **Settings**.

Making a backup only reads the amiibo. It is not changed.

## The keys file

An amiibo is signed for the one tag it lives on. To move a backup to another tag, RelayPad has
to sign it again for that tag, and that takes two keys that belong to Nintendo.

- RelayPad does not come with the keys and cannot fetch them.
- The keys file has to come from **your own console**. This guide does not explain how to get
  it out, and RelayPad does not help with that step.
- It is one file of 160 bytes holding both keys.

Without the keys file you can still make backups and see which amiibo a backup holds. You only
need it to write a backup on a tag.

To load it, press **Write** in the NFC view, choose the amiibo, and in step 2 press
**Load keys file…**. With **Keep a copy on this PC** on, you load it only once: the copy stays
in RelayPad's folder on your PC. **Forget keys** deletes that copy.

## Write a backup on a blank tag

Writing seals the tag for good. It becomes that amiibo and can never be written again, so
RelayPad asks before it writes.

1. In the NFC view press **Write**, or **Copy to another tag** on an amiibo you just backed up.
2. Choose the amiibo: one of your recent reads, or a `.bin` backup with **Load .bin…**.
3. Load your keys file if it is not loaded yet. RelayPad tells you whether the backup verifies
   with your keys; one that does not is not written.
4. Put a blank NTAG215 on the controller and press **Write amiibo**.
5. RelayPad reads the tag and asks, naming the amiibo and the tag. Check both and press
   **Yes, write it**.
6. Keep the tag still until RelayPad says it is done.

Only a blank NTAG215 is written. Any other tag, an amiibo included, is left untouched. If you
swap the tag after confirming, nothing is written on the new one.

RelayPad cannot read back the last two values it writes on the tag (its password), because the
controller does not report them. The way to be sure is to read the new tag again in RelayPad
and try it on your console.

## Questions

**Does the written tag work on a console?**
It is meant to: the tag is signed and sealed like an original amiibo. Read it again in RelayPad
to check it, then try it on your console.

**Can I write over an amiibo or reuse a tag?**
No. An amiibo is sealed, and so is every tag RelayPad writes.

**Can I use a `.bin` made by another tool?**
Yes, if it is a full backup of an amiibo that you own.

**Where do I get the keys file or amiibo files?**
Only from your own console and your own amiibo. RelayPad does not provide or link to either.
