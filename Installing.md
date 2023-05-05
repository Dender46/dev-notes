# Installing

## Android SDK and Android NDK
Install via Android Studio SDK manager.

**How to set environment vars:**
- `ANDROID_HOME` = `C:\Users\<USER>\AppData\Local\Android\Sdk`
- `ANDROID_NDK_HOME` = `C:\Users\<USER>\AppData\Local\Android\Sdk\ndk\21.4.7075529`

## Bazel
Download bazelisk - rename it to `bazel.exe` and put somewhere (`C:\dev\bazel`). Then add its path to %PATH%

## MacOS Bootable Drive
### Error while making bootble drive: `Terminating app due to uncaught exception 'NSInternalInconsistencyException'`
Sollution from [link](https://discussions.apple.com/thread/251386184)

Run following command before making bootable drive:
```
sudo plutil -replace CFBundleShortVersionString -string "12.6.03" /Applications/Install\ macOS\ Sierra.app/Contents/Info.plist
```
Continue with the process.
