# 📦 Bill Store — Your Digital Bill Storage

[![Android Release CI](https://img.shields.io/badge/Android_APK-Signed_Release_v2.3-079B70?style=for-the-badge&logo=android&logoColor=white)](../../releases)
[![Architecture](https://img.shields.io/badge/Architecture-100%25_Offline_First-1763E8?style=for-the-badge)](./index.html)
[![Platform](https://img.shields.io/badge/Platform-Capacitor_6_%7C_Android-0875F9?style=for-the-badge&logo=capacitor&logoColor=white)](./.github/workflows/build-android.yml)
[![Languages](https://img.shields.io/badge/Languages-8_Indian_Languages-F59E0B?style=for-the-badge)](#multilingual-support)

**Bill Store (बिल स्टोर)** is an offline-first Android digital bill storage app and party-wise invoice organizer built for wholesalers, retailers, and shopkeepers. It keeps purchase bills, multi-page *parchas*, party folders, and date-wise party payment history organized in a private local database—without cluttering the phone's personal photo gallery or uploading sensitive business records to external cloud servers.

## ✨ Key Features

* **📸 Multi-Page Bill & Parcha Capture**: Snap or import multi-page invoices with instant client-side image compression, watermarks, pinch-to-zoom inspection, and full-screen viewing.
* **📁 Party-Wise Folders & Uncluttered Balance Tracker**: Automatically groups bills by wholesaler or shop name. Includes a clean 1-line **Paid & Balance Left** bar that opens a dedicated payment sheet to record date-wise payments and view saved payment dates.
* **🔍 Instant Search & Smart Date Filters**: Filter bills across the home dashboard, full-screen view, or inside specific party folders by note, amount, date presets (*Today, Yesterday, Last 7 Days, This Month*), or custom date ranges.
* **💬 Native WhatsApp Image + Caption Sharing**: Shares multi-page JPEG bill photos alongside structured party, amount, date, and note details directly to WhatsApp via Android `FileProvider` intents.
* **📊 Full-Fidelity Excel (CSV) Backup & Restore**: One-tap offline backup and restore (including embedded bill images) exported directly to the device's `Downloads` folder, paired with configurable **Weekly / Monthly Smart Backup Reminders**.
* **🌐 8 Indian Languages**: Full native interface localization in English, हिन्दी (Hindi), मराठी (Marathi), ગુજરાતી (Gujarati), ਪੰਜਾਬੀ (Punjabi), বাংলা (Bengali), தமிழ் (Tamil), and తెలుగు (Telugu).
* **🔒 100% Offline & Private by Design**: Powered by persistent `IndexedDB` + `localStorage` storage. Zero cloud tracking, zero external API dependencies, and zero personal gallery mixing.

## 🛠️ Tech Stack & Architecture

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend UI** | HTML5, Tailwind CSS, Lucide Icons | Responsive mobile-first fintech UI with dark mode support |
| **Storage Engine** | IndexedDB (`BillStoreUserDB_v2`) + LocalStorage | High-capacity offline persistence for multi-page compressed bill photos |
| **Native Runtime** | Capacitor 6 Android + Custom Java Bridge | Native `FileProvider` WhatsApp image sharing, hardware back-button routing, and `MediaStore` Downloads export |
| **CI/CD Pipeline** | GitHub Actions (`ubuntu-24.04`, JDK 21, Node 22) | Automated Gradle `assembleRelease` build signed with RSA-2048 v1/v2 production keystore |

## 📲 Downloading & Installing the Android APK

1. Open the **[Releases](../../releases)** tab of this repository (or the latest run under the **[Actions](../../actions)** tab).
2. Download **`BillStore.apk`** to your Android phone.
3. Tap to install. Because updates are signed with a persistent production release certificate, new versions install cleanly over existing versions without losing saved bills.

## 🔐 Privacy & Security Notice

Bill Store operates **100% offline**. All bill photos, notes, amounts, and party balances are processed and stored locally on your device. No personal or business data is ever transmitted to external servers.
