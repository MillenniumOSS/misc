# Custom ROM Install Instructions

## Applies to LG7n and LG8n and LH7n

### Requirements:
1. Unlocked Bootloader
2. External SD Card(optional, but recommended)
3. ROM Recovery
4. PC or Secondary Phone and SD Card
5. Brain(MANDATORY)
6. Common Sense(MANDATORY)
7. Reading Comprehension(MANDATORY)
8. Coffee (optional)
---
### Useful Links:

[Legacy Install Guide(for old ROMs)](https://github.com/MillenniumOSS/misc/blob/main/ROM-install-legacy.md)

---
First things first,
1. Copy ROM zip file to SD Card:
   - Place the ROM zip file in the main directory of your external SD card. this is Important
---
### Main Flashing Instructions(Clean Flash):
1. Copy ROM zip file to SD Card:
   - Place the ROM zip file in the main directory of your external SD card.
2. Flash the ROM Recovery
   - Reboot into bootloader mode
   - Flash vendor_boot: fastboot flash --slot=all vendor_boot vendor_boot.img
3. Reboot to Recovery:
   - Boot into the ROM Recovery, DO NOT USE ORANGEFOX.
4. Factory Reset (First time or switching ROM)
5. Install ROM:
   - Using ADB Sideload (ROM Recovery):
adb sideload rom-filename.zip
(This one should be common sense to change to the actual ROM zip name)
Using SD Card (Custom ROM's Recovery):
- Navigate to the ROM zip file and install it.
- When prompted to reboot to recovery, select Yes
6. Reboot System:
   - Reboot your device and enjoy the new ROM.
---
### Notes:
- If the device doesn't boot successfully, reinstall the ROM using the same instructions.
---
### Known Issues:
- Can't boot GSIs (Enforcing; not tested with Permissive mode). - wontfix
