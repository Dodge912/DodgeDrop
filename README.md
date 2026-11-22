<div align="center">

# ⚡ DodgeDrop

### **Next-Gen Wireless LAN File Sharing for Windows & Android**
*Experience the freedom of Apple AirDrop on Windows — powered by Native Google Quick Share.*

[![Release](https://img.shields.io/badge/Release-v1.0.0-3b82f6?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/Dodge912/DodgeDrop/releases)
[![Website](https://img.shields.io/badge/Website-Live%20Demo-10b981?style=for-the-badge&logo=googlechrome&logoColor=white)](https://dodge912.github.io/DodgeDrop/)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(64--bit)-0078d4?style=for-the-badge&logo=windows11&logoColor=white)](https://github.com/Dodge912/DodgeDrop)
[![Android](https://img.shields.io/badge/Android-Quick%20Share%20Native-34d399?style=for-the-badge&logo=android&logoColor=white)](https://github.com/Dodge912/DodgeDrop)
[![Speed](https://img.shields.io/badge/LAN%20Speed-Up%20to%20120%20MB%2Fs-f59e0b?style=for-the-badge&logo=speedtest&logoColor=white)](https://github.com/Dodge912/DodgeDrop)
[![Security](https://img.shields.io/badge/Security-E2EE%20UKEY2%20P--256-8b5cf6?style=for-the-badge&logo=auth0&logoColor=white)](https://github.com/Dodge912/DodgeDrop)
[![Author](https://img.shields.io/badge/Built%20by-DODGE-ec4899?style=for-the-badge)](https://github.com/Dodge912)

<br/>

[📥 Download Installer](#-download--installation) • [✨ Features](#-key-features) • [🚀 How Quick Share Works](#-how-quick-share-works-no-app-needed) • [📊 Comparison](#-comparison-matrix) • [🛡️ Security](#-built-in-security--anti-tamper-shield)

<br/>

```
      ┌─────────────────────────────────────────────────────────────────┐
      │  📱 Android Phone (Gallery / Files)                             │
      │     └─► Tap "Share" ──► "Quick Share"                           │
      │                             │                                   │
      │        Direct Local Wi-Fi   ▼ (Up to 120 MB/s • No Cloud)       │
      │                             │                                   │
      │  💻 Windows PC (DodgeDrop) ◄┘                                   │
      │     └─► Instant Popup Approval ──► Saved to Downloads Folder!   │
      └─────────────────────────────────────────────────────────────────┘
```

</div>

---

## 🌟 Why DodgeDrop?

Sharing large 4K videos, folders, and raw photos between an Android phone and a Windows PC has traditionally been clunky: slow Bluetooth transfers (0.5 MB/s), cloud storage upload limits, or hunting for USB cables.

**DodgeDrop solves this permanently.**

By implementing Google's native **Quick Share / Nearby Share** protocol directly inside Windows over your local home/office Wi-Fi router, you can beam files directly from your phone's native **Gallery Share menu** straight to your PC.

* 🚫 **No Android Apps or APKs needed**
* 🚫 **No Bluetooth required on your PC** (works over pure Ethernet LAN & Wi-Fi)
* 🚫 **Zero Cloud Uploads** (100% offline and private)
* ⚡ **Gigabit Speeds** (up to 120 MB/s over 5GHz/6GHz Wi-Fi)
* ♾️ **Unlimited File Sizes** (send 50 GB archives with zero compression)

---

## 🛠️ The "Quick Share Bluetooth Fix": How DodgeDrop Works Without Bluetooth

If you have ever tried using official Google Quick Share on a Windows desktop, you probably encountered this frustrating barrier:
> ⚠️ *"Your PC requires Bluetooth to use Quick Share"* or *"PC not showing up in Quick Share search"*.

### Why Standard Quick Share Fails on Many Windows PCs:
1. **Desktop PCs Lack Bluetooth Hardware**: Most custom gaming rigs, workstations, and office desktops connect via wired Ethernet LAN and have no Bluetooth / BLE card installed.
2. **Official App Enforces Bluetooth**: The standard Google Quick Share app refuses to accept transfers without an active Bluetooth Low Energy (BLE UUID `0xFE2C`) adapter.
3. **Bluetooth is Painfully Slow**: Even when Bluetooth works, transfer speeds rarely exceed 0.5 – 1.5 MB/s, making 4K video transfers virtually impossible.

### How DodgeDrop Solves It:
* 📡 **Direct Wi-Fi / Ethernet LAN Broadcast**: DodgeDrop advertises Google's native `_FC9F5ED42C8A._tcp.local.` service directly across your home or office router subnet.
* 📱 **Instant Phone Discovery**: When you set Quick Share visibility to **"Everyone"** on your Android phone, Android actively scans your local Wi-Fi and instantly shows your PC in the share list — **zero Bluetooth required on your PC**.
* ⚡ **Full LAN Gigabit Velocity**: Once you tap your PC, DodgeDrop opens a direct TCP socket and streams your files at **50 to 120 MB/s** (up to 100x faster than Bluetooth).

---

## ✨ Key Features

### 🟢 1. Native Google Quick Share Receiver
Your Windows PC appears directly on your Android phone's built-in Quick Share sheet. Select photos in Google Photos, Samsung Gallery, or any file manager, tap your PC's name, and receive files instantly with one click.

### 🌐 2. Universal Web & QR Code Transfer
Have an iPhone, iPad, Mac, Linux, or another computer? DodgeDrop includes an embedded Axum HTTP/WebSocket server. Simply scan the dynamic desktop QR code with your camera to open the DodgeDrop Web Portal directly in Safari or Chrome.

### 🏷️ 3. Customizable Discoverable Name
Change your PC's broadcast name on the fly (e.g. from `DODGE-PC` to `Living Room PC` or `Office Laptop`). Renaming immediately updates local network mDNS discovery.

### 🛡️ 4. Military-Grade UKEY2 Cryptography
Every transfer establishes an ephemeral Diffie-Hellman P-256 session and negotiates an encrypted tunnel with AES-256-GCM. An optional 4-digit verification PIN ensures complete transfer authenticity.

### 🔒 5. Anti-Tamper & Security Shield
DodgeDrop includes hardware-level anti-debugging protection, direct Windows Process Environment Block (PEB) validation, and full symbol stripping to guarantee process integrity.

---

## 🚀 How Quick Share Works (No App Needed!)

```
  Step 1                     Step 2                     Step 3
┌─────────────────────┐    ┌─────────────────────┐    ┌─────────────────────┐
│ 📸 Open Gallery     │    │ ⚡ Tap Quick Share  │    │ 💻 Tap Your PC Name │
│                     │    │                     │    │                     │
│ Select photos, 4K   │───►│ Choose "Quick Share"│───►│ Tap "DODGE-PC" and  │
│ videos, or folders  │    │ (Ensure visibility  │    │ accept the desktop  │
│ and tap Share.      │    │ is set to Everyone) │    │ popup prompt!       │
└─────────────────────┘    └─────────────────────┘    └─────────────────────┘
```

> **💡 Wi-Fi Tip**: Over pure Ethernet/Wi-Fi without Bluetooth hardware on the PC, set your phone's Quick Share visibility to **"Everyone"** (or tap *"Turn on for 10 minutes"*). This triggers your phone to actively discover local network devices.

---

## 📊 Comparison Matrix

| Feature | ⚡ **DodgeDrop** | 🔵 Windows Bluetooth | ☁️ Google Drive / OneDrive | 💬 WhatsApp / Telegram |
|:---|:---:|:---:|:---:|:---:|
| **Transfer Speed** | **50 – 120 MB/s** | 0.2 – 1.5 MB/s | Limited by Internet Upload | Capped & Throttled |
| **Internet Required?** | ❌ **No (100% Offline)** | ❌ No | ✅ Yes (Full Upload & Download) | ✅ Yes |
| **Phone App Required?** | ❌ **No (Native OS Share)** | ❌ No | ✅ Yes | ✅ Yes |
| **File Quality** | 💎 **100% Original Bit-for-Bit**| 💎 Original | 💎 Original | ❌ Compressed / Resized |
| **File Size Limit** | ♾️ **Unlimited** | Limited by patience | Quota Limits (15 GB) | 2 GB Max |
| **Cross-Platform (iOS/Mac)** | ✅ **Yes (via Web QR)** | ❌ No | ✅ Yes | ✅ Yes |

---

## 📥 Download & Installation

### Option 1: Download Release Installer
Download the latest Windows installer bundle directly from GitHub Releases:

* **[Download DodgeDrop Installer (.exe)](https://github.com/Dodge912/DodgeDrop/releases/latest/download/DodgeDrop_1.0.0_x64-setup.exe)** *(Recommended NSIS Setup)*
* **[Download DodgeDrop Package (.msi)](https://github.com/Dodge912/DodgeDrop/releases/latest/download/DodgeDrop_1.0.0_x64_en-US.msi)** *(Enterprise WiX Installer)*
* **[Download Portable DodgeDrop (.exe)](https://github.com/Dodge912/DodgeDrop/releases/latest/download/dodgedrop.exe)** *(No Install Needed)*

### Option 2: Portable Standalone Executable
If you prefer not to install, simply download `dodgedrop.exe` and run it directly. All web assets, icons, and database migrations are embedded inside the single executable!

### System Requirements
* **Operating System**: Windows 10 (1809+) or Windows 11 (64-bit)
* **Network**: Local Wi-Fi or Ethernet LAN router connection
* **Android**: Android 6.0+ (Samsung Galaxy, Google Pixel, Xiaomi, OnePlus, Motorola, etc.)
* **iOS / Other**: Any modern browser (Safari, Chrome, Firefox, Edge)

---

## 🛠️ Building from Source

If you want to compile DodgeDrop yourself from source:

### Prerequisites
1. [Node.js](https://nodejs.org/) (v18+)
2. [Rust & Cargo](https://rustup.rs/) (Stable 1.78+)
3. Microsoft Visual Studio 2022 C++ Build Tools

### Build Steps
```bash
# 1. Clone the repository
git clone https://github.com/your-username/DodgeDrop.git
cd DodgeDrop

# 2. Install frontend dependencies
npm install

# 3. Build optimized frontend
npm run build

# 4. Compile standalone release binary
npx tauri build --no-bundle

# Or build the full installer bundle (.exe & .msi)
npx tauri build
```

The resulting executables will be located in:
* Executable: `src-tauri/target/release/dodgedrop.exe`
* Installers: `src-tauri/target/release/bundle/nsis/` and `bundle/msi/`

---

## 🛡️ Built-in Security & Anti-Tamper Shield

DodgeDrop is compiled with industrial binary hardening to protect memory and user privacy:
* **Anti-Debugging Detection**: Active inspection of PEB `BeingDebugged` and `NtGlobalFlag` via direct 64-bit assembly (`mov rax, gs:[0x60]`).
* **Symbol Stripping**: All internal symbol names, variable tables, and line mappings are stripped (`strip = true`).
* **Fat Link-Time Optimization (`lto = "fat"`)**: Aggressive cross-crate inlining eliminates disassembly module boundaries.
* **DevTools Lockout**: Client-side right-click context menu and inspection shortcuts (`F12`, `Ctrl+Shift+I`) are suppressed in release builds.

---

## 👨‍💻 Author & Credits

Developed and designed with passion by **DODGE**.

* **Author**: DODGE
* **Application**: DodgeDrop
* **Engine**: Tauri 2 + Rust Tokio + React 19 + Tailwind CSS
* **License**: MIT License

---

<div align="center">
  <sub>Built with ❤️ by DODGE. Next-Generation Local LAN File Sharing.</sub>
</div>
