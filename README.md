<h1 align="center">
  <a href="https://pitchblackrecovery.com"><img src="https://raw.githubusercontent.com/shovon668/xda-template/r3/pbrp3-banner-xda.png" alt="Welcome to PitchBlack Recovery Project 👋" width="600"></a>
  <br>
 Welcome to PitchBlack Recovery Project 👋
  <br>
</h1>

# PitchBlack Recovery Project device tree for Samsung S20 Ultra aka z3s

## Kernel source 
Available at https://github.com/corsicanu/android_kernel_samsung_universal9830 (thanks @corsicanu)

## Bugs
- ADB Sideload
- Fastbootd

## How to build
This repository is compatible with the Android 12.1 tree of [the PBRP minimal manifest](https://github.com/PitchBlackRecoveryProject/manifest_pb)
1. Set up the build environment following instructions from [here](https://github.com/PitchBlackRecoveryProject/manifest_pb?tab=readme-ov-file#how-to-build)
2. In the root folder of cloned repo you need to clone the device tree:
```bash
git clone -b android-12.1 https://github.com/ExtremeXT/pbrp_android_device_samsung_z3s.git device/samsung/z3s
```
3. To build:
```bash
. build/envsetup.sh && lunch pbrp_z3s-eng && mka recoveryimage -j$(nproc —all)
```
