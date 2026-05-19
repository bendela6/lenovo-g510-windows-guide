# How to Reinstall Windows on a Lenovo G510

A simple, step-by-step guide. No tech jargon.

## What you need before you start

1. **A USB stick** — at least 8 GB. Everything on it will be erased.
2. **Another working computer** — to make the USB stick.
3. **Power cable** for your Lenovo G510 (do not run on battery during install).
4. **Internet** — Wi-Fi password if you have one.
5. **About 1–2 hours** of free time.

> **Recommended:** Install **Windows 10 (64-bit)**. The G510 is from 2013, so Windows 11 is not officially supported (it works with tricks, but Windows 10 is easier and gets security updates until October 2025... after that, see the note at the bottom).

---

## STEP 1 — Back up your files

Reinstalling Windows **erases everything** on the C: drive.

- Copy important files (photos, documents, downloads) to an external drive, another USB, or the cloud (Google Drive, OneDrive, Dropbox).
- Don't forget: browser bookmarks, saved passwords (export them), and any program license keys.

---

## STEP 2 — Make the Windows USB installer

Do this on **any working computer**.

1. Plug your empty USB stick into the working computer.
2. Open a web browser and go to:
   **https://www.microsoft.com/software-download/windows10**
3. Click **"Download tool now"** (Media Creation Tool).
4. Open the downloaded file. Click **Accept**.
5. Choose **"Create installation media (USB flash drive...) for another PC"**. Click **Next**.
6. Leave the defaults (Language, Edition, 64-bit). Click **Next**.
7. Choose **"USB flash drive"**. Click **Next**.
8. Pick your USB stick from the list. Click **Next**.
9. Wait. It will download Windows and put it on the USB (15–30 minutes).
10. When it says "Your USB flash drive is ready", click **Finish**.

Safely eject the USB. Done.

---

## STEP 3 — Plug the USB into the Lenovo G510

1. **Shut down** the G510 completely (not sleep — fully off).
2. Plug in the **power cable**.
3. Plug the **USB stick** into a USB port on the G510.

---

## STEP 4 — Boot from the USB stick

The G510 has a little secret button called the **Novo button**. It's a tiny pinhole, usually on the **left side** of the laptop near the power cable, with a small curved arrow icon.

1. Make sure the laptop is **OFF**.
2. Take a paperclip or pin and **gently press the Novo button** for 1 second.
3. The laptop will turn on and show a menu like this:
   - Normal Startup
   - BIOS Setup
   - Boot Menu
   - System Recovery
4. Use the arrow keys to pick **"Boot Menu"** and press **Enter**.
5. You'll see a list of drives. Pick the one that says **"USB HDD"** or your USB stick's name. Press **Enter**.

> **Doesn't see the USB?** Pick "BIOS Setup" instead, go to the **Boot** tab, change **"Boot Mode"** to **UEFI** (or try **Legacy Support** if UEFI doesn't work), set **"Boot Priority"** to **Legacy First** if needed, press **F10** to save and exit, then try the Novo button again.

---

## STEP 5 — Install Windows

The Windows installer will start. Take your time — each screen is simple.

