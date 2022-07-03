# ih8sn-OnePlus6T
_The following information was primarily gathered from the [xda-developers](https://forum.xda-developers.com/t/rom-official-fajita-12-lineageos-19.4437349/) forum for the OnePlus6T_

## On the OnePlus 6T
1. Enable Developer Mode
2. Enable USB Debugging 
3. Enable USB root debugging

## On the PC
1. Download [ih8sn-aarch64.zip](https://github.com/GordonSmith/ih8sn/releases/download/latest/ih8sn-aarch64.zip) from the latest tag/release
2. Extract the contents of the zip file
3. In a cmd prompt (assuming adb is on your PATH):

```sh
adb wait-for-device root
adb wait-for-device remount
adb wait-for-device push system\addon.d\60-ih8sn.sh /system/addon.d/
adb wait-for-device push system\bin\ih8sn /system/bin/
adb wait-for-device push system\etc\init\ih8sn.rc /system/etc/init/
adb wait-for-device push system\etc\ih8sn.conf /system/etc/
adb enable-verity
adb unroot
adb reboot
```

## On the OnePlus 6T
1. Disable Developer Mode
