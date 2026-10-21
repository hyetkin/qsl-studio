# QSL STUDIO PRO 📻

[![Release](https://img.shields.io/github/v/release/hyetkin/qsl-studio?color=blue&label=Latest%20Version)](https://github.com/hyetkin/qsl-studio/releases/latest)
[![Platform](https://img.shields.io/badge/Platforms-macOS%20%7C%20Windows%20%7C%20Linux-emerald)]()
[![License](https://img.shields.io/badge/License-Proprietary%20%2F%20Freeware-purple)]()

**QSL STUDIO PRO** is an advanced, standalone desktop workstation designed for amateur radio operators worldwide. It combines visual drag-and-drop QSL card designing, high-speed multi-format log conversion (ADIF, Cabrillo, CSV, EDI), batch card generation with subpixel typography, automated e-QSL emailing, and intelligent online QSO data enrichment.

Developed with passion by **Haluk Yetkin (TA2LE)**.

---

## ⚡ Direct Download Links (Latest v2.3.1)

Visit the [**Official GitHub Releases Page**](https://github.com/hyetkin/qsl-studio/releases/tag/v2.3.1) to download the package for your platform:

| Platform | Format | Description | Direct Download Link |
| :--- | :--- | :--- | :--- |
| 🍏 **macOS** | `.dmg` | Apple Silicon (M1/M2/M3/M4) & Intel Universal | [QSLStudio-v2.3.1-macOS-Universal.dmg](https://github.com/hyetkin/qsl-studio/releases/download/v2.3.1/QSLStudio-v2.3.1-macOS-Universal.dmg) |
| 🪟 **Windows (Setup)** | `.exe` | Windows 10 / 11 64-bit Installer | [QSLStudio-v2.3.1-Setup-x64.exe](https://github.com/hyetkin/qsl-studio/releases/download/v2.3.1/QSLStudio-v2.3.1-Setup-x64.exe) |
| 🪟 **Windows (Portable)**| `.zip` | Windows 10 / 11 64-bit Standalone (No Install) | [QSLStudio-v2.3.1-Windows-x64-Portable.zip](https://github.com/hyetkin/qsl-studio/releases/download/v2.3.1/QSLStudio-v2.3.1-Windows-x64-Portable.zip) |
| 🐧 **Linux (AppImage)** | `.AppImage` | Universal executable for all distributions | [QSLStudio-v2.3.1-Linux-x86_64.AppImage](https://github.com/hyetkin/qsl-studio/releases/download/v2.3.1/QSLStudio-v2.3.1-Linux-x86_64.AppImage) |
| 🐧 **Linux (DEB)** | `.deb` | Debian, Ubuntu, Linux Mint native package | [qsl-studio_2.3.1_amd64.deb](https://github.com/hyetkin/qsl-studio/releases/download/v2.3.1/qsl-studio_2.3.1_amd64.deb) |
| 🛡️ **Checksums** | `.txt` | SHA-256 package verification checksums | [SHA256SUMS.txt](https://github.com/hyetkin/qsl-studio/releases/download/v2.3.1/SHA256SUMS.txt) |

---

## 🌍 Multilingual Support & Documentation

QSL Studio Pro provides native internationalization adhering strictly to amateur radio conventions across 8 languages:
- 🇬🇧 **English** | 🇹🇷 **Türkçe** | 🇩🇪 **Deutsch** | 🇪🇸 **Español** | 🇯🇵 **日本語** | 🇮🇹 **Italiano** | 🇫🇷 **Français** | 🇵🇹 **Português**

Official operations manuals in vector PDF format are available for all 8 languages on the [Releases Page](https://github.com/hyetkin/qsl-studio/releases/tag/v2.3.1).

---

## 🌟 Key Features

- **🔍 RFC 2606 Clean Data Filtering:** Automatically detects and strips placeholder emails (`@example.com`, `@example.org.tr`, `.test`, `.invalid`), ensuring reliable email resolution and delivery.
- **🧭 CEPT & Multi-Station DXCC Resolver:** Comprehensive ITU prefix engine resolving Turkish call districts (1–0), US call areas, and portable/mobile/CEPT variants (`/P`, `/M`, `/MM`, `/4`, `DL/TA2LE`) into dedicated cards and accurate DXCC flags.
- **✉️ Selective Card & E-QSL Dispatching:** Interactive multi-select checkboxes, master toggle header, gallery selection tags, and quick filter pills (`All`, `Ready Only`, `Deselect All`) with dynamic recipient counts.
- **🔑 Multi-Station Security Key Vault:** Seamless token inheritance for base/portable variants (`TA2LE/P` shares `TA2LE` license) with encrypted at-rest storage and self-healing token verification.
- **🎨 Visual Drag & Drop Canvas Studio:** Interactive WYSIWYG canvas with magnetic smart alignment guides, layering controls, rotation, and typography styling.
- **🔄 Universal Log Converter:** Seamless two-way conversion across ADIF (`.adi`, `.adif`), Cabrillo (`.cbr`, `.log`), CSV, and EDI formats. Compatible with Log4OM, N1MM+, Logger32, HRD, WSJT-X, JTDX, and QRZ.com.
- **✉️ Automated E-QSL Mailer:** High-throughput batch email dispatcher supporting QSL Studio Pro Verified Relay, direct SMTP (Gmail, Outlook), and Microsoft 365 Graph API.
- **⚡ UDP Live Logger Bridge:** Intercepts real-time QSOs from WSJT-X, JTDX, and N1MM+ Logger via UDP multicast/unicast on ports `2237` / `2333`.
- **🏷️ Multi-Profile Station Manager:** Manage portable (`/P`), club (`YM2LE`), and mobile stations with custom gridsquares, QTHs, and default card designs.
- **🖨️ Multi-Card PDF Export:** Automatically composes 4 QSL cards per A4 sheet or prints standard 24-up Avery adhesive labels.
- **🚀 In-App Automatic Updates & Diagnostics:** Notifies you immediately when a new update is released, and features one-click sanitized diagnostic log exports for rapid support.

---

## 🐛 Feedback & Issue Reporting

Encountered an issue or have a feature idea?
- Open an issue on our [GitHub Issues Tracker](https://github.com/hyetkin/qsl-studio/issues).
- Send feedback or direct inquiries to: `qrz@ta2le.tr`.

---

## 📜 License & Copyright

© 2026 Haluk Yetkin (TA2LE). All rights reserved.  
Distributed as proprietary freeware for amateur radio operators worldwide.
