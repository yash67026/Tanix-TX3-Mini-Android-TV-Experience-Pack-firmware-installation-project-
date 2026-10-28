# Tanix-TX3-Mini-Android-TV-Experience-Pack-firmware-installation-project-
A technical guide for installing Android TV Experience on the Tanix TX3 Mini, including firmware flashing, required drivers, setup, troubleshooting, and recovery procedures.
Installing Android TV Experience Pack on Tanix TX3 Mini

1. Verify the Hardware

Before flashing anything, confirm that the device is the original Tanix TX3 Mini with Amlogic S905W. Check the existing Android system under Settings → About and, if necessary, inspect the motherboard for the board/model information. Do not flash an S905W ROM onto the TX3 Mini+ S905W2 variant. An incompatible image can cause boot failure or a brick.

2. Required Files and Equipment

Prepare:
a. Compatible Android TV/ATV Experience .img ROM for TX3 Mini S905W
b. Link: https://drive.google.com/file/d/16YSotFxOmtXAPZfVvzHCXRQxOiianCdl/view
c. Amlogic USB Burning Tool, preferably the version recommended by the ROM.
d. Amlogic USB device drivers. These are normally installed together with the Burning Tool.
e. Windows PC.
f. USB-A-to-USB-A male-to-male data/OTG cable.
g. HDMI cable and the original power adapter.
h. Small paperclip/toothpick for operating the recovery button.
i. Keep a copy of the original Tanix stock firmware available before experimenting. Tanix's firmware centre currently lists the TX3 Mini S905W separately from newer TX3 Mini+ models.

3. Install the Burning Tool and Drivers

Extract the Amlogic USB Burning Tool package and run its installer as Administrator. During installation, allow the Amlogic USB drivers to be installed. Restart Windows afterward if requested.
Launch the Burning Tool. If its interface appears in Chinese, change the language to English from the menu.

4. Load the Android TV Image

a. Inside USB Burning Tool:
b. File → Import Image → select the compatible .img file
c. Wait for the image to finish verification. Do not start flashing until the image has been successfully loaded.

NOTE...!
For normal firmware flashing, leave options such as Erase Flash and Erase Bootloader at their default state unless the ROM's instructions specifically require them. The standard Amlogic procedure is to import the image, verify it, and then start the flashing process.

5. Enter Flashing/Recovery Mode

a. Completely power off the TX3 Mini.
b. Connect the OTG USB port of the TX3 Mini to the Windows PC using the USB data cable.
c. Insert a paperclip/toothpick into the AV port to locate the hidden reset/recovery button.
d. Press and hold the recovery button.
e. While holding it, connect the TX3 Mini's power adapter.
f. Continue holding the button for several seconds.
g. The Burning Tool should detect the device. The TX3 Mini's recovery button is commonly located inside the AV port.

NOTE...!
Once the device appears in the Burning Tool:
a. Confirm that the device has been detected.
b. Click Start.
c. Allow the firmware to transfer completely.
d. Do not disconnect USB.
e. Do not remove power.
f. Do not close the Burning Tool.
g. Wait until the progress reaches 100% and the tool reports Burning Successfully. The documented TX3 Mini procedure follows this exact sequence.
h. When successful, click Stop, close the tool, and disconnect the USB cable.

7. First Boot

a. Connect the TX3 Mini to the TV through HDMI and reconnect its original power adapter. The first boot after a complete ROM installation can take considerably longer than a normal boot.
b. Once Android TV starts:
c. Select language.
d. Connect to Wi-Fi/Ethernet.
e. Sign in with your Google account if supported by the ROM.
f. Configure the remote.
g. Check Settings → About.

Perform a factory reset only if the ROM documentation recommends it or if you experience problems after migration.

8. If the Box Is Not Detected

a. If USB Burning Tool does not detect the TX3 Mini:
b. Try another USB-A-to-USB-A data cable.
c. Try another USB port, preferably USB 2.0.
d. Reinstall the Amlogic drivers.
e. Run Burning Tool as Administrator.
f. Confirm that you are using the correct OTG port.
g. Power the box off completely and repeat the recovery-button procedure.
h. Try another Burning Tool version recommended for the particular ROM.
i. The PC does not need the TV box to display anything during the USB flashing process; detection occurs through the USB connection.

Recovery / Unbrick Procedure

a. If the TX3 Mini becomes stuck on the logo, bootloops, or produces a black screen after an unsuccessful flash, first attempt the normal recovery-button procedure again using the correct stock S905W firmware.
b. Download the correct original TX3 Mini S905W stock .img.
c. Open Amlogic USB Burning Tool.
d. Import the stock image.
e. Power the TX3 Mini off.
f. Connect its OTG port to the PC.
g. Hold the AV-port recovery button.
h. Apply power while continuing to hold the button.
i. Wait for the PC to detect the device.
j. Click Start.
k. Allow the stock firmware to reach 100%.
l. Click Stop.
m. Disconnect the USB cable.
n. Reconnect HDMI and power.
o. Allow several minutes for the first boot.
p. Amlogic's USB Burning Tool can also be used to restore damaged firmware and corrupted bootloaders.

Advanced Recovery

a. If the box is completely unresponsive and cannot enter USB recovery mode, some Amlogic boards can be forced into mask/USB boot mode by temporarily shorting specific test points on the motherboard while connecting USB. 
b. Do not guess the test points. They vary between boards. Obtain the exact TX3 Mini board revision and a verified test-point diagram before attempting this procedure.
c. Once the PC detects the device, the stock firmware can be flashed using USB Burning Tool. Advanced recovery documentation describes this technique for Amlogic devices, but the correct board-specific shorting points are essential.

Most important rule: never flash an image merely because it says “TX3 Mini.” Verify S905W + RAM/storage configuration + board revision first. Firmware compatibility is more important than the Android TV version itself.
