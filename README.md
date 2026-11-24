# Ledger: who owes whom

A simple app for tracking money you owe and money owed to you.

## Use it
Open `index.html` in any browser. There's nothing to install and no server. Your data stays in the browser (localStorage).

## Features
- **Add entries**: "I gave / lent money" (they owe you more) or "I got / borrowed money" (you owe them more), with an amount, a date and a note.
- **Balance for each person**: green means they owe you, red means you owe them.
- **Summary**: total owed to you, total you owe, and your net balance.
- **Settle up**: one click records a payment that brings a person's balance to zero.
- **Full history for each person**: click a person to see it, and delete entries you don't want.
- **Search and filter**: All, Owe me, I owe, Settled.
- **Currency picker**: USD, INR, EUR, GBP, CAD, AUD, JPY.
- **Backups**: export or import your data as JSON.
- Works on phones and supports dark mode.

## Android app
The `android/` folder holds an Android app (Android 8.0 or later) that runs the same `index.html` inside a WebView. Data is saved on the phone, and **Export backup** and **Import backup** use Android's file picker.

**Get the APK.** Each push builds the app with GitHub Actions. Open the repo's **Actions** tab, choose the latest **Build Android APK** run, and download the **Ledger-apk** artifact. Unzip it, copy `app-debug.apk` to your phone, and open it (allow "Install unknown apps" when asked).

**Build it yourself.** Open the `android/` folder in Android Studio and press Run, or run `cd android && ./gradlew assembleDebug`.
