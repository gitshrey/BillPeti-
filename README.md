# 📦 BillPeti — Your Digital Bill Storage


[Architecture](https://www.google.com/search?q=./index.html)
[Platform](https://www.google.com/search?q=./.github/workflows/build-android.yml)
[](#multilingual-support)

**BillPeti (बिल पेटी)** is an offline-first Android digital bill vault and party-wise invoice organizer built for Indian wholesalers, retailers, and shopkeepers. It keeps purchase bills, multi-page *parchas*, party folders, and overall party payment balances organized in a private local database—without cluttering the phone's personal photo gallery or uploading sensitive business records to external cloud servers.

## ✨ Key Features

* **📸 Multi-Page Bill & Parcha Capture**: Snap or import multi-page invoices with instant client-side image compression, watermarks, pinch-to-zoom inspection, and full-screen viewing.
* **📁 Party-Wise Folders & Balance Tracker**: Automatically groups bills by wholesaler or shop name. Includes an optional per-party **Paid & Balance Left** toggle so merchants can track overall payments made and remaining balance due without complex ledger overhead.
* **🔍 Instant Search & Smart Date Filters**: Filter bills across the home dashboard, full-screen view, or inside specific party folders by note, amount, date presets (*Today, Yesterday, Last 7 Days, This Month*), or custom date ranges.
* **💬 Native WhatsApp Image + Caption Sharing**: Shares multi-page JPEG bill photos alongside structured party, amount, date, and note details directly to WhatsApp via Android `FileProvider` intents.
* **📊 Full-Fidelity Excel (CSV) Backup & Restore**: One-tap offline backup and restore (including embedded bill images) exported directly to the device's `Downloads` folder, paired with configurable **Weekly / Monthly Smart Backup Reminders**.
* **🌐 8 Indian Languages**: Full native interface localization in English, हिन्दी (Hindi), मराठी (Marathi), ગુજરાતી (Gujarati), ਪੰਜਾਬੀ (Punjabi), বাংলা (Bengali), தமிழ் (Tamil), and తెలుగు (Telugu).
* **🔒 100% Offline & Private by Design**: Powered by persistent `IndexedDB` + `localStorage` storage. Zero cloud tracking, zero external API dependencies, and zero personal gallery mixing.

## 🛠️ Tech Stack & Architecture

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend UI** | HTML5, Tailwind CSS, Lucide Icons | Responsive mobile-first fintech UI with dark mode support |
| **Storage Engine** | IndexedDB (`BillPetiUserDB_v2`) + LocalStorage | High-capacity offline persistence for multi-page compressed bill photos |
| **Native Runtime** | Capacitor 6 Android + Custom Java Bridge | Native `FileProvider` WhatsApp image sharing, hardware back-button routing, and `MediaStore` Downloads export |
| **CI/CD Pipeline** | GitHub Actions (`ubuntu-24.04`, JDK 21, Node 22) | Automated Gradle `assembleRelease` build signed with RSA-2048 v1/v2 production keystore |

## 📲 Downloading & Installing the Android APK

1. Open the releases tab of this repository .
2. Download **`BillPeti.apk`** to your Android phone.
3. Tap to install. Because updates are signed with a persistent production release certificate, new versions install cleanly over existing versions without losing saved bills.

## 🔐 Privacy & Security Notice

BillPeti operates **100% offline**. All bill photos, notes, amounts, and party balances are processed and stored locally on your device. No personal or business data is ever transmitted to external servers.
