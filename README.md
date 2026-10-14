### ROOT-IMG-EXTRACTOR
<!-- ================= HEADER SECTION 

  <h1>⚡ Root IMG Extractor</h1>
  
  <p><strong>One Tap Firmware Image Extractor for Rooted Android Devices</strong></p>

  <!-- BADGES -->
  <a href="https://github.com/developer-x-store/ROOT-IMG-EXTRACTOR/releases/download/ROOT-IMG-EXTRACTOR/ROOT.IMG.EXTRACTOR_.apk">
    <img src="https://img.shields.io/badge/Download-APK-00FFFF?style=for-the-badge&logo=android" alt="Download APK">
  </a>
  <img src="https://img.shields.io/badge/Platform-Android_8.0+-3DDC84?style=for-the-badge&logo=android" alt="Platform">
  <img src="https://img.shields.io/badge/Language-Kotlin-7F52FF?style=for-the-badge&logo=kotlin" alt="Kotlin">
  <img src="https://img.shields.io/badge/Root-Magisk%20%7C%20KernelSU%20%7C%20APatch-FF0055?style=for-the-badge" alt="Root Required">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License">

  <br><br>
  
  <p>Stop typing complex commands in <b>Termux</b>. Extract <code>boot.img</code>, <code>vbmeta.img</code>, <code>vendor.img</code>, and <code>vendor_boot.img</code> directly from your device with a single tap using a beautiful Neon Cyberpunk GUI.</p>

</div>

---

> [!WARNING]
> ### 🚫 STRICT INSTALLATION NOTICE: MT MANAGER ONLY 🚫
> **এই অ্যাপটি সাধারণ Android Package Installer বা অন্য কোনো ফাইল ম্যানেজার (যেমন Google Files, Solid Explorer) দিয়ে ইনস্টল করা যাবে না।**
> 
> This APK is intentionally built with a modified signature and partition targeting. **It will ONLY install successfully via MT Manager (MT管理器).** If you try to install it using the standard Android installer or any other app, the installation will fail or show a "Package Parse Error".
> 
> **👉 How to install:**
> 1. Download the APK from the Releases section.
> 2. Open **MT Manager**.
> 3. Navigate to the downloaded APK file.
> 4. Tap on it and select **Install**.
> 5. Grant Root Permission when prompted by Magisk/KernelSU.

---

## 📖 Table of Contents
- [✨ Features](#-features)
- [📸 Screenshots](#-screenshots)
- [⚙️ How to Use](#️-how-to-use)
- [🛠️ Tech Stack](#️-tech-stack)
- [⚠️ Disclaimer](#️-disclaimer)
- [👨‍💻 Developer](#-developer)

---

## ✨ Features

- 🔒 **Smart Root Detection:** Automatically checks for Root access (Magisk, KernelSU, APatch). Blocks entry if Root is not granted.
- 📊 **Active Partition Scanner:** Scans `/dev/block/by-name/` to list all active partitions and their exact sizes.
- 🔀 **A/B Slot Detection:** Automatically detects the active slot (e.g., Slot A or Slot B) for seamless A/B device support.
- 🔍 **Real-time Filter:** Quickly search through dozens of partitions (e.g., type "vbmeta" or "boot").
- ☑️ **Batch Selection:** Select multiple files at once with "Select All" and "Deselect All" options.
- 📂 **Auto Extract Folder:** Creates a dedicated `Extractor` folder in your internal storage to save the dumped images.
- 🎨 **Cyberpunk Neon UI:** Full-screen, ad-free experience with premium Neon Red, Green, Blue, and Yellow glowing buttons.
- 🪶 **Ultra Lightweight:** Tiny APK size, minimal RAM usage, and zero battery drain.

---

## 📸 Screenshots

| Root Permission Check | Main Dashboard (Empty) | Partition List & Selection |
| :---: | :---: | :---: |
| <img src="YOUR_IMAGE_LINK_1" width="280" style="border-radius: 10px; border: 1px solid #FF0055;"> | <img src="YOUR_IMAGE_LINK_2" width="280" style="border-radius: 10px; border: 1px solid #00FFFF;"> | <img src="YOUR_IMAGE_LINK_3" width="280" style="border-radius: 10px; border: 1px solid #00FF00;"> |
| *Checks for Root access* | *Waiting for partition scan* | *Scanned 73 partitions with A/B slots* |

---

## ⚙️ How to Use

Follow these simple steps to extract your firmware images:

1. **Download & Install:** Download the APK from the [Releases](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME/releases) page. **Remember: Install it using MT Manager only!**
2. **Grant Root:** Open the app and grant Superuser (su) permission when prompted.
3. **Scan Partitions:** Tap the glowing **`CHECK PARTITION`** button at the top.
4. **Select Files:** Once the list populates, tap the download icon on the right side of the files you want to extract (e.g., `boot_a.img`, `vbmeta_a.img`).
5. **Extract:** Tap the **`SELECT FILES TO EXTRACT`** button at the bottom. 
6. **Done!** The files will be saved in `/Internal Storage/Extractor/`.

### 🔄 Workflow Diagram
```mermaid
graph TD;
    A[Launch App] --> B{Root Granted?}
    B -- No --> C[Show Error & Exit Button]
    B -- Yes --> D[Main Dashboard]
    D --> E[Tap CHECK PARTITION]
    E --> F[Scan /dev/block/by-name/]
    F --> G[Select .img files to extract]
    G --> H[Tap SELECT FILES TO EXTRACT]
    H --> I[(Save to /Extractor/ Folder)]
    I --> J[Success!]
