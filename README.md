# Persistent-Live-USB-manual
In this manual you will see how to create Persistent Live USB
# 🐧 How to Create a Persistent Live USB (Ubuntu)

> This guide explains step-by-step how to install Ubuntu onto a flash drive **with persistence**, allowing you to carry a fully functional OS between machines.

---

## ⚠️ Warning

Please be aware:
- Instructions may vary depending on your device and manufacturer.
- **Read all steps carefully before taking action.**
- If something goes wrong, use ChatGPT or online forums to troubleshoot.

---

## 📚 Table of Contents

1. [Why Persistent Live USB?](#why-persistent-live-usb)
2. [Hardware Requirements](#hardware-requirements)
3. [Step 1: Format & Write ISO Using Rufus](#step-1-format--write-iso-using-rufus)
4. [Step 2: Install Ubuntu to Second Flash Drive](#step-2-install-ubuntu-to-second-flash-drive)
5. [RST Mode Fix (if needed)](#rst-mode-fix-if-needed)
6. [Check if Ubuntu Works Properly](#check-if-ubuntu-works-properly)
7. [How to Boot Back Into Windows](#how-to-boot-back-into-windows)
8. [Author](#author)

---

## Why Persistent Live USB?

- A **persistent Live USB** stores Ubuntu permanently on a flash drive.
- Unlike a regular bootable USB, this one can **save your files and settings**.
- Ideal for working on any PC without affecting internal storage.

---

## Hardware Requirements

- 🧊 **Flash Drive 1**: Used for the Ubuntu ISO. (e.g. 16–64 GB, USB 2.0+)
- 🔥 **Flash Drive 2**: Used for the actual Ubuntu system. (64 GB+ **USB 3.0 or 3.2 recommended**)
- 💻 A laptop or PC (e.g. Acer Aspire 7, Core i7 9th Gen was used)

📌 Notes:
- Make sure both flash drives are **empty**
- USB 3.0+ is recommended for speed
- 64 GB is optimal; smaller drives may fill up quickly
- Flash drive lifetime may decrease with daily use (due to heating)

---

## Step 1: Format & Write ISO Using Rufus

1. Insert **Flash Drive 1**.
2. Download Ubuntu ISO: [ubuntu.com/focal](https://releases.ubuntu.com/focal/)
3. Download [Rufus](https://rufus.ie)
4. In Rufus:
   - Select device
   - Choose "Disk or ISO"
   - Select your Ubuntu ISO
   - Keep default options
5. ⚠️ **Warning**: This will format the drive. Backup important data.
6. Click **Start**, choose "ISO image mode" if prompted
7. Wait ~15–20 minutes
8. ✅ Flash Drive 1 is now ready

---

## Step 2: Install Ubuntu to Second Flash Drive

1. Insert **both flash drives**
2. Reboot and enter Boot Menu (usually F12, F10, or Esc)
3. Select the USB with Ubuntu ISO → GRUB menu → Choose "Try Ubuntu"
4. Once in Ubuntu:
   - Open "Disks" to verify Flash Drive 2 is visible
   - Launch **Install Ubuntu 20.04 LTS**
   - Language: English, connect Wi-Fi
   - If you get a **storage error**, skip ahead to [RST Fix](#rst-mode-fix-if-needed)
5. Installation Options:
   - Choose **Normal installation**
   - IMPORTANT: Select **"Something else"** — NOT "Erase disk"!
6. Create partitions on Flash Drive 2:
   - Delete all partitions
   - Create:
     - `/` partition (root): e.g. 58 GB, ext4, mount point `/`
     - `swap`: e.g. 2 GB, swap area
7. Select device for bootloader: Flash Drive 2 (e.g. `/dev/sdb`)
8. Click **Install Now** → Confirm partition changes
9. Select time zone (e.g. Almaty), username, and password
10. Wait for installation (15–60 min) → Click **Restart Now**
11. Remove both flash drives → Insert only Flash Drive 2
12. Boot again → GRUB menu → Select Ubuntu  
✅ You're in! Ubuntu is installed on your second flash drive 🎉

---

## RST Mode Fix (If Needed)

If Ubuntu cannot see your drives or shows "No storage devices found", Intel RST (Rapid Storage Technology) might be the issue.

**How to fix it:**

1. Quit installer
2. Reboot → Enter BIOS (usually F2)
3. Press `Ctrl + S` in BIOS to reveal hidden SATA settings
4. Change **SATA Mode** from `"Optane without RAID"` to `"AHCI"`
5. Reboot → Try Ubuntu again

---

## Check if Ubuntu Works Properly

### ✅ Method 1: Save a File
- Save a `.txt` file in Documents
- Reboot → If file is still there, persistence works

### ✅ Method 2: Wi-Fi
- If Ubuntu connects to the internet, it works

### ✅ Method 3: Update System
```bash
sudo apt update && sudo apt upgrade
