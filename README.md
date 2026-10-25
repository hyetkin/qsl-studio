# QSL Studio Pro v3.0.0

[![CI/CD — Multi-Platform Build & Release](https://github.com/hyetkin/qsl-studio-pro/actions/workflows/build_and_release.yml/badge.svg)](https://github.com/hyetkin/qsl-studio-pro/actions/workflows/build_and_release.yml)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-blue)](https://github.com/hyetkin/qsl-studio/releases/tag/v3.0.0)
[![Python](https://img.shields.io/badge/Python-3.11%20%7C%203.12-green.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-Proprietary%20%2F%20Amateur%20Radio-orange.svg)](#)

A modern, standalone cross-platform Amateur Radio Desktop Workstation for QSL Card Designing, WYSIWYG Drag-and-Drop Editing, Universal ADIF/CSV/Cabrillo Log Conversion, Printable A4 PDF Export, High-Speed Asynchronous E-QSL Delivery, QRZ Stealth Online Enrichment, Dual-Sided Studio, IARU Bureau Sorting & Shipping Label Generation, ClubLog Integration, and Real-Time Station Dashboard.

Developed by **Haluk Yetkin (TA2LE)**.

---

## 💻 Native Desktop Application (Installers)

QSL Studio Pro runs as a **native standalone desktop application** with zero Python setup required for end users:

* **Windows (10/11 x64):**
  * Installer: [`QSLStudio-v3.0.0-Setup-x64.exe`](https://github.com/hyetkin/qsl-studio/releases/tag/v3.0.0). Includes standard installation wizard, Start Menu/Desktop shortcuts, uninstaller, and automatic Windows Firewall rule for WSJT-X/N1MM UDP capture.
  * Portable: [`QSLStudio-v3.0.0-Windows-x64-Portable.zip`](https://github.com/hyetkin/qsl-studio/releases/tag/v3.0.0) (Standalone, no install needed).
* **macOS (Universal / Apple Silicon & Intel):** Open [`QSLStudio-v3.0.0-macOS-Universal.dmg`](https://github.com/hyetkin/qsl-studio/releases/tag/v3.0.0) and drag **QSL Studio.app** to your `/Applications` folder.
* **Linux (Ubuntu / Debian / Universal):**
  * **Debian / Ubuntu:** `sudo dpkg -i qsl-studio_3.0.0_amd64.deb`
  * **Universal Linux:** Download [`QSLStudio-v3.0.0-Linux-x86_64.AppImage`](https://github.com/hyetkin/qsl-studio/releases/tag/v3.0.0), run `chmod +x` and launch directly on any distribution.

---

## 🚀 Running from Source (Developers)

```bash
# Clone the repository
git clone https://github.com/hyetkin/qsl-studio-pro.git
cd qsl-studio-pro

# Set up Python virtual environment
python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Native Desktop Application
python app.py
```

> **Note for Headless / Browser Mode:**
> * By default, QSL Studio Pro launches in a dedicated **Native Desktop Window** (`pywebview`).
> * To open in your default web browser instead: `python app.py --browser`
> * To run in headless server mode (no window, no browser): `python app.py --no-browser` (binds to `http://127.0.0.1:8765`).

---

## ✨ Key Features (v3.0.0 Next-Gen)

1. **Native Desktop Window & Modern UI:**
   - Standalone window with hardware-accelerated rendering, clean shutdown on exit, and responsive high-DPI scaling.
   - Comprehensive **10-Language Support** (`en`, `tr`, `de`, `es`, `fr`, `it`, `ja`, `pt`, `nl`, `ru`).

2. **Visual Drag & Drop Card & Template Studio (WYSIWYG):**
   - **Dual-Sided Card Studio**: Seamless front and back design workflow with zero-config layout switching.
   - Upload custom station artwork or generate built-in templates (`Classic DX`, `POTA / SOTA`, `Modern Table`).
   - **Auto-Detect Boxes (`detect-fields`)** scans templates for write-in rectangles automatically using computer vision.
   - Live drag, resize, typography selection, QR Code positioning, and real-time rendered preview.

3. **IARU Bureau Sorter & Shipping Label Generator:**
   - Bundled offline directory of **183 Official IARU World QSL Bureaus**.
   - Intelligent relevance-based bureau lookup and hierarchical alias/prefix resolution.
   - Printable **IARU Bureau Parcel Shipping Labels (PDF)** with automated text-wrapping and society address formatting.
   - SASE / Self-Addressed Stamped Envelope generation.

4. **Log Ingestion & Station Management:**
   - Drag & drop `.adi`, `.adif`, `.csv`, `.log` (Cabrillo), `.adx` (XML), or `.json` logs.
   - Embedded SQLite Station Database (`qsl_studio.db`) with sub-millisecond indexed queries and multi-station profile switching.
   - 2-Way Confirmation Lifecycle tracking (Paper Sent/Received, Bureau Sent/Received, E-QSL Sent/Received).
   - Live Great Circle distance (`km`) and Azimuth compass bearing calculation from Maidenhead grids.

5. **Live Station HUD & Telemetry:**
   - Real-time station telemetry, solar conditions, propagation indices, and ClubLog API integration.
   - Real-time logger UDP listener capturing live QSOs from **WSJT-X**, **N1MM+**, **Logger32**, and **Log4OM**.

6. **Multi-Provider E-QSL Delivery Engine:**
   - **TA2LE Relay API:** High-speed asynchronous relay with server-side queue, rate-limiting, and hardware node-locking.
   - **Standard SMTP / TLS:** Compatible with Gmail, Outlook, custom mail servers.
   - **Microsoft 365 & Google OAuth2:** Secure cloud email integration via external browser authorization.
   - **IMAP Integration:** Auto-saves sent QSL cards to `Sent` folder and monitors `INBOX` to download received e-QSL cards into `output/received_qsls/`.

7. **Universal Log Converter & Print Production:**
   - Seamless two-way conversion between compact ADI, formatted ADIF, CSV, Cabrillo, and ADX.
   - Automatic byte-vs-character length correction for non-ASCII UTF-8 strings.
   - Print export: **A4 4-up QSL Cards PDF** (with crop marks) and **A4 24-up QSO / Address Labels PDF**.

8. **QRZ Stealth Online Enrichment:**
   - Human-paced querying (jitter & burst brakes) and session safety caps preventing Cloudflare rate limits.
   - Batch callsign deduplication slashing redundant traffic.

---

## 🛠️ Automated CI/CD & Multi-Platform Packaging

This project uses an automated GitHub Actions matrix workflow (`.github/workflows/build_and_release.yml`):
* **Quality Gate:** 238 automated unit, AppSec & integration tests run in parallel across Ubuntu, Windows, and macOS (Python 3.11 & 3.12).
* **Multi-Platform Build:** Automatically compiles Windows Inno Setup installers, macOS DMGs, and Linux .deb / AppImages.
* **Release Publishing:** Automated signing, checksum generation (SHA-256), and multi-platform binary asset attachment.
