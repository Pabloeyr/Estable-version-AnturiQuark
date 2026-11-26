<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="branding/logo-dark.png">
    <img src="branding/logo-light.png" alt="Anturi" width="460">
  </picture>
</p>

<h2 align="center">Anturi Quark App</h2>
<p align="center">Android app to run electrochemical measurements on the Anturi Quark over Bluetooth Low Energy</p>

---

<p align="center">
  <a href="https://anturi.cl/"><img src="https://img.shields.io/badge/Website-anturi.cl-0B2033?style=flat" alt="Website anturi.cl"></a>
  <a href="https://www.linkedin.com/company/anturi/"><img src="https://img.shields.io/badge/LinkedIn-Anturi-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn Anturi"></a>
  <img src="https://img.shields.io/badge/App-1.2.0-0B2033?style=flat" alt="App 1.2.0">
  <img src="https://img.shields.io/badge/Firmware-3.21.6-0B2033?style=flat" alt="Firmware 3.21.6">
  <img src="https://img.shields.io/badge/Android-7.0%2B-3DDC84?style=flat&logo=android&logoColor=white" alt="Android 7.0+">
  <img src="https://img.shields.io/badge/Made%20in-Chile-D52B1E?style=flat" alt="Made in Chile">
</p>

---

## About

The **Anturi Quark** is a portable potentiostat for electrochemical measurements with screen-printed electrodes. This app is its control panel: it finds the Quark over Bluetooth, sends the measurement parameters, shows the results, exports them to Excel and keeps the Quark's firmware up to date.

## Download

| File | Contents |
|---|---|
| [**AnturiQuark app.zip**](AnturiQuark%20app.zip) | The app (`Anturi_Quark_App_1.2.0.apk`), version 1.2.0, with firmware 3.21.6 inside |
| [**Quark_Actualizacion_USB_3.21.6.zip**](Quark_Actualizacion_USB_3.21.6.zip) | One-time USB-C firmware update for Quarks that came with app 1.1.0 (Windows 10/11 and 64-bit Linux) |
| [**User guide (PDF, Spanish)**](Guia_de_uso_Anturi_Quark_261126.pdf) | How to use the app and the Quark, the Quark's light, firmware updates and troubleshooting |

## Updating from app 1.1.0

Do these steps once, in this order. They take about 15 minutes.

### 1. Install the new app on the phone

**Check the phone first.** The app needs an **Android** phone (it does not work on iPhone) with:

- **Android 7.0 or later.** To check it, open **Settings › About phone** (on Samsung: **Settings › About phone › Software information**) and look at **Android version**: it must be 7, 8, 9, 10 or higher.
- A **64-bit** processor and **Bluetooth Low Energy**. Practically every Android phone sold since 2017 has both. If Android says **App not installed** when you install it, the phone is probably 32-bit and cannot run the app.

1. **Uninstall the 1.1.0 app first.** On the phone, touch and hold the **Anturi Quark App** icon › **Uninstall**. Android treats 1.2.0 as a different app, so if you skip this you end up with two icons with the same name. Your Excel files in `Download/MiApp` are kept, but you will need to calibrate the Quark again and recreate your setups.

The quickest way to get the app onto the phone is to download it on a computer and send it to yourself on WhatsApp (other ways are listed below).

**On the computer**

