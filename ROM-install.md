# Custom ROM Install Instructions

## Applies to LG7n and LG8n and LH7n

### Requirements:
1. Unlocked Bootloader
2. External SD Card(optional, but recommended)
3. LineageOS Recovery or OrangeFox Recovery
4. PC or Secondary Phone and SD Card
5. Brain(MANDATORY)
6. Common Sense(MANDATORY)
7. Reading Comprehension(MANDATORY)
8. Coffee (optional)
---
### Useful Links:

[AB Prep Tool](https://github.com/MillenniumOSS/misc/releases/tag/firmware)

---
First things first,
1. Copy ROM zip file to SD Card:
   - Place the ROM zip file in the main directory of your external SD card. this is Important

### Preparations for First Flash (Skippable in future roms if already done or if already in cusrom) (Needed if you reflashed stock rom or coming from GSI, never skip this on first install if coming from stock or GSI)

#### ⚠️ WARNING: DO NOT SKIP THIS PART IF YOU'RE INSTALLING THIS ROM FOR THE FIRST TIME, THIS IS TO ENSURE A/B SWITCHING WON'T CAUSE ANY ISSUES, I AM NOT HELD RESPONSIBLE FOR ANY ISSUES CAUSED BY SKIPPING THIS PART ⚠️

##### THIS IS THE ONLY TIME ORANGEFOX SHOULD BE USED

1. Reboot to Bootloader:
   - Power off your device and boot into the bootloader.

2. Disable VBMeta (skip if already done):
fastboot flash vbmeta --slot all --disable-verity --disable-verification vbmeta.img

3. Flash OrangeFox Recovery (if not already done):
   - Follow the instructions in the OrangeFox post.

4. Flash AB Partition Prep Tool (first time only):
   - Boot into OrangeFox Recovery.
   - Flash the AB PrepTool zip
Note: This overwrites OrangeFox with Stock Recovery, don't reboot yet
5. Flash vendor_boot.img:
   - Using OrangeFox(SCROLL DOWN TO FIND "Vendor Boot Image" in the SELECTION) or fastboot:   
fastboot flash vendor_boot --slot all vendor_boot.img
  -Tick "Flash to both slots if flashing with orangefox
6. Reboot to LineageOS Recovery:
fastboot reboot
   - Press the volume up button until you enter LineageOS Recovery.
---
### Main Flashing Instructions(Clean Flash):
1. Copy ROM zip file to SD Card:
   - Place the ROM zip file in the main directory of your external SD card.
2. Reboot to Recovery:
   - Boot into the ROM Recovery, DO NOT USE ORANGEFOX.
3. Factory Reset (First time or switching ROM)
4. Install ROM:
   - Using ADB Sideload (LineageOS Recovery):
adb sideload lineage-20.0-xxxxxxxx-UNOFFICIAL-LGxn.zip
(This one should be common sense to change to the actual ROM zip name)
Using SD Card/Internal Storage (OrangeFox Recovery):
- Navigate to the ROM zip file and install it.
Using SD Card (Custom ROM's Recovery):
- Navigate to the ROM zip file and install it.
- When prompted to reboot to recovery, select Yes
4. Reboot System:
   - Reboot your device and enjoy the new ROM.
---
### Notes:
- If the device doesn't boot successfully, reinstall the ROM using the same instructions.
---
### Known Issues:
- Can't boot GSIs (Enforcing; not tested with Permissive mode). - wontfix
