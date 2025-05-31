
# POCO M4 Pro 5G ADB Debloat Script

A minimal and effective **ADB-based debloat script** for the **POCO M4 Pro 5G**. This script removes unnecessary Xiaomi, Google, Facebook, and system bloatware to improve performance and reduce background activity — all **without root**.

> ⚠️ Use responsibly. This script is for advanced users. Always backup your data before proceeding.

---

## 📱 Supported Device

- **POCO M4 Pro 5G**
- Tested on MIUI 13/14 (Global ROM)

---

## 🚀 Features

- Removes MIUI ads, trackers, and system bloat
- Disables non-essential Google and Facebook services
- Preserves core system, dialer, messaging, and Play Store functionality
- Fully scriptable and easily editable
- No root or bootloader unlock required

---

## 🛠️ Requirements

- ADB installed on your computer ([Install ADB](https://developer.android.com/tools/adb))
- USB Debugging enabled on your phone
- A USB cable

---

## 📦 Apps Removed

The script removes bloatware from:

- **MIUI & Xiaomi system apps** (ads, analytics, tracking, cloud, gallery, screen recorder, etc.)
- **Google apps** (YouTube, Gmail, Maps, Assistant, Contacts, TTS, etc.)
- **Facebook bloat** (Facebook system services and pre-installed apps)
- **Miscellaneous overlays, services, and testing tools**

See the script (`POCO_M4PRO_5G.sh`) for the full list.

---

## 📂 Usage

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/poco-m4pro-debloat
cd poco-m4pro-debloat

# 2. Connect your phone with USB Debugging enabled
adb devices  # Make sure your device is listed

# 3. Run the script
bash POCO_M4PRO_5G.sh
````

The script will automatically uninstall all listed packages for the current user (`--user 0`).

---

## 🔁 Restore a Package (if needed)

If you accidentally removed an app you need, you can reinstall it (if it's still present in `/system`) with:

```bash
adb shell cmd package install-existing <package_name>
```

Example:

```bash
adb shell cmd package install-existing com.miui.gallery
```

---

## 🧠 Notes

* No logs are saved — this is a one-shot terminal script.
* This script is **non-interactive** — it runs through all removals in one go.
* Some Google services are excluded for safety (e.g., Play Services, Play Store, Dialer, etc.)
* You can comment/uncomment packages directly in the script to suit your needs.

---

## 📁 Repository Structure

```
poco-m4pro-debloat/
├── POCO_M4PRO_5G.sh     # Main debloat script
└── README.md            # This file
```

---

## 🙌 Credits

Created by [Rakesh](https://github.com/rax-2)
Inspired by open ADB debloat tools and custom ROM communities.

---


