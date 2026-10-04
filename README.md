# Inside the Ultra: build the APK

You need a free GitHub account and a computer (or your phone's browser in "Desktop site" mode).

1. Create a new repository on github.com and upload everything in this folder
   (including the hidden `.github` folder): Add file > Upload files.
2. Open the repository's **Actions** tab. The "Build APK" run starts by itself
   (or press "Run workflow"). It takes about 5 minutes.
3. Open the finished run, download the **inside-the-ultra-apk** artifact, unzip it,
   and send `app-debug.apk` to your phone.
4. Tap the APK on the phone and allow "Install unknown apps" when asked.

The APK is a debug build (fine for personal use). For the Play Store you would
need a signed release build.

## Build locally instead (Android Studio + Node 20 + JDK 17)
    npm install
    npx cap add android
    npx cap open android      # then Build > Build APK(s)
Add `android:screenOrientation="sensorLandscape"` to the activity in AndroidManifest.xml.
