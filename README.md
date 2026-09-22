# Health Planner (Android)

BMI, exercise plan, calorie target, food log, weekly summary and weight tracking, packaged as an Android app with Capacitor.

## One-time setup
1. Install Node.js 22 or newer.
2. Install Android Studio (a recent version; it includes the JDK and Android SDK).
3. In this folder run: `npm install`

## Easiest: get the APK without installing anything (GitHub)
1. Create a free GitHub account and a new empty repository.
2. Upload everything in this folder to it (or use `git push`). Do not upload node_modules.
3. Open the repository's Actions tab. The "Build APK" workflow runs automatically (or press Run workflow).
4. After about 5 minutes open the finished run and download the `health-planner-apk` artifact. Unzip it to get app-debug.apk.
5. Send the APK to your phone, tap it, and allow "Install unknown apps" when asked.

## Run on your phone from Android Studio
1. On your phone: Settings > About phone > tap "Build number" 7 times, then enable Developer options > USB debugging.
2. Plug the phone into your computer and accept the prompt on the phone.
3. Run: `npm run open` (opens the project in Android Studio). Wait for the Gradle sync to finish.
4. Choose your phone in the device dropdown and press the green Run button.

## Get an APK file to share
In Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s). The debug APK appears under android/app/build/outputs/apk/debug/.

## Changing the app
The whole app is www/index.html. After any edit run `npm run sync`, then Run again in Android Studio.

## Before publishing on Google Play
- Change the app ID (currently com.example.healthplanner). Ask Claude to regenerate the project with your ID rather than editing it by hand.
- Add an app icon and splash screen.
- Build a signed release bundle (Build > Generate Signed Bundle / APK) and keep the keystore file safe.
