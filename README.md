## In general
You might find it usefull to install a ***packagename app*** to simplify searching **packagenames** in your *adventures journey* to debloat your phone.
You can find them in one of your favorite playstores.

### some best practices

#### prerequirements
-  `adb` is installed.
-  Phone is enabled in *develop settings*.
- *usb-debugging* is enabled.

1. start an `adb server`
```s
adb devices
```
2. accept *access* on your device.
3. 

when you are finished close the `adb server` by running `adb kill-server`.

## how 2 ...
### find packages
When you modified `<YOUR_PACKAGE_NAME>` to your likings.
- Run `adb shell pm list packages | grep <YOUR_PACKAGE_NAME>`

### find system packages
This will print a list only for system packages.
- Run `adb shell pm list packages -s`
### find 3rd party packages
This will print a list only 3rd party (or non-system) packages.
- Run `adb shell pm list packages -3`
### find enabled packages
- Run `adb shell pm list packages -e`
### find disabled packages
- Run `adb shell pm list packages -d`
### find path to the installed APK files
- Run `adb shell pm list packages -f`

## :hankey: Possible Errors :hankey:
### unauthorized device
If you see an error like this. 
![](images/device_unauthorized.JPG)
It's most likely you didn't accept your computer authorization on your device.
1. Click *"Revoke USB debugging authorizations"*
2. Run `adb devices`
3. Click `accept` on your device.
