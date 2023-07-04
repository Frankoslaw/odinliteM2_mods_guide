# Set of guides how to mod ayn odin lite handheld.

Disclaimer: This guide only applies to ayn odin lite M2. I don't own M0 or any other ayn handheld so I cannot test my ports on them. Also everything described here comes at a risk of bricking your device. So think twice before you will do it.

## Unlocking bootloader:

### 1. Disable oem lock

Click 5 times on build number in settings to enable developer settings. Then in "System" options you will see new "Developer options" field. Now you need to tick option "OEM Unlocking" and "USB Debugging". After this connect your device using usb to a computer, install adb and type `adb devices` after that accept the prompt on the device to give the access to usb debugging.

### 2. Unlock flashing

Now you can type this commands to unlock the device. **THIS IS LAST WORNING AFTER THIS STEP THERE IS NO TURNING BACK. UNLOCKING BOOTLOADER CAN BRICK YOUR DEVICE AND WILL VOID YOUR WARRANTY. BE AWARE OF THE RISKS.** Also this step will erase your whole device memory so its recomended to make backup beforhend.

```sh
adb reboot bootloader
fastboot flashing unlock
```

Now on your device accept the prompt and wait for the process to finish. To return to the OS type in cmd:

```sh
fastboot reboot
```

Congratualations now your device is unlocked.

## Content:

- **magisk** - Guide to rooting ayn odin lite
- **backup** - Backup files dumped directly from device:
  - build.prop
  - getvar-all.txt - fastboot variables
  - hardware.txt - removed from repo, because of security concers, but you can dump it yourself using `hwinfo` command in termux ( Disclaimer: It requires root )
- **TWRP** - Team Win Recovery Project port for alps/odinlite_6877_fhd_v1. **Work in progress**
## Usefull articles:

### unbrick mt6877
https://www.xda-developers.com/bypass-mediatek-sp-flash-tool-authentication-requirement/

### Build enviorment
https://source.android.com/docs/setup/start/initializing

## TODO:

- build device tree for TWRP
- build device tree for Lineage OS
- encrypt backups non public part with sops
