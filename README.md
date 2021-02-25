## In general
You might find it usefull to install a ***packagename app*** to simplify searching **packagenames** in your *adventures journey* to debloat your phone.
You can find them in one of your favorite playstores.

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