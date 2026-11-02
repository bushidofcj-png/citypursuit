# City Pursuit APK

Game file: www/index.html (edit it, push, and a new APK is built).

## Build the APK without Android Studio
1. Create a free account at github.com and make a new repository (private is fine).
2. Upload everything in this folder, including the hidden .github folder.
3. Open the repository's Actions tab and wait for "Build APK" to finish (about 5 minutes).
4. Open the finished run, scroll to Artifacts, download city-pursuit-apk, unzip it.
5. Send app-debug.apk to your phone and tap it to install
   (Android will ask you to allow installs from your browser or file manager).

## Build locally instead (needs Node 20, Java 17, Android Studio)
npm install
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk
