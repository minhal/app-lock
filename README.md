# Password Please - App Lock

A free app locker for Android with no ads and no internet access.
Lock any app (including the Play Store and Settings) with a PIN or a password, with optional fingerprint unlock.
When you open a locked app, it politely asks: "Password, please."

## Build the APK on GitHub (phone only, free)

1. Sign in at github.com and create a new repository (the **+** button, then **New repository**).
2. In the new repository, tap **Add file › Upload files**, upload `AppLock.zip`, and tap **Commit changes**.
3. Tap **Add file › Create new file**. Name it exactly `.github/workflows/build.yml`,
   paste in the contents of `build.yml`, and tap **Commit changes**.
4. Open the **Actions** tab. A build starts by itself and takes about 5 minutes.
5. When it shows a green check, open the repository's **Releases** (on the main page) and download `AppLock.apk`.
6. Open the downloaded file on your phone. If asked, allow your browser to install apps.

Every time you change a file in the repository, GitHub builds a new APK. New builds install over old ones.

To update an existing repository with a new `AppLock.zip`, upload it again with **Add file › Upload files**
and commit. GitHub replaces the old zip and builds the new version.

## Build with Android Studio (computer)

1. Unzip `AppLock.zip`.
2. In Android Studio, choose **Open** and pick the `AppLock` folder.
3. Connect your phone with USB debugging on, and press **Run**.

## Before publishing on Google Play

- Store title: `Password Please - App Lock` (26 of the 30 characters allowed).
- Store icon: `store/play_store_icon_512.png`.
- Google Play needs an `.aab` bundle signed with your own upload key, not this test APK.
- The app ID is `com.passwordplease.applock`. It can't be changed after you publish.
- The background service uses the "special use" type, so the Play Console will ask you to describe it. The text is in `AndroidManifest.xml`.
- App lockers must use Usage access and "Display over other apps". This app does not use the Accessibility service.
