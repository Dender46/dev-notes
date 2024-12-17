# Fixes

## Unity Windows build doesn't update window resolution after rebuilding
 - _Windows:_ delete registry key located at `HKCU\Software\[company name]\[product name]`
 - _macOS:_ delete the corresponding preferences file located in `~/Library/Preferences/unity`

<sup>source: https://forum.unity.com/threads/cant-change-resolution-for-standalone-build.323931/</sup>

<br>

## Installing an APK file via `adb` doesn't show an app
```cmd
adb shell pm uninstall com.company.appname
adb install -r -g file.apk
```

<br>

## Building C++ .exe with `cl` errors with `fatal error C1034: iostream: no include path set`
Possible solution is to call this in the terminal, and then open VSCode from that terminal
```cmd
cmd /c 'call "C:\Program Files\Microsoft Visual Studio\2022\Professional\VC\Auxiliary\Build\vcvars64.bat"'
```
```cmd
code .
```
or run `Developer Command Prompt` from Start menu and then launch VSCode

<br>

## Fix previous commits with wrong author email and name
```cmd
git rebase -r <some_commit_before_all_of_your_bad_commits> --exec 'git commit --amend --no-edit --reset-author'
```

<sup>source: https://stackoverflow.com/questions/750172/how-do-i-change-the-author-and-committer-name-email-for-multiple-commits</sup>

<br>
