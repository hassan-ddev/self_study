# 🐧 Ubuntu Linux — Installation Guide
## Clean Step-by-Step Installation from Scratch

---

## 📦 What You Need Before Starting

| Item | Details |
|---|---|
| USB Flash Drive / Memory Card + Reader | Minimum 8GB |
| Rufus Application | For making USB bootable (Windows only) |
| Ubuntu ISO File | ~5.9GB download |

---

## ⚠️ Important Warning

> **Backup your data first.**
> This process **wipes all data** on your SSD/Hard Drive.
> Save all personal and important files to an external drive or cloud before proceeding.

---

## Step 1 — Download Rufus

Rufus is the tool that turns your USB into a bootable drive.

1. Open your browser
2. Search **"Rufus"**
3. Click the first link (rufus.ie)
4. Scroll down to the download section
5. Download **rufus-x.xx.exe** — standard version for Windows

---

## Step 2 — Download Ubuntu ISO

1. Open a new browser tab
2. Search **"Ubuntu download ISO"**
3. Click the first link (ubuntu.com)
4. Download the Ubuntu ISO file (~5.9GB)

> 💡 **Tip:** Do not save the ISO file on the USB you plan to make bootable. Save it to your local storage (e.g. Downloads folder).

---

## Step 3 — Make the USB Bootable with Rufus

1. Plug in your USB flash drive or memory card
2. Open Rufus
3. Configure it as follows:

| Setting | What to Select |
|---|---|
| Device | Select your USB drive (if multiple USBs are plugged in, select carefully) |
| Boot Selection | Browse and select your downloaded Ubuntu `.iso` file |
| Partition Scheme | **MBR** if your PC was manufactured **before 2015** |
| Partition Scheme | **GPT** if your PC was manufactured **after 2015** |

4. Click **Start**
5. Wait for the process to complete — this takes a few minutes
6. Your USB is now bootable ✅

---

## Step 4 — Boot from USB

1. **Shut down** your PC completely
2. Turn it back on and **immediately press `F12`** repeatedly
   - If `F12` doesn't work, try `Fn + F12` or `F2` / `Delete` (depends on manufacturer)
3. The **Boot Menu** will open
4. Select your USB drive from the list
5. Select **"Install Ubuntu"**

---

## Step 5 — Install Ubuntu

From here Ubuntu's installer guides you. You will be asked to choose:

- Language and keyboard layout
- Installation type (Erase disk and install Ubuntu — this is the full clean install)
- Timezone
- Username and password

Answer each screen and the installation will complete automatically.

---

## ✅ Done!

Once installation finishes, remove the USB when prompted and your system will restart into Ubuntu Linux.

---

*Ubuntu Installation Guide · Prepared by Hassan Shahzad · June 2026*
