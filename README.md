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
  <img src="https://img.shields.io/badge/Firmware-3.21.2-0B2033?style=flat" alt="Firmware 3.21.2">
  <img src="https://img.shields.io/badge/Android-7.0%2B-3DDC84?style=flat&logo=android&logoColor=white" alt="Android 7.0+">
  <img src="https://img.shields.io/badge/Made%20in-Chile-D52B1E?style=flat" alt="Made in Chile">
</p>

---

## About

The **Anturi Quark** is a portable potentiostat for electrochemical measurements with screen-printed electrodes. This app is its control panel: it finds the Quark over Bluetooth, sends the measurement parameters, shows the results, exports them to Excel and keeps the Quark's firmware up to date.

## Download

| File | Contents |
|---|---|
| [**AnturiQuark app.zip**](AnturiQuark%20app.zip) | The app (`Anturi_Quark_App_1.2.0.apk`), version 1.2.0, with firmware 3.21.2 inside |
| [**Quark_Actualizacion_USB_3.21.2.zip**](Quark_Actualizacion_USB_3.21.2.zip) | One-time USB-C firmware update for Quarks that came with app 1.1.0 (Windows 10/11 and 64-bit Linux) |
| [**User guide (PDF, Spanish)**](Guia_de_uso_Anturi_Quark_201126.pdf) | How to use the app and the Quark, the Quark's light, firmware updates and troubleshooting |

## What's new in 1.2.0

- **Stop** button to end a measurement and keep the data recorded so far.
- Shorter parameter names (E start, E step, t pulse…), a separate **Experiment name** field and a single confirmation before running.
- Each Quark is identified by a **6-character ID**. The app no longer shows the Quark's MAC address.
- Excel files with units, every DC sample and its time in seconds. Each technique keeps its own last result. SWV adds the **ΔI vs E base** curve.
- **Send report** for support, **Share** for calibration results, and **firmware updates from the app** over Bluetooth.
- The Quark turns itself off after 10 minutes without measurements, never during a measurement or an update.

## Updating from app 1.1.0

Do these steps once, in this order. They take about 15 minutes.

### 1. Install the new app on the phone

1. **Uninstall the 1.1.0 app first.** Android treats 1.2.0 as a different app. Your Excel files in `Download/MiApp` are kept, but you will need to calibrate the Quark again and recreate your setups.
2. Download **AnturiQuark app.zip** on your phone (or on a computer and copy it to the phone) and extract it.
3. Open `Anturi_Quark_App_1.2.0.apk`. If Android asks, allow **Install unknown apps** for the app you opened it with (Files, Chrome, WhatsApp…).
4. If Google Play Protect shows a warning, tap **Install anyway**. The app is not distributed through Google Play yet.
5. Open **Anturi Quark App** and accept the Bluetooth permissions.

### 2. Update the Quark's firmware over USB-C (Windows 11)

You need a Windows 10 or 11 computer, a USB-C cable that carries data, and the Quark with at least 30 % battery.

1. Download **Quark_Actualizacion_USB_3.21.2.zip** on the computer.
2. Right-click the ZIP › **Properties**. If **Unblock** appears at the bottom, tick it and press **OK**. Then right-click the ZIP › **Extract All…** › **Extract**.
3. Close the app on the phone. Turn on the Quark with its button (slow blue blink).
4. Connect the USB-C cable from the Quark straight to a USB port of the computer. Windows recognizes it by itself; no drivers are needed.
5. In the extracted folder, double-click **Actualizar_Quark**. If **Windows protected your PC** appears, click **More info** › **Run anyway**.
6. A black window goes through steps 1/4 to 4/4 by itself (check, backup, write, verify). It takes about 3 minutes. Do not disconnect the cable, turn off the Quark or close the window.
7. When **LISTO / DONE** appears in green, press any key. The Quark restarts by itself. Disconnect the cable.
8. In the app, tap **Find Quarks**. The Quark now shows as **Anturi Quark-XXXXXX**. Connect and calibrate it: **Settings › Calibrate current**, with the electrode disconnected (about 40 s).

If an error appears, keep the Quark on and connected and run **Actualizar_Quark** again: it resumes where it stopped. If it persists, send the `registro_….txt` file from the folder to contacto@anturi.cl. On Linux, run `bash actualizar_quark.sh` (see `LEEME.txt` in the ZIP).

### 3. Next updates

From now on, new firmware comes inside the app: **Settings › Firmware update** installs it over Bluetooth. If the transfer is interrupted, the Quark keeps the version it had.

## Features

- **Techniques:** DC, cyclic voltammetry (CV), differential pulse voltammetry (DPV) and square wave voltammetry (SWV).
- **Current ranges:** ±145 µA, ±1.45 mA and ±14.5 mA, plus auto range for CV.
- **Results:** calibrated and raw current, plotted by sample or time, the I/V curve and, for SWV, ΔI vs E base.
- **Excel export:** every test is saved as an `.xlsx` file with parameters and units, and can be shared from the app.
- **Setups:** save and reload the parameters of each technique.
- **Calibration:** gain and offset correction for each range, using the Quark's internal precision resistor. Results can be shared.
- **Test mode:** measures the internal precision resistor instead of the electrode, to check the device.
- **Device status:** battery and temperature, low-battery warning, remote power off and automatic power off.
- **Support:** Send report builds a text with app and firmware versions, Quark status, calibration and the last measurements. It does not include your location or the Quark's MAC address.

## Requirements

- Android 7.0 or later, with Bluetooth Low Energy, on a 64-bit phone (practically every phone from 2017 onwards).
- An Anturi Quark device.
- For the one-time USB-C update: a Windows 10/11 or 64-bit Linux computer and a USB-C data cable.

## Contact

Questions or a case for us? Reach us at **[anturi.cl](https://anturi.cl/)**, **contacto@anturi.cl** or on **[LinkedIn](https://www.linkedin.com/company/anturi/)**.