2. Open this page and, in the **Download** table at the top, click **AnturiQuark app.zip**. The browser saves it in your **Downloads** folder. If GitHub opens a page for the file instead, click **Download raw file** (the arrow icon at the top right).
3. Open **Downloads**, right-click **AnturiQuark app.zip** › **Extract All…** › **Extract**. A folder called **AnturiQuark app** opens. Inside is the app, `Anturi_Quark_App_1.2.0.apk` (Windows may show it as *Anturi_Quark_App_1.2.0*, type *APK File*).
4. Open WhatsApp on the computer (the WhatsApp app or [web.whatsapp.com](https://web.whatsapp.com)) and open the chat with yourself: search for your own name or number, it shows as **(You)**.
5. Click **+** (or the paperclip) › **Document**, choose `Anturi_Quark_App_1.2.0.apk` in the **AnturiQuark app** folder and send it. Send it as **Document**, not as photo or video.

**On the phone**

6. Open WhatsApp, go to the chat with yourself and tap the file to download it (about 24 MB). When it finishes, tap it again to open it.
7. Android asks for permission to install apps from WhatsApp: tap **Settings**, turn on **Allow from this source**, go back and tap **Install**.
   - **Samsung phones:** instead you may see **Unknown apps blocked** (*Aplicaciones desconocidas bloqueadas*). That is Samsung's **Auto Blocker**. Tap **OK**, open **Settings › Security and privacy › Auto Blocker** and turn it off (it may ask for your PIN), then tap the file in WhatsApp again. Once the app is installed you can turn Auto Blocker back on; the app keeps working.
8. If Google Play Protect shows a warning, tap **More details** › **Install anyway**. The app is not distributed through Google Play yet.
9. Tap **Open** (or open **Anturi Quark App** from the app list) and accept the Bluetooth permissions. The app follows the phone's language (Spanish or English); you can change it in **Settings › Language**.

Other ways to get the APK onto the phone: open this page in the phone's browser, download **AnturiQuark app.zip** and extract it with the **Files** app; or copy `Anturi_Quark_App_1.2.0.apk` from the computer to the phone's **Download** folder with a USB cable. Then continue from step 7, allowing installs for the app you opened it with (Files, Chrome…).

### 2. Update the Quark's firmware over USB-C (Windows 11)

You need a Windows 10 or 11 computer, a USB-C cable that carries data, and the Quark with at least 30 % battery.

1. Download **Quark_Actualizacion_USB_3.21.6.zip** on the computer.
   - **If the download fails or the ZIP disappears from Downloads,** Windows Defender removed it by mistake (it may say *Virus detected* or name a threat like `Trojan:Script/Ulthar.A!ml`). It is a false alarm from Defender's automatic detection; the package is safe. To get it back:
     1. Open the **Start** menu, type **Windows Security** (*Seguridad de Windows*) and open it.
     2. Go to **Virus & threat protection** (*Protección contra virus y amenazas*) › **Protection history** (*Historial de protección*).
     3. Click the most recent entry that mentions **Quark_Actualizacion_USB_3.21.6.zip**. If Windows asks for permission, click **Yes**.
     4. Open **Actions** (*Acciones*) and choose **Allow on device** (*Permitir en el dispositivo*). If it only offers **Restore** (*Restaurar*), choose that.
     5. Download the ZIP again from this page (if **Restore** already put it back in **Downloads**, skip this). It should now stay in **Downloads**.
2. Right-click the ZIP › **Properties**. If **Unblock** appears at the bottom, tick it and press **OK**. Then right-click the ZIP › **Extract All…** › **Extract**.
3. Close the app on the phone. Turn on the Quark with its button (slow blue blink).
4. Connect the USB-C cable from the Quark straight to a USB port of the computer. Windows recognizes it by itself; no drivers are needed.
5. In the extracted folder, double-click **Actualizar_Quark**. If **Windows protected your PC** appears, click **More info** › **Run anyway**.
6. A black window goes through steps 1/4 to 4/4 by itself (check, backup, write, verify). It takes about 3 minutes. Do not disconnect the cable, turn off the Quark or close the window.
7. When **LISTO / DONE** appears in green, press any key. The Quark restarts by itself. Disconnect the cable.
8. In the app, tap **Find Quarks** (*Buscar Quarks*). The Quark now shows as **Anturi Quark**, with its 6-character ID below. Connect and calibrate it: **Settings › Autotuning › Calibrate current** (*Ajustes › Autotuning › Calibrar corriente*), with the electrode disconnected (about 40 s).

If an error appears, keep the Quark on and connected and run **Actualizar_Quark** again: it resumes where it stopped. If it persists, send the `registro_….txt` file from the folder to contacto@anturi.cl. On Linux, run `bash actualizar_quark.sh` (see `LEEME.txt` in the ZIP).

### 3. Next updates

From now on, new firmware comes inside the app: **Settings › Update** (*Ajustes › Actualizar*) installs it over Bluetooth. If the transfer is interrupted, the Quark keeps the version it had.

## Features

- **Techniques:** DC, cyclic voltammetry (CV), differential pulse voltammetry (DPV) and square wave voltammetry (SWV).
- **Current ranges:** ±145 µA, ±1.45 mA and ±14.5 mA, plus auto range for CV.
- **Results:** calibrated and raw current, plotted by sample or time, the I/V curve and, for SWV, ΔI vs E base. Pinch to zoom on any chart.
- **Excel export:** every test is saved as an `.xlsx` file with parameters and units, and can be shared from the app.
- **Setups:** save and reload the parameters of each technique. Preconcentration time in tenths of a second.
- **Calibration:** gain and offset correction for each range, using the Quark's internal precision resistor. Results can be shared.
- **Test mode:** measures the internal precision resistor instead of the electrode, to check the device.
- **Device status:** battery and temperature (tap to refresh), low-battery warning, remote power off and automatic power off. The app warns when the Quark turns off or goes out of range.
- **Temperature protection:** above 55 °C the Quark does not start measurements; above 60 °C it turns off.
- **Language and themes:** English or Spanish, and four color themes (Settings › Language, Settings › Theme).
- **Support:** Send report builds a text with app and firmware versions, Quark status, calibration and the last measurements. It does not include your location or the Quark's MAC address.

## Requirements

- An Android phone (not iPhone) with **Android 7.0 or later** (API 24), a 64-bit (arm64) processor and Bluetooth Low Energy. Practically every Android phone sold since 2017 qualifies.
- An Anturi Quark device.
- For the one-time USB-C update: a Windows 10/11 or 64-bit Linux computer and a USB-C data cable.

## Contact

Questions or a case for us? Reach us at **[anturi.cl](https://anturi.cl/)**, **contacto@anturi.cl** or on **[LinkedIn](https://www.linkedin.com/company/anturi/)**.