1. **Language / Time / Keyboard** — Leave defaults. Click **Next**.
2. Click **"Install now"**.
3. **Product key screen** — Click **"I don't have a product key"** (Windows will activate later automatically if it was activated before on this laptop).
4. **Pick edition** — Choose **Windows 10 Home** (or Pro if that's what you had). Click **Next**.
5. **License terms** — Tick the box. Click **Next**.
6. Choose **"Custom: Install Windows only (advanced)"**. ← This is the important one.
7. **Pick the drive**. You'll see a list of partitions:
   - **WARNING:** This is the step that erases your data.
   - Click each partition (Drive 0 Partition 1, 2, 3, etc.) and click **Delete** for each one — until you see just **"Drive 0 Unallocated Space"**.
   - Click on **"Drive 0 Unallocated Space"** and click **Next**.
8. **Wait.** Windows will copy files and restart a few times by itself (20–40 minutes). Don't touch anything. If it asks to boot from USB again, **don't** — let it boot from the hard drive.

> **If it keeps booting from USB:** Pull the USB out after the first restart.

---

## STEP 6 — First-time setup

After it restarts, you'll see the blue setup screens.

1. Pick your **region** (country). Click **Yes**.
2. Pick your **keyboard layout**. Click **Yes**, then **Skip** for the second one.
3. Connect to **Wi-Fi** (enter your password).
4. Choose **"Set up for personal use"**. Click **Next**.
5. **Sign in with a Microsoft account** — enter your email and password.
   - **No Microsoft account?** Click "Offline account" or "Create account" in the bottom corner.
6. Create a **PIN** (4+ digits) for quick login.
7. **Privacy settings** — turn things off if you want more privacy. Click **Accept**.
8. Skip Cortana, OneDrive, Office trial offers (click "No"/"Skip" on each).
9. Wait while it finishes ("This may take a few minutes...").

You'll land on the desktop. 🎉

---

## STEP 7 — Install drivers (important!)

Windows installs most drivers automatically, but a few G510-specific ones improve performance.

1. Open Edge browser. Go to:
   **https://support.lenovo.com**
2. Type **"G510"** in the search box.
3. Pick **"Lenovo G510 Laptop (IdeaPad)"**.
4. Click **"Drivers & Software"** → **"Manual Update"**.
5. Download and install (one at a time):
   - **Chipset driver** (Intel)
   - **Graphics / VGA driver**
   - **Wireless LAN driver** (if Wi-Fi isn't working)
   - **Audio driver** (if no sound)
   - **Bluetooth driver**

> **Easier option:** Skip this step and let **Windows Update** handle it. Open **Settings → Update & Security → Windows Update → Check for updates**. Run it 2–3 times until nothing new shows up.

---

## STEP 8 — Update Windows

1. Click **Start** → **Settings** (gear icon) → **Update & Security**.
2. Click **Check for updates**.
3. Let it download and install everything. This takes a while.
4. Restart when asked.
5. Repeat until it says "You're up to date".

---

## STEP 9 — Install your programs

Reinstall what you use:
- **Browser:** Chrome, Firefox, etc.
- **Microsoft Office** (if you have a license)
- **VLC** (plays any video)
- **7-Zip** (opens .zip and .rar files)
- **Your printer's driver** (from the printer's brand website)

Copy your backed-up files back from your external drive.

---

## Common problems

**Q: USB stick doesn't show up in Boot Menu.**
A: Go into BIOS Setup (Novo button → BIOS Setup) → Boot tab → enable **Legacy Support** AND set **Boot Priority** to **Legacy First**. Save with F10. Try again.

**Q: "We couldn't create a new partition" error.**
A: Unplug all USBs except the install one. Or, in the partition step, delete ALL partitions until only one big "Unallocated Space" remains.

**Q: No Wi-Fi after install.**
A: Use a wired Ethernet cable temporarily, run Windows Update, OR download the wireless driver on another computer from Lenovo's site and copy it over with a USB.

**Q: Screen is huge / low resolution.**
A: Means graphics driver isn't installed yet. Run Windows Update or install it from the Lenovo site.

**Q: Laptop is slow after install.**
A: Wait 30 minutes after first boot — Windows runs background tasks. Also: the G510 will be MUCH faster with an **SSD** ($25 upgrade) replacing the old hard drive.

---

## Note about Windows 11

Windows 10 security updates end **October 14, 2025**. After that:
- **Easiest:** Keep using Windows 10 — it still works, just no new security patches.
- **Or:** Install Windows 11 using a workaround tool called **Rufus** (it skips the CPU check). Search "install Windows 11 on unsupported PC Rufus" for guides.

---

## Quick reference

| What | Key |
|---|---|
| Open Boot Menu | **Novo button** (pinhole) or **F12** |
| Open BIOS | **Novo button** → BIOS Setup, or **F2** |
| Save BIOS settings | **F10** |
| Cancel / Back | **Esc** |

---

**You're done!** Take your time on each step. If something looks wrong, stop and re-read — don't click randomly. Good luck. 🛠️
