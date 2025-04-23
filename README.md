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

As you can see, **Persistent Live USB is more powerful**, but it requires more time and effort to configure.

---
## 2️⃣ Hardware Required

To create a Persistent Live USB, you'll need:

 ###  Hardware Options
 - **Option A — single-stick setup**  
   • One USB drive ≥ 32 GB (Rufus/Ventoy can add a persistence partition).  
 - **Option B — two-stick setup (easier for beginners)**  
   • *Installer USB* ≥ 8 GB • *Main USB* ≥ 32 GB  
 - **Any PC/laptop that can boot from USB**

---

###  Example Configuration Used:

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

## 3️⃣ Formatting and Writing ISO to a Flash Drive Using Rufus

First you need to prepare the first flash drive. For this purpose flash drive must be formatted and written with ISO file. You will have to download needed files and software in next steps.

---

**step 1)** **Insert First Flash Drive**  
Insert your first flash drive (for ISO only) into a USB port of your laptop or PC.

**step 2)** **Download Ubuntu ISO**  
Go to [Ubuntu Releases](https://releases.ubuntu.com/focal/) and download the desired version (e.g., Ubuntu 20.04).

**step 3)** **Download Rufus**  
Go to [Rufus Official Website](https://rufus.ie/ru/) and download suitable for you version of **Rufus**.
![Rufus Interface](images/slide10.png)

**step 4)** **Launch Rufus**  
Open the Rufus software. You will see a window with device and boot selection options.
![Rufus Interface](images/slide11.png)

**step 5)** **Select Your first Flash Drive**  
In the **Device** field, choose your flash memory (for ISO).

**step 6)** **Select ISO File**  
After selecting in “Boot selection” please choose “Disk or ISO” option. 

**step 7)** Press button “Select” and find your ISO file (which you downloaded from website)

ℹ️ Leave other parameters as default unless you know what you're doing.

⚠️ **Attention:**  
**Rufus will format your flash drive completely!**  
Make sure there are no important files on it.

**step 8)** **Click start button**  
If you are sure click “Start” button. Please, make sure that you have constant power supply because upload interrupt may cause problems. Also, next window can appear and please select ISO image mode: 

![Rufus Interface](images/slide12(1).png)

**step 9)** Wait a few minutes on USB 3.x (up to ~15 min on older USB 2.0).  
When Rufus shows **READY**, your installer stick is done:
![Rufus Interface](images/slide12(2).png)


✅ First flash drive is now ready!


## 4️⃣ Ubuntu Installation on the Second Flash Drive

In this section we will install Ubuntu on the second flash drive.  
Please be patient as this is the longest and most complicated part of the manual.

---

 **Step 1)** Insert two flash drives in USB ports  
 **Step 2)** Please, turn your PC (or laptop) off and during power-up, press the Boot Menu key (depending on the model).  
 **Step 3)** When Boot menu is opened you can see several options. Please select your flash memory with ISO file of Ubuntu  
(in my case it was called just “Ubuntu”).  

![Rufus Interface](images/slide14(1).png)

After this you will see GRUB menu like this and select first option – Ubuntu.

 **Step 4)** When you clicked on your Ubuntu you will see this screen and please select “Try Ubuntu” option.

 ![Rufus Interface](images/slide14(2).png)

 **Step 5)** After you selected “Try Ubuntu” option you will see next screen (it is desktop).  

 ![Rufus Interface](images/slide15.png)
 
 **Step 6)** Verify if laptop sees second flash drive (where we are going to install Ubuntu).  

For this purpose, find "Disks" (search via "Activities" → type Disks).  
There should be:  
- Your hard drive (500GB or similar)  
- USB stick with ISO image (first flash drive)  
- Your second flash drive (in my case 64GB Kingston) ← that's where we'll install Ubuntu.

 **Step 7)** Return to desktop. Click “Install Ubuntu 20.04 LTS” and in following windows choose next parameters:  
- Language — English  
- Keyboard layout  
- Connect Wi-Fi if you want.  

If after Wi-Fi connection you see this (image below), please look at section called “RST turning off”.  
If not, please continue following instructions.

 ![Rufus Interface](images/slide16.png)

 **Step 8)** After you set up Wi-Fi settings you will see this screen (image below).  

 ![Rufus Interface](images/slide17(1).png)
 
I chose normal installation with downloading updates.  
Click “Continue” after selecting suitable for you options.


 **Step 9)** After step 8 you will see this IMPORTANT screen. Please choose option “Something else”. If you chose “Erase disk and install Ubuntu” it will delete Windows OS! Be careful in this step

  ![Rufus Interface](images/slide17(2).png)

  **Step 10)** We clicked on “Something else” because we want to allocate memory on  second flash memory for correct working. After selecting “Something else” you will see this!

  ![Rufus Interface](images/slide18.png)
  
In “Device for boot installation” please select your second flash drive. In my case my flash drive Kingston 64GB is /dev/sdb. Also, you can understand if this is your flash drive by looking at memory capacity. If your memory stick is 64 GB, then in this menu you will see 61991 MB (nearly 64 GB).

**Step 11)** Choose string /dev/sdb  fat32 and press minus sign “-” to delete

**Step 12)** After deleting there will be "free space" under /dev/sdb

