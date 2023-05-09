# Installing

## Android SDK and Android NDK
Install via Android Studio SDK manager.

**How to set environment vars:**
- `ANDROID_HOME` = `C:\Users\<USER>\AppData\Local\Android\Sdk`
- `ANDROID_NDK_HOME` = `C:\Users\<USER>\AppData\Local\Android\Sdk\ndk\21.4.7075529`

## Install Android SDK and NDK on Windows Bash (WSL)
``` bash
cd /home/<user>/
sudo apt-get install unzip
wget https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip
unzip sdk-tools-linux-4333796.zip -d Android
rm sdk-tools-linux-4333796.zip
sudo apt-get install -y lib32z1 openjdk-8-jdk
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
export PATH=$PATH:$JAVA_HOME/bin
printf "\n\nexport JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64\nexport PATH=\$PATH:\$JAVA_HOME/bin" >> ~/.bashrc
cd Android/tools/bin
./sdkmanager "platform-tools" "platforms;android-30" "build-tools;30.0.3" "ndk;21.4.7075529"
export ANDROID_HOME=/home/<user>/Android
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
printf "\n\nexport ANDROID_HOME=/home/<user>/Android\nexport PATH=\$PATH:\$ANDROID_HOME/tools\nexport PATH=\$PATH:\$ANDROID_HOME/platform-tools" >> ~/.bashrc
android update sdk --no-ui
sudo apt-get install gradle
gradle -v
adb start-server
```
<sup>source: https://gist.github.com/jjvillavicencio/18feb09f0e93e017a861678bc638dcb0</sup>

## Bazel
Download bazelisk - rename it to `bazel.exe` and put somewhere (`C:\dev\bazel`). Then add its path to %PATH%

## MacOS Bootable Drive
### Error while making bootble drive: `Terminating app due to uncaught exception 'NSInternalInconsistencyException'`
Run following command before making bootable drive:
```
sudo plutil -replace CFBundleShortVersionString -string "12.6.03" /Applications/Install\ macOS\ Sierra.app/Contents/Info.plist
```
Continue with the process.

<sup>source: https://discussions.apple.com/thread/251386184</sup>
