#  How to Create a Persistent Live USB (Ubuntu)

> This is a short manual on how to set up a **Persistent Live USB**, allowing you to run Ubuntu with saved files and settings on any device — portable and powerful.

---

## ⚠️ Warning

You may encounter problems when following the instructions. Please understand that things may look different on different devices from different manufacturers, so use ChatGPT and other tools to solve unexpected problems.
Also, before taking action, please read the instructions first!


---

## 📚 Structure of the Manual

- 1️⃣ Why Persistent Live USB?  
- 2️⃣ Hardware required  
- 3️⃣ Formatting and writing ISO to a flash drive using Rufus  
- 4️⃣ Ubuntu installation on second flash drive  
- 5️⃣ RST turning off  
- 6️⃣ Checking Ubuntu for functionality  
- 7️⃣ How to return to Windows OS again?  

---

## 1️⃣ Why Persistent Live USB?

There are several ways to run Ubuntu:

- Install it alongside Windows
- Use it in a virtual machine
- Run it as a **bootable USB**

But this tutorial teaches you how to create a **Persistent Live USB**.

With a Persistent Live USB:

- Ubuntu is **stored on your flash drive**
- You can **work on any device**, keeping files, programs, and settings
- You are **not dependent on any specific computer**
- It works **like a mini portable Linux system**

## Comparison: Bootable Flash vs Persistent USB

| Property                | Bootable Flash | Persistent USB |
|------------------------|----------------|----------------|
| Saves data             | ❌ No          | ✅ Yes         |
| Can install programs   | ❌ No          | ✅ Yes         |
| Used for installation  | ✅ Yes         | ✅ Yes         |
| Suitable for daily use | ❌ No          | ✅ Yes         |
| Resource usage         | 🟢 Low         | 🟡 Medium      |


As you can see, **Persistent Live USB is more powerful**, but it requires more time and effort to configure.

---
## 2️⃣ Hardware Required

To create a Persistent Live USB, you'll need:

### 🔧 Basic Requirements:
- **First flash memory** — For the Ubuntu ISO file (used only for installation).
- **Second flash memory** — For installing and running Ubuntu itself.
- **Laptop or PC** — Any device that supports booting from USB.

---

### 🧪 Example Configuration Used:

- **First Flash Memory:**  
  USB 2.0, 64GB, Apacer AH333 (can be even 16 GB, just enough for ISO file)

- **Second Flash Memory:**  
  64GB Kingston DataTraveler Exodia M, USB 3.2

- **Laptop:**  
  Acer Aspire 7, Core i7, 9th Gen  

---

### ⚠️ Important Recommendations:

- **Empty Drives:**  
  Make sure both flash drives are empty — all data will be erased.

- **USB Speed Matters:**  
  Use USB 3.0 or higher for the **second** flash drive (Ubuntu itself) to ensure fast installation and usage.

- **Storage Size:**  
  Avoid using flash drives below 32 GB — it will cause issues with saving files.  
  **Recommended size: 64 GB**

- **Durability Note:**  
  Running Ubuntu directly from a flash drive causes heat, which can reduce the flash drive’s lifespan.

---

## 💾 Formatting and Writing ISO to a Flash Drive Using Rufus

This step prepares the **first flash drive** for Ubuntu installation by writing the ISO file onto it.

---

step ① **Insert First Flash Drive**  
Insert your first flash drive (for ISO only) into a USB port of your laptop or PC.

---

step ② **Download Ubuntu ISO**  
Go to [Ubuntu Releases](https://releases.ubuntu.com/focal/) and download the desired version (e.g., Ubuntu 20.04).

---

step ③ **Download Rufus**  
Go to [Rufus Official Website](https://rufus.ie/ru/) and download the latest version of **Rufus**.

---

step ④ **Launch Rufus**  
Open the Rufus software. You will see a window with device and boot selection options.

---

step ⑤ **Select Your Flash Drive**  
In the **Device** field, choose your flash memory (for ISO).

---

step ⑥ **Select ISO File**  
In the **Boot selection** field, choose `Disk or ISO image`, then press `Select` and pick your downloaded ISO file.

ℹ️ Leave other parameters as default unless you know what you're doing.

---

⚠️ **Attention:**  
**Rufus will format your flash drive completely!**  
Make sure there are no important files on it.

---

step ⑦ **Start the Process**  
Click `Start`. When a prompt appears, choose **ISO Image Mode**.

---

step ⑧ **Wait for Completion**  
It will take approximately **15–20 minutes**.  
Once finished, the flash memory will contain the bootable Ubuntu ISO.

✅ First flash drive is now ready!