**Step 13)** Press on "free space" under /dev/sdb and click plus sign “+”

  ![Rufus Interface](images/slide19.png)

  After you pressed “+” this window appears

  Choose settings like in image except memory capacity. You can have capacity more or less than my, so consider this fact and write your own. In mount point always choose “\” option. Click OK after finishing.
**Step 14)** *Skip manual swap*—Ubuntu 20.04+ creates a swap **file** automatically.  
 Add a swap partition only if your PC has < 4 GB RAM and you know you need it.
**Step 15)** After you have done allocating memory, you can check your settings (image below) before approving allocation:

![Rufus Interface](images/slide21(1).png)

If everything is OK, press “Install now”

**Step 16)** After you pressed “Install now”, you see final window. You see how much memory you allocated for Ubuntu. Click “Continue” if you agree:

![Rufus Interface](images/slide21(2).png)

**Step 17)** After you clicked “Continue” it will ask your time zone. Please select your time zone. In my case I chose Almaty.

![Rufus Interface](images/slide22(1).png)

**Step 18)** Choose name, password and don’t forget them. Go “Continue” after you wrote down name and password. 

![Rufus Interface](images/slide22(2).png)

**Step 19)** After all was set up you will see screen of installation:

![Rufus Interface](images/slide23.png)

This process can require time for installing (from 15 minutes to 1 hour). If generation of USB flash drive is newest, if internet speed is high - installing can be much faster.

**Step 20)** After installation complete next window can appear:

![Rufus Interface](images/slide24(1).png)

Please, press “Restart now”.

**Step 21)** When you see “Remove the installation medium and press ENTER”:  
 1. Unplug **only** the installer USB.  
 2. **Keep** the main Ubuntu USB inserted.  
 3. Press **Enter** – the PC reboots into GRUB on that stick.

![Rufus Interface](images/slide24(2).png)

**Step 22)** After pressing Enter you will see GRUB menu:

![Rufus Interface](images/slide25.png)

Select Ubuntu. It is your Ubuntu installed to your second flash memory stick. 


✅ Installation has been completed!


---
## 5️⃣  Do I need to disable Intel RST?
*Usually not for a USB-only install.*  
RST only blocks **internal-disk** installs.  
If you later plan to dual-boot onto the laptop’s SSD, switch SATA mode to **AHCI** first; otherwise you can skip this step entirely.

**Step 1)** Please click “quit” (not restart) like in image:

![Rufus Interface](images/slide27(1).png)

**Step 2)** Turn off your laptop (PC)
**Step 3)** Open BIOS (press F2 during power-up)
**Step 4)** You will see information string like this (image below):

![Rufus Interface](images/slide27(2).png)


**Step 5)** Using arrows on your keyboard please select “Main”:
**Step 6)** Press Ctrl + S. This shortcut will reveal hidden parameters like SATA mode. 
**Step 7)** In SATA mode change "Optane without RAID" to “AHCI”.

✅ Now, you have turned RST mode off. You can continue Ubuntu installation

Return to desktop:
- Please turn laptop off
- open BIOS,
- select Ubuntu, 
- In GRUB menu select Ubuntu, 
- click “Try Ubuntu” to see desktop. 
- Do setting up again (language, keyboard layout, wifi)

---

## 6️⃣ Checking Ubuntu for functionality  

How to verify if my Ubuntu on second flash drive will work properly?

**Method 1**

- Please open “Files”. 
- Go in folder Documents or Desktop.
- Create any file (I created .txt file) and save it
- Turn off laptop
- Remove flash memory form your laptop
- Insert flash memory again
- Launch Ubuntu from GRUM menu.
- Open “Files” and verify if your created file is there. If yes flash memory with Ubuntu works properly. 


**Method 2**
- Also, you can check flash memory on working capability by connecting to WIFI network. If connects to it properly – your Ubuntu works. 


**Method 3**
- Also, you can check it by updates. Open terminal (Ctrl + Alt + T) and insert: 
sudo apt update && sudo apt upgrade
If system is being updated – your Ubuntu works properly.


**Method 4**
- You can download different programs. I successfully installed ROS with Gazebo and launched them. My flash drive worked.


---

## 7️⃣ How to return to Windows OS again?  

Most Windows 10/11 systems boot fine in **AHCI**.  
If Windows *does* fail, enter BIOS and switch **AHCI → Optane/RAID**, then be sure “Windows Boot Manager” is at the top of the boot list.

After you turned laptop off, removed flash memory with Ubuntu and powered it up you can receive this image (Grub rescue mode):

![Rufus Interface](images/slide31.png)

Just open BIOS menu, again find SATA mode option, change from “AHCI” to "Optane without RAID". This will help to load Windows OS properly. Shut down laptop and power it up again. After this you can again face with Grub rescue mode (look at image below):

![Rufus Interface](images/slide32.png)

Again, now you just need to:
- Turn off your laptop completely (hold the power button).
- Enter BIOS (on Acer, it's usually F2 during startup).
- Go to the Boot tab.
- Make sure Windows Boot Manager is first in the boot order.
If not — move it to the top using F5/F6.
- Save changes (F10, then Enter).
- Restart the laptop — Windows should boot up.


✅ This is the end of the instructions!

Made by: Adilet Toleshev, MS Student in Robotics (2025).
























