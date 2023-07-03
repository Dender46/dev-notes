# Fixes

## Unity Windows build doesn't update window resolution after rebuilding
 - _Windows:_ delete registry key located at `HKCU\Software\[company name]\[product name]`
 - _macOS:_ delete the corresponding preferences file located in `~/Library/Preferences/unity`

<sup>source: https://forum.unity.com/threads/cant-change-resolution-for-standalone-build.323931/</sup>

## Installing an APK file via `adb` doesn't show an app
```
adb shell pm uninstall com.company.appname
adb install -r -g file.apk
```
