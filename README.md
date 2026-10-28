# Tanix TX3 Mini – Android TV Experience

A technical guide for installing **Android TV Experience** on the **Tanix TX3 Mini**, including firmware flashing, required drivers, setup, troubleshooting, and recovery/unbrick procedures.

> [!WARNING]
> **Verify your hardware before flashing.** This guide is intended for the **Tanix TX3 Mini based on the Amlogic S905W**. Do **not** flash an S905W firmware image onto a **TX3 Mini+ with S905W2**, as incompatible firmware can cause boot failure or permanently brick the device.

---

## Table of Contents

- [1. Hardware Verification](#1-hardware-verification)
- [2. Required Files and Equipment](#2-required-files-and-equipment)
- [3. Install USB Burning Tool and Drivers](#3-install-usb-burning-tool-and-drivers)
- [4. Load the Android TV Image](#4-load-the-android-tv-image)
- [5. Enter Flashing / Recovery Mode](#5-enter-flashing--recovery-mode)
- [6. Flash the Android TV Experience ROM](#6-flash-the-android-tv-experience-rom)
- [7. First Boot and Setup](#7-first-boot-and-setup)
- [8. Troubleshooting – Device Not Detected](#8-troubleshooting--device-not-detected)
- [9. Recovery / Unbrick Procedure](#9-recovery--unbrick-procedure)
- [10. Advanced Recovery](#10-advanced-recovery)
- [Important Notes](#important-notes)

---

## 1. Hardware Verification

Before flashing anything, verify that your device is the **original Tanix TX3 Mini with Amlogic S905W**.

You can check the hardware using:

- **Settings → About** on the existing Android installation.
- The processor/chipset information.
- RAM and internal storage configuration.
- The motherboard model/revision, if necessary.

Make sure the firmware matches the exact hardware configuration.

> [!CAUTION]
> Do not flash an **S905W** ROM onto a **TX3 Mini+ S905W2**. Firmware compatibility depends on the chipset, board revision, RAM/storage configuration, and other hardware components.

---

## 2. Required Files and Equipment

Prepare the following before starting:

### Firmware

- Compatible **Android TV / ATV Experience `.img` ROM** for the Tanix TX3 Mini S905W.

**Android TV Experience ROM:**

[Download Android TV Experience ROM](https://drive.google.com/file/d/16YSotFxOmtXAPZfVvzHCXRQxOiianCdl/view)

### Required Software

- **Amlogic USB Burning Tool**
- Compatible **Amlogic USB drivers**
- Windows PC

### Hardware

- USB-A-to-USB-A male-to-male **data/OTG cable**
- HDMI cable
- Original TX3 Mini power adapter
- Paperclip or toothpick for operating the recovery/reset button

### Recommended

Keep a complete copy of the **original Tanix stock firmware** before modifying the device. This can be used to restore the box if the Android TV installation fails.

> [!IMPORTANT]
> Make sure the USB cable supports **data transfer**. Charge-only cables will not allow the Burning Tool to communicate with the TX3 Mini.

---

## 3. Install USB Burning Tool and Drivers

1. Download and extract the **Amlogic USB Burning Tool** package.
2. Run the installer **as Administrator**.
3. Allow the Amlogic USB drivers to be installed when prompted.
4. Restart Windows if requested.
5. Launch **Amlogic USB Burning Tool**.
6. If the interface is displayed in Chinese, change the language to **English** from the appropriate menu.

Verify that the Burning Tool launches correctly before connecting the TX3 Mini.

---

## 4. Load the Android TV Image

1. Open **Amlogic USB Burning Tool**.
2. Select:

   **File → Import Image**

3. Select the compatible Android TV Experience `.img` file.
4. Wait while the tool loads and verifies the image.
5. Do not begin flashing until the image has been successfully loaded.

> [!NOTE]
> For a normal firmware installation, leave options such as **Erase Flash** and **Erase Bootloader** at their default settings unless the documentation supplied with the specific ROM instructs otherwise.

---

## 5. Enter Flashing / Recovery Mode

Follow these steps carefully:

1. Completely power off the TX3 Mini.
2. Connect the TX3 Mini's **OTG USB port** to the Windows PC using the USB data cable.
3. Locate the hidden recovery/reset button inside the **AV port**.
4. Using a paperclip or toothpick, **press and hold the recovery button**.
5. While continuing to hold the button, connect the TX3 Mini's original power adapter.
6. Continue holding the recovery button for several seconds.
7. The Amlogic USB Burning Tool should detect the device.

The recovery button is commonly located inside the AV port on the TX3 Mini.

> [!TIP]
> If the device is not detected, keep the recovery button pressed for a few additional seconds before releasing it.

---

## 6. Flash the Android TV Experience ROM

Once the TX3 Mini appears in the Burning Tool:

1. Confirm that the device has been detected.
2. Click **Start**.
3. Allow the firmware transfer to proceed.
4. Do **not** disconnect the USB cable.
5. Do **not** remove power from the TX3 Mini.
6. Do **not** close the Burning Tool.
7. Wait for the process to reach **100%**.
8. Confirm that the tool reports **Burning Successfully**.
9. Click **Stop**.
10. Close the Burning Tool.
11. Disconnect the USB cable.

> [!CAUTION]
> **Do not interrupt the flashing process.** Disconnecting USB, removing power, or forcibly closing the Burning Tool while the firmware is being written can corrupt the bootloader or system partitions.

---

## 7. First Boot and Setup

After successfully flashing the ROM:

1. Connect the TX3 Mini to the TV using HDMI.
2. Connect the original power adapter.
3. Turn on the TV and select the appropriate HDMI input.
4. Wait for Android TV to boot.

The first boot after a complete firmware installation may take considerably longer than a normal boot.

Once Android TV starts:

1. Select your preferred language.
2. Connect to Wi-Fi or Ethernet.
3. Sign in with your Google account, if supported by the ROM.
4. Configure the remote control.
5. Open **Settings → About** and verify the installed Android TV version.
6. Test Wi-Fi, Bluetooth, HDMI audio/video, remote controls, and other hardware functions.

Only perform a factory reset if recommended by the ROM documentation or if problems occur after migration.

---

## 8. Troubleshooting – Device Not Detected

If the Amlogic USB Burning Tool does not detect the TX3 Mini, try the following:

- Try another **USB-A-to-USB-A data cable**.
- Try another USB port on the PC.
- Prefer a **USB 2.0 port** when available.
- Reinstall the Amlogic USB drivers.
- Run the Burning Tool as Administrator.
- Confirm that you are using the correct **OTG USB port** on the TX3 Mini.
- Completely power off the TX3 Mini and repeat the recovery-button procedure.
- Try another compatible version of the Amlogic USB Burning Tool.
- Verify that the firmware is intended for the **S905W TX3 Mini**.

The TV box does not necessarily need to display anything while entering USB flashing mode. Communication with the PC occurs through the USB connection.

---

# 9. Recovery / Unbrick Procedure

If the TX3 Mini becomes stuck at the boot logo, enters a boot loop, or displays a black screen after an unsuccessful flash, attempt to restore the device using the correct **stock S905W firmware**.

### Procedure

1. Obtain the correct original **Tanix TX3 Mini S905W stock `.img`**.
2. Open **Amlogic USB Burning Tool**.
3. Select **File → Import Image**.
4. Load the stock firmware image.
5. Completely power off the TX3 Mini.
6. Connect the TX3 Mini's OTG port to the PC.
7. Press and hold the recovery button inside the AV port.
8. Connect the original power adapter while continuing to hold the button.
9. Wait for the PC and Burning Tool to detect the device.
10. Click **Start**.
11. Allow the stock firmware to reach **100%**.
12. Wait for **Burning Successfully**.
13. Click **Stop**.
14. Disconnect the USB cable.
15. Connect the HDMI cable.
16. Reconnect the power adapter.
17. Allow several minutes for the first boot.

The Amlogic USB Burning Tool can be used to restore damaged firmware and, depending on the condition of the device, recover corrupted system or bootloader components.

> [!IMPORTANT]
> Always use firmware specifically intended for your hardware revision. Do not use a random TX3 Mini firmware simply because the filename contains "TX3 Mini."

---

# 10. Advanced Recovery

If the TX3 Mini is completely unresponsive and **cannot enter normal USB recovery mode**, some Amlogic boards can be forced into **mask ROM / USB boot mode**.

This may involve temporarily shorting specific test points on the motherboard while connecting the device to a PC.

> [!CAUTION]
> **Do not guess or randomly short motherboard test points.** The locations differ between board revisions. Incorrectly shorting components or test points can permanently damage the device.

Before attempting advanced recovery:

1. Identify the exact TX3 Mini motherboard revision.
2. Obtain a verified board-specific test-point diagram.
3. Confirm the correct mask-ROM recovery procedure.
4. Disconnect the device from power before making any motherboard connections.
5. Proceed only when the correct test points have been positively identified.

Once the PC detects the device in mask/USB boot mode, the appropriate stock firmware can generally be flashed using the Amlogic USB Burning Tool.

---

# Important Notes

- **Always verify the chipset before flashing.**
- The original TX3 Mini and TX3 Mini+ are **not necessarily firmware-compatible**.
- Verify **S905W + RAM + storage + board revision** before selecting a ROM.
- Keep the original stock firmware as a recovery option.
- Use a reliable USB data cable.
- Do not interrupt the flashing process.
- Do not disconnect power while firmware is being written.
- Back up important data before modifying the device.
- Android TV functionality can vary depending on the ROM, Google certification, DRM/Widevine support, and hardware configuration.

> [!WARNING]
> **Firmware flashing is performed at your own risk.** The author of this guide is not responsible for device damage, data loss, bootloader corruption, or bricking caused by incorrect firmware, interrupted flashing, incompatible hardware, or improper recovery procedures.

---

## Credits & References

- [Amlogic USB Burning Tool – CoreELEC Wiki](https://wiki.coreelec.org/coreelec%3Aaml_usb_tool)
- [TX3 Mini Firmware / Resources](https://www.tanixtvbox.com/firmware-centre/)
- [i12bretro – Tanix TX3 Mini Guides](https://i12bretro.github.io/tutorials/0302.html)

---

## Disclaimer

This repository is intended for **educational and technical reference purposes**. Always verify firmware compatibility with the exact hardware revision of your device before flashing.
