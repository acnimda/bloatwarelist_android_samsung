## bloatware list Samsung S21

## Globally :earth_africa:

### TL:DR
You want to debloat your *brand new* android phone, without reading the README file, and use straight away some *awesome* `commands` with `adb`.

### prerequirements
1.  `adb` is installed.
2.  Phone is enabled in *develop settings*.
3. *usb-debugging* is enabled.

### NOTE :bowtie::
- Use of this bloatwarelist is always and everywhere on your own risk.
- :warning: This is not an advice, nor a financial advice! :warning:
- I like drinking :beer:.
- :green_book: If you have questions, read the README first :green_book:
- Feedback, suggesstions and donations are more then welcome.

## packages sort

### facebook
1. Run `adb shell pm list packages | grep facebook`
2. Run `adb shell pm uninstall --user 0 com.facebook.system`
3. Repeat this with all **packages** you found.
#### NOTE!:
If, somehow, you want to keep data and cache of the **package** add  `-k`, this isn't default.
#### full list
```s
adb shell pm uninstall --user 0 com.facebook.system
adb shell pm uninstall --user 0 com.facebook.appmanager
adb shell pm uninstall --user 0 com.facebook.services
```
#### Note2:
Due to your region, some packages might prevented from uninstalling. You can disable them instead. Use following command on `adb shell`:
```s
adb shell pm disable-user --user 0 com.facebook.system 
adb shell pm disable-user --user 0 com.facebook.services
adb shell pm disable-user --user 0 com.facebook.appmanager
```




