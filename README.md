# android-dev-install
android dev install

## install

### android sdk

```sh
snap install androidsdk
androidsdk 'system-images;android-30;default;x86_64' platform-tools 'cmdline-tools;latest' 'build-tools;30.0.3' emulator 'platforms;android-30'
avdmanager create avd -n test -k 'system-images;android-30;default;x86_64'
emulator -avd test
```

### environment variables

```sh
export ANDROID_SDK_ROOT=$HOME/AndroidSDK
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools/
export PATH=$PATH:$ANDROID_SDK_ROOT/cmdline-tools/latest/bin/
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator/
```

### cordova

```sh
npm i -g cordova
cordova create MyApp
cd MyApp
cordova platform add browser
cordova platform add android

cordova requirements
cordova run android
cordova run browser
cordova build
```
