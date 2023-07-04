# Set of guides how to mod ayn odin lite handheld.

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
