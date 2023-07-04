# Root ayn odin lite with magisk

## 1. Get boot.img from official firmware on ayn tech site

https://www.ayntec.com/pages/software

## 2. Patch the image directly on the device using official magisk apk

https://github.com/topjohnwu/Magisk

## 3. Flash the patched image using fastboot

Disclaimer: Ayn odin lite uses android 11 and what comes with it is A/B partition scheme. Because of that you will need to flash both boot_a and boot_b. Otherwise after the update or reboot your device will switch the slot into unrooted version.

```ps
adb reboot bootloader
fastboot --disable-verity --disable-verification flash boot_a magisk_patched.img
fastboot --disable-verity --disable-verification flash boot_b magisk_patched.img
fastboot reboot
```
