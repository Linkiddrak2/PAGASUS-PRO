<div align="center">

```
         ██████╗ ███████╗ ██████╗  █████╗ ███████╗██╗   ██╗███████╗
         ██╔══██╗██╔════╝██╔════╝ ██╔══██╗██╔════╝██║   ██║██╔════╝
         ██████╔╝█████╗  ██║  ███╗███████║███████╗██║   ██║███████╗
         ██╔═══╝ ██╔══╝  ██║   ██║██╔══██║╚════██║██║   ██║╚════██║
         ██║     ███████╗╚██████╔╝██║  ██║███████║╚██████╔╝███████╗
         ╚═╝     ╚══════╝ ╚═════╝ ╚═╝  ╚═╝╚══════╝ ╚═════╝ ╚══════╝
```

# PEGASUS v1.3

**Android Device Management & Security Audit Tool**

[![Python](https://img.shields.io/badge/Python-3.7%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Windows%20%7C%20macOS-lightgrey?style=for-the-badge)](https://github.com/thakur2309/PAGASUS-PRO)
[![ADB](https://img.shields.io/badge/Requires-ADB-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/tools/adb)
[![Version](https://img.shields.io/badge/Version-1.3-orange?style=for-the-badge)](https://github.com/thakur2309/PAGASUS-PRO/releases)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/thakur2309/PAGASUS-PRO?style=for-the-badge)](https://github.com/thakur2309/PAGASUS-PRO/stargazers)

<br/>

> 🛡️ **For Educational & Personal Use Only**  
> Use only on devices you own or have explicit written permission to access.

<br/>

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Device Setup](#-android-device-setup) • [Changelog](#-changelog) • [License](#-license)

</div>

---

## 📌 What is Pegasus?

**Pegasus** is a powerful Python-based Android Device Management and Security Audit tool built on top of **ADB (Android Debug Bridge)**. It provides an interactive, color-coded terminal menu to remotely manage, monitor, analyze, and audit Android devices — entirely from your PC, with no third-party app required on the phone.

### Who is it for?

| Audience | Use Case |
|----------|----------|
| 🧑‍💻 Android Developers | Quick device control and log monitoring during development |
| 🔐 Security Researchers | Audit and assess your own device's security posture |
| 🎓 Students | Learn Android internals, ADB commands, and mobile security |
| 🖥️ Power Users | Manage and control phones wirelessly over Wi-Fi |

---

## ✨ Features

### 📱 Device Management

| Option | Feature | Description |
|--------|---------|-------------|
| 1 | **Check Device** | View model name, Android version, and battery level |
| 2 | **Connect Device** | Connect via USB or wirelessly over Wi-Fi (TCP/IP) |
| 3 | **Disconnect Device** | Cleanly disconnect wireless ADB sessions |
| 4 | **Screen Recording** | Record device screen and auto-pull to your PC |
| 5 | **Screen Mirror** | Live real-time screen mirroring via `scrcpy` |
| 6 | **Show APK List** | List all installed packages, export clean list to file |
| 7 | **Take Screenshot** | Capture and pull screenshot instantly |
| 8 | **Power Off** | Remotely power off the device |
| 15 | **Reboot Device** | Remotely reboot the device |
| 18 | **Toggle Wi-Fi** | Enable or disable device Wi-Fi remotely |
| 19 | **Check Storage** | View storage usage in human-readable format |
| 20 | **Take Photo** | Trigger camera, capture photo, and auto-pull to PC |
| 21 | **Troubleshoot** | Kill and restart ADB server for connection issues |
| 23 | **Connection History** | View session connect/disconnect timestamps |

### 📦 App Management

| Option | Feature | Description |
|--------|---------|-------------|
| 9 | **Install APK** | Sideload and install any `.apk` from your PC |
| 10 | **Delete APK** | Uninstall any package by its package name |
| 16 | **Start App** | Launch any installed application remotely |

### 📂 File Transfer

| Option | Feature | Description |
|--------|---------|-------------|
| 11 | **Pull File** | Copy any file from device storage to PC |
| 12 | **Push File** | Copy any file from PC to device storage |

### 📋 Data & Logs

| Option | Feature | Description |
|--------|---------|-------------|
| 13 | **Send SMS** | Open SMS intent with pre-filled number and message |
| 14 | **Dump Contacts** | Extract contacts (Name + Number), save to `.txt` |
| 17 | **Get Device Logs** | Pull full `logcat` dump and save locally |

### 🔐 Advanced Security Audit *(Option 22)*

> Unlocks a dedicated penetration testing and security audit submenu.

| Sub-Option | Feature | Description |
|-----------|---------|-------------|
| 1 | **Root Detection** | Detect if device has been rooted via multiple methods |
| 2 | **APK Permissions Dump** | List all dangerous permissions granted per installed app |
| 3 | **Device Security Audit** | Check patch level, encryption state, and build tags |
| 4 | **Debuggable Apps Scanner** | Identify debug-enabled apps (common security risk) |
| 5 | **Interactive ADB Shell** | Open a live terminal shell session on the device |
| 6 | **Network Security Check** | Inspect Wi-Fi security type + optional `nmap` scan |
| 7 | **Dump SMS / Call Logs** | Export messages and call records to `.txt` files |
| 8 | **Security Log Filter** | Filter `logcat` for permission denials and security events |
| 9 | **Vulnerability Scanner** | Compare patch date against known risk threshold |
| 10 | **Network Connections Monitor** | View active network connections via `netstat` |

---

## 💻 Installation

### ⚡ One-Line Quick Install

| Platform | Command |
|----------|---------|
| **Ubuntu / Debian / Kali** | `sudo apt install -y python3 adb scrcpy git && git clone https://github.com/thakur2309/PAGASUS-PRO.git && cd PAGASUS-PRO && python3 pegasus.py` |
| **Arch / Manjaro / BlackArch** | `sudo pacman -S python android-tools scrcpy git && git clone https://github.com/thakur2309/PAGASUS-PRO.git && cd PAGASUS-PRO && python3 pegasus.py` |
| **macOS** | `brew install python android-platform-tools scrcpy git && git clone https://github.com/thakur2309/PAGASUS-PRO.git && cd PAGASUS-PRO && python3 pegasus.py` |
| **Windows** | Install Python + ADB manually (see guide below), then run: `git clone https://github.com/thakur2309/PAGASUS-PRO.git && cd PAGASUS-PRO && python pegasus.py` |

---

### 🐧 Linux — Ubuntu / Debian / Kali

**Step 1 — Update system packages**
```bash
sudo apt update && sudo apt upgrade -y
```

**Step 2 — Install Python 3**
```bash
sudo apt install python3 python3-pip -y
```

**Step 3 — Install ADB**
```bash
sudo apt install adb -y
```

**Step 4 — Install scrcpy** *(optional — for Screen Mirror)*
```bash
sudo apt install scrcpy -y
```

**Step 5 — Install nmap** *(optional — for Network Security Scan)*
```bash
sudo apt install nmap -y
```

**Step 6 — Clone the repository**
```bash
git clone https://github.com/thakur2309/PAGASUS-PRO.git
cd PAGASUS-PRO
```

**Step 7 — Run Pegasus**
```bash
python3 pegasus.py
```

---

### 🔷 Linux — Arch / Manjaro / BlackArch

**Step 1 — Update system**
```bash
sudo pacman -Syu
```

**Step 2 — Install Python and ADB**
```bash
sudo pacman -S python android-tools
```

**Step 3 — Install scrcpy** *(optional)*
```bash
sudo pacman -S scrcpy
```

**Step 4 — Install nmap** *(optional)*
```bash
sudo pacman -S nmap
```

**Step 5 — Clone and run**
```bash
git clone https://github.com/thakur2309/PAGASUS-PRO.git
cd PAGASUS-PRO
python3 pegasus.py
```

---

### 🪟 Windows 10 / 11

**Step 1 — Install Python 3**

1. Download from: https://www.python.org/downloads/
2. Run the installer
3. ✅ **Check "Add Python to PATH"** before clicking Install

Verify in Command Prompt:
```cmd
python --version
```

**Step 2 — Install ADB (Android Platform Tools)**

1. Download from: https://developer.android.com/tools/releases/platform-tools
2. Extract the `.zip` to a folder (e.g., `C:\platform-tools\`)
3. Add to Windows PATH:
   - Press `Win + S` → Search **"Environment Variables"**
   - Click **"Edit the system environment variables"**
   - Click **"Environment Variables"** → Under System Variables, select `Path` → **Edit**
   - Click **New** → Enter `C:\platform-tools`
   - Click **OK** on all windows

Verify:
```cmd
adb version
```

**Step 3 — Install scrcpy** *(optional)*

1. Download from: https://github.com/Genymobile/scrcpy/releases
2. Extract to a folder (e.g., `C:\scrcpy\`)
3. Add `C:\scrcpy\` to PATH using same method above

**Step 4 — Install Git** *(if not installed)*

Download from: https://git-scm.com/download/win → Install with default options

**Step 5 — Clone and run**

Open **Command Prompt** or **PowerShell**:
```cmd
git clone https://github.com/thakur2309/PAGASUS-PRO.git
cd PAGASUS-PRO
python pegasus.py
```

> 💡 **Tip:** Use **Windows Terminal** (free from Microsoft Store) for best color rendering.

---

### 🍎 macOS — Intel & Apple Silicon (M1/M2/M3)

**Step 1 — Install Homebrew** *(if not installed)*
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

**Step 2 — Install Python 3**
```bash
brew install python
```

Verify:
```bash
python3 --version
```

**Step 3 — Install ADB**
```bash
brew install android-platform-tools
```

Verify:
```bash
adb version
```

**Step 4 — Install scrcpy** *(optional)*
```bash
brew install scrcpy
```

**Step 5 — Install nmap** *(optional)*
```bash
brew install nmap
```

**Step 6 — Clone and run**
```bash
git clone https://github.com/thakur2309/PAGASUS-PRO.git
cd PAGASUS-PRO
python3 pegasus.py
```

---

## 📱 Android Device Setup

USB Debugging must be enabled on your Android device before Pegasus can connect.

### Enable USB Debugging

```
Settings → About Phone
→ Tap "Build Number" 7 times rapidly
→ "You are now a developer!" message appears
→ Go back → Settings → Developer Options
→ Toggle ON "USB Debugging"
→ Connect phone to PC via USB
→ On phone popup: tap "Allow"
```

### Switch to Wireless Mode (Wi-Fi ADB)

> One-time USB setup required. After that, go fully wireless.

1. Connect device via USB cable
2. Launch Pegasus → Select **`[2] Connect a Device`**
3. Enter `y` when asked to enable TCP/IP mode
4. Find your device IP: **Settings → Wi-Fi → Tap connected network → IP Address**
5. Enter the IP in Pegasus when prompted
6. Unplug USB — connection is now wireless ✅

---

## 🚀 Usage

```bash
# Linux / macOS
python3 pegasus.py

# Windows
python pegasus.py
```

**Main Menu Preview:**

```
══════════════════════════════════════════════════════════════

[1] Check Device           [2] Connect a Device      [3] Disconnect Device

[4] Screen Recording       [5] Screen Mirror          [6] Show APK List

[7] Take Screenshot        [8] Power Off              [9] Install APK

[10] Delete APK            [11] Pull File             [12] Push File

[13] Send SMS              [14] Dump Contacts         [15] Reboot Device

[16] Start App             [17] Get Device Logs       [18] Toggle Wi-Fi

[19] Check Storage         [20] Take Photo            [q] Quit

[21] Troubleshoot Connection

[22] Unlock Advanced Security Tools

[23] View Device Connection History

══════════════════════════════════════════════════════════════
```

---

## 📂 Output Files

All generated files are saved in the **same directory** where you run the script.

| Filename | Generated By |
|----------|-------------|
| `screen.png` | Take Screenshot |
| `record.mp4` | Screen Recording |
| `apk_list.txt` | Show APK List |
| `contacts.txt` | Dump Contacts |
| `device_log.txt` | Get Device Logs |
| `storage_info.txt` | Check Storage |
| `sms_logs.txt` | Dump SMS (Security Tools) |
| `call_logs.txt` | Dump Call Logs (Security Tools) |
| `connection_log.txt` | Auto-generated connection session log |

---

## 📋 Dependency Summary

| Dependency | Required | Purpose | Install |
|-----------|----------|---------|---------|
| Python 3.7+ | ✅ Yes | Run the tool | `sudo apt install python3` |
| ADB | ✅ Yes | Device communication | `sudo apt install adb` |
| scrcpy | ⚪ Optional | Screen Mirror feature | `sudo apt install scrcpy` |
| nmap | ⚪ Optional | Network scan in Security Tools | `sudo apt install nmap` |
| Git | ⚪ Optional | Cloning the repository | `sudo apt install git` |

---

## 📝 Changelog

### v1.3 — Latest Release
- ✅ **Advanced Security Tools submenu** added (Option 22) — 10 features:
  - Root Detection (multi-method), APK Permissions Audit, Full Security Audit
  - Debuggable Apps Scanner, Interactive Shell, Network Security Check
  - SMS/Call Log Dump, Security Log Filter, Vulnerability Scanner, Network Monitor
- ✅ **Device Connection History** with timestamps and session duration (Option 23)
- ✅ **Multi-device support** — list and select when multiple devices detected
- ✅ **Selective wireless disconnect** — choose specific device or disconnect all
- ✅ **ADB Troubleshoot** — kill/restart ADB server to fix stuck connections (Option 21)
- ✅ **Improved contact dump** — clean `Name: Number` format parsing
- ✅ **Cleaner APK list** — shows only package names, no raw path clutter
- ✅ **Human-readable storage** — `df -h` for easy reading
- ✅ **Auto connection logging** — session log written on start and exit

### v1.2
- ✅ Expanded to full 20-option main menu
- ✅ Power Off and Reboot device remotely
- ✅ APK Install (sideload) and Uninstall
- ✅ File Push and Pull (two-way transfer)
- ✅ Send SMS via Android intent
- ✅ Dump device contacts
- ✅ Logcat device log dump
- ✅ Toggle Wi-Fi state on device
- ✅ Storage info check
- ✅ Remote camera trigger and photo pull
- ✅ `re` module added for contact parsing

### v1.1
- ✅ Check device info (model, Android version, battery)
- ✅ USB and Wi-Fi ADB connect and disconnect
- ✅ Screen recording with custom duration
- ✅ Live screen mirroring via scrcpy
- ✅ List installed packages and save to file
- ✅ Take and pull screenshot

### v1.0
- ✅ Initial release — basic ADB wrapper
- ✅ Interactive terminal menu UI
- ✅ Dependency checker on startup
- ✅ Color-coded terminal output (Linux/macOS)

---

## 📜 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2024 thakur2309

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## ⚠️ Disclaimer

> **Pegasus is developed strictly for educational and personal use.**
>
> - ✅ Only use this tool on Android devices **you own** or have **explicit written permission** to access.
> - ❌ Unauthorized access to someone else's device is **illegal** under cybercrime and privacy laws worldwide — including the IT Act (India), CFAA (USA), Computer Misuse Act (UK), and equivalent laws in other countries.
> - The developer (**thakur2309**) holds **zero liability** for any illegal, unethical, or unauthorized use of this software.
> - All data extraction features (contacts, SMS, call logs) are intended exclusively for **personal data backup** and **security research on your own device**.

---

## 🤝 Contributing

Contributions, bug reports, and feature suggestions are welcome!

1. Fork this repository
2. Create your branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "feat: add your feature"`
4. Push to branch: `git push origin feature/your-feature-name`
5. Open a **Pull Request**

---

## ⭐ Support the Project

If Pegasus helped you, please consider giving it a **⭐ star** on GitHub.  
It helps others find the project and motivates continued development.

---

<div align="center">

**Made with ❤️ by [thakur2309](https://github.com/thakur2309)**

*Stay ethical. Use responsibly.*

</div>
