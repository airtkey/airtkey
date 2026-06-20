# Flashing the ESP32 Firmware

{% hint style="warning" %}
**Critical:** Flash the ESP32 **before** connecting it to the UM980 module!
{% endhint %}

## 📋 Prerequisites

* ESP32 WROOM board
* USB-C cable
* Desktop/Laptop with Chrome or Edge browser
* Stable internet connection (for firmware download)

{% stepper %}
{% step %}
## Download the Firmware

Download the latest firmware binary from the official repository:

🔗 **GitHub:** [ESP32 NTRIP duo new.bin](https://github.com/incarvr6/esp32-ntrip-DUO/blob/master/ESP32%20NTRIP%20duo%20new.bin)

1. Click on `ESP32 NTRIP duo new.bin`
2. Click the **"Download"** button (or right-click → Save Link As)
3. Save the file to an easy-to-find location (e.g., Desktop)

{% hint style="info" %}
The firmware supports both **Onocoy AND RTK Direct simultaneously** — dual NTRIP output!
{% endhint %}
{% endstep %}

{% step %}
## Install USB Driver (If Needed)

If your ESP32 isn't recognized, install the **CH340 USB driver**:

1. Download the driver: [CH340 Driver (Windows)](https://www.wch.cn/downloads/CH341SER_ZIP.html)
2. Extract the ZIP file
3. Right-click on `silabser.inf`
4. Select **"Install"**

{% hint style="info" %}
On some systems, Windows automatically installs the driver. Check Device Manager first.
{% endhint %}
{% endstep %}

{% step %}
## Open ESPHome Web Flasher

1. Open **Chrome** or **Edge** (Firefox may have issues)
2. Go to: [**https://web.esphome.io/**](https://web.esphome.io/)
3. Click **"Connect"**
{% endstep %}

{% step %}
## Enter Boot Mode

{% hint style="warning" %}
**Important:** Hold the BOOT button before connecting!
{% endhint %}

1. Connect your ESP32 to the PC via **USB-C cable**
2. **Hold the BOOT button** (small button on the board)
3. While holding BOOT, plug the USB cable into the PC
4. Release the BOOT button after 2 seconds

```
┌─────────────────────────────┐
│  Hold BOOT → Plug USB       │
│  Release after ~2 seconds   │
└─────────────────────────────┘
```
{% endstep %}

{% step %}
## Select COM Port

1. In ESPHome Web Flasher, click **"Connect"**
2. Select your ESP32's COM port from the dropdown
3. Click **"Connect"**

{% hint style="warning" %}
**Troubleshooting - No COM Port?**

* Try a different USB cable (some cheap cables only charge!)
* Install the CH340 driver (see above)
* Try a different USB port (use USB 2.0, not USB 3.0)
* On Linux: Run `ls /dev/ttyUSB*` to find the port
{% endhint %}
{% endstep %}

{% step %}
## Flash the Firmware

1. Click **"Install"** in ESPHome Web Flasher
2. Select the `ESP32 NTRIP duo new.bin` file you downloaded
3. Wait for the flashing process to complete (\~30–60 seconds)

```
✅ Progress indicator shows during flash
✅ "Successfully installed." message when done
```
{% endstep %}

{% step %}
## Complete the Flash

1. **Disconnect** the USB cable from the ESP32
2. Wait 5 seconds
3. **Reconnect** the USB cable

{% hint style="info" %}
This ensures the ESP32 boots into normal mode, not flash mode.
{% endhint %}
{% endstep %}

{% step %}
## Verify Success

After \~20 seconds, check for a new WiFi network:

| Expected WiFi Name | Default Password                     |
| ------------------ | ------------------------------------ |
| `ESP32-NTRIP-DUO`  | <ul><li>It is not secured.</li></ul> |

You can see this network in your phone's WiFi settings.

{% hint style="success" %}
Your ESP32 is now running the NTRIP Duo firmware.
{% endhint %}
{% endstep %}
{% endstepper %}

## ✅ Quick Verification Checklist

* [ ] Firmware file downloaded successfully
* [ ] ESP32 entered boot mode correctly
* [ ] COM port detected and connected
* [ ] Flash completed without errors
* [ ] WiFi network "ESP32-NTRIP-DUO" visible



## 🔧 Troubleshooting

| Problem                  | Solution                                          |
| ------------------------ | ------------------------------------------------- |
| No COM port detected     | Install CH340 driver, try different USB cable     |
| Flash fails              | Hold BOOT button properly, try different USB port |
| WiFi network not visible | Wait 30 seconds, check USB power is sufficient    |
| ESP32 not responding     | Press EN/RST button to reboot                     |

## 📚 Additional Resources

| Resource            | Link                                                                  |
| ------------------- | --------------------------------------------------------------------- |
| ESPHome Web Flasher | [web.esphome.io](https://web.esphome.io/)                             |
| Firmware Repository | [ESP32 NTRIP DUO GitHub](https://github.com/incarvr6/esp32-ntrip-DUO) |
| Installation Video  | [YouTube Tutorial](https://youtu.be/33Mu5EV7fOE)                      |
