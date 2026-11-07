# BillKhata (बिल खाता) - Android App Repository

This repository contains the complete **BillKhata** Android application, pre-configured with **Capacitor 6** and an automated **GitHub Actions APK & Google Play Store AAB Builder**.

## 1. How to Build & Install the APK Directly from GitHub (No Coding Needed)

1. Create a free account at [github.com](https://github.com) and create a new repository named `billkhata`.
2. Upload all files from this folder (including `.github/workflows/build-android.yml`, `www/index.html`, `package.json`, and `capacitor.config.json`) to your repository.
3. Click the **Actions** tab at the top of your GitHub repository.
4. GitHub will automatically run **"Build BillKhata Android APK & Play Store AAB"** (takes ~3 minutes).
5. Once finished, click on the completed workflow run and download **`BillKhata-Installable-APK`** under the **Artifacts** section.
6. Unzip it on your phone and tap `app-debug.apk` to install **BillKhata** on your Android device.

## 2. How to Publish on Google Play Store

1. Create a developer account at [Google Play Console](https://play.google.com/console) ($25 one-time registration fee).
2. Generate a signing keystore (using Android Studio -> *Build* -> *Generate Signed Bundle / APK* -> *Android App Bundle*).
3. Upload the signed `.aab` file to **Production** or **Internal Testing** in Google Play Console.
