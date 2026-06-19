# 📱 Phone Repair Toolkit — Windows Installation

## ✅ What's included

- **`PhoneRepairToolkit.exe`** — Main executable (177 MB)
- All required Electron runtime DLLs
- Bundled HTML/CSS/JS (no Node.js installation required on the target PC)

**Total folder size**: ~255 MB (uncompressed)
**Compressed**: ~104 MB (ZIP)

## 📥 Installation

### Method 1: Run directly (Portable — No installation required)

1. Extract the ZIP file to any folder, e.g., `C:\PhoneRepairToolkit\`
2. Open the folder
3. Double-click **`PhoneRepairToolkit.exe`**
4. The app opens — no installation, no admin rights needed

> **Tip**: You can also run it from a USB drive.

### Method 2: Create a desktop shortcut

1. Right-click on `PhoneRepairToolkit.exe` → **Send to** → **Desktop (create shortcut)**
2. Double-click the desktop shortcut to launch

### Method 3: Add to Start Menu (manual)

1. Press `Win + R`, type `shell:start menu` and press Enter
2. Create a new folder called "Phone Repair Toolkit"
3. Copy `PhoneRepairToolkit.exe` and the entire folder there
4. Right-click → Create shortcut

## ⚙️ System Requirements

- **OS**: Windows 10 / 11 (64-bit)
- **RAM**: 4 GB minimum, 8 GB recommended
- **Disk**: 500 MB free space
- **ADB**: Required for connecting to Android devices
  - Download from: https://developer.android.com/tools/releases/platform-tools
  - Extract and add to PATH
  - Or place `adb.exe` in the same folder as `PhoneRepairToolkit.exe`

## 🚀 First Run

1. Launch `PhoneRepairToolkit.exe`
2. The main window opens with the sidebar
3. Click **"🔌 ADB Console"** in the sidebar
4. Connect your Android phone via USB with USB debugging enabled
5. The device should appear in the dropdown within 5 seconds

## 🔌 ADB Console Features

| Feature | Description |
|---|---|
| **Device List** | Auto-refresh every 5 seconds, shows model + Android version + battery |
| **Quick Commands** | 12 preset commands (device info, battery, storage, processes, etc.) |
| **Custom Commands** | Type any `adb shell` command, press Enter to execute |
| **Streaming** | `Ctrl+Enter` to stream long-running commands (logcat, etc.) |
| **Command History** | `↑` / `↓` arrow keys to recall previous commands |
| **Live Output** | See results in real-time with timestamps and duration |
| **Cancel** | Stop streaming commands mid-execution |
| **File Transfer** | Push / pull files to/from device |
| **APK Install** | Install APK files on connected device |
| **Reboot** | System / Recovery / Bootloader / EDL modes |
| **Device Info** | Model, manufacturer, build number, fingerprint, security patch |
| **Battery** | Level, temperature, voltage, status, health |
| **Storage** | df -h on /data, /system, /sdcard |
| **Processes** | Top 100 running processes |
| **Screenshot** | Capture device screen and save as PNG |

## 🔒 Security Notes

- The app runs **locally** — no data sent to external servers
- USB device access is restricted to **whitelisted vendors** (MediaTek, Qualcomm, Samsung, etc.)
- Sensitive values (IMEI, serial numbers) are **masked** in any logging
- For legitimate device repair only — see EULA in the app's About menu

## ⚠️ Windows SmartScreen Warning

When running for the first time, Windows may show:
> "Windows protected your PC — Microsoft Defender SmartScreen prevented an unrecognized app from starting"

This is normal for unsigned apps. To run:
1. Click **"More info"**
2. Click **"Run anyway"**

The app is safe — it's just not code-signed yet. For production deployment, sign it with an EV Code Signing Certificate.

## 🆘 Troubleshooting

| Problem | Solution |
|---|---|
| "adb: command not found" | Install Android Platform Tools and add to PATH |
| Device not detected | Enable USB debugging: Settings → About phone → tap Build number 7 times → Developer options → USB debugging |
| Device shows as "unauthorized" | Accept the RSA fingerprint dialog on the phone |
| App won't start | Install [Visual C++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe) |
| Antivirus flags the app | Add exception in your antivirus for the app folder |

## 📞 Support

For issues or questions, contact the development team.

---

**Version**: 0.2.0
**Build date**: 2026-06-16
**Electron version**: 30.5.1
**Target platform**: Windows 10/11 x64
