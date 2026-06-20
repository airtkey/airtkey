# Device Setup & WiFi Config

> 💡 **Final Step:** Configure your ESP32 to connect to your home WiFi and send RTCM data to onocoy's NTRIP caster.

***

## 📋 Prerequisites

* [ ] ESP32 firmware flashed ✓
* [ ] UM980 configured ✓
* [ ] Wiring complete and verified ✓
* [ ] GNSS antenna has clear 360° sky view
* [ ] onocoy account registered (for NTRIP credentials)

> 💡 **Need onocoy credentials?** Sign up at [onocoy.com](https://onocoy.com/) and add your device to get NTRIP server details.

***

{% stepper %}
{% step %}
## 🔌 Step 1: Power On

1. Connect the **USB-C power cable** to your ESP32
2. Wait for the device to boot (\~20 seconds)

> ⚠️ **Important:** Use a **stable USB power source** (5V, ≥1A). A phone charger or powered USB hub works well.
{% endstep %}

{% step %}
## 📡 Step 2: Connect to ESP32 WiFi

1. Open your phone or laptop's WiFi settings
2. Find the network: **`ESP32-NTRIP-DUO`**

> 💡 **Tip:** The ESP32 creates its own WiFi network for initial setup.
{% endstep %}

{% step %}
## 🌐 Step 3: Open the Web Interface

1. Open a **web browser** (Chrome, Edge, Safari)
2. Enter the ESP32's IP address:

```
http://192.168.4.1
```

3. You should see the **ESP32 NTRIP DUO** web interface
{% endstep %}

{% step %}
## 📶 Step 4: Configure Home WiFi

1. Go to the **WiFi Settings** section
2. Enter your home WiFi credentials:

| Setting  | Value                  |
| -------- | ---------------------- |
| SSID     | Your WiFi network name |
| Password | Your WiFi password     |

3. Click **"Save"** or **"Apply"**

> 💡 **Tip:** The ESP32 will restart and connect to your home network automatically.
{% endstep %}

{% step %}
## 🔗 Step 5: Configure onocoy NTRIP

1. In the web interface, find **NTRIP Server Settings**
2. Enter your onocoy NTRIP caster details:

| Setting    | Value                                |
| ---------- | ------------------------------------ |
| Host       | servers`.onocoy.com`                 |
| Port       | `2101` (check your onocoy dashboard) |
| Mountpoint | Your credential                      |
| Username   | Your credential                      |
| Password   | Your credential password             |

> ⚠️ **Important:** Get these values from your onocoy dashboard at [app.onocoy.com](https://app.onocoy.com/)!
{% endstep %}

{% step %}
## ⚙️ Step 6: Configure UART (Default Usually Works)

The ESP32 and UM980 communicate via serial. Default settings:

| Setting   | Value    |
| --------- | -------- |
| UART      | UART0    |
| Baud Rate | `115200` |
| Data Bits | `8`      |
| Stop Bits | `1`      |
| Parity    | `None`   |

> 💡 **Tip:** These are the default values. Only change if you modified the UM980's settings.
{% endstep %}

{% step %}
## 🔄 Step 7: Save and Reboot

1. Click **"Save Configuration"**
2. Wait for the ESP32 to reboot (\~30 seconds)
3. The ESP32 will:
   * Connect to your home WiFi
   * Receive GPS data from UM980
   * Forward RTCM corrections to onocoy
{% endstep %}
{% endstepper %}

***

## ✅ Final Checklist

Before you leave your device running 24/7, verify everything:

### Hardware Checklist

* [ ] ESP32 firmware flashed successfully
* [ ] UM980 configured for RTCM3 output
* [ ] All wiring correct (use the [Wiring Diagram](/broken/pages/53f8e587865a9a602acc46818bdaa2e70e0c2677))
* [ ] GNSS antenna has **clear 360° sky view**
* [ ] Antenna mount is **stable and vibration-free**
* [ ] USB-C power is **permanently connected**
* [ ] Device is connected to **internet 24/7**

### Software Checklist

* [ ] ESP32 connected to home WiFi
* [ ] onocoy NTRIP credentials configured
* [ ] UART settings match UM980 configuration
* [ ] onocoy shows device as "Online" (check dashboard)

### Placement Checklist

* [ ] Antenna in optimal location (highest point, no obstructions)
* [ ] No metallic objects nearby (causes signal interference)
* [ ] Good GPS signal quality (check onocoy dashboard)
* [ ] Protected from weather (if outdoor installation)

***

## 📊 Expected Behavior

After successful configuration:

| Indicator           | Expected                          |
| ------------------- | --------------------------------- |
| ESP32 Web Interface | Shows "Connected to WiFi"         |
| onocoy Dashboard    | Device status = "Online"          |
| GPS Fix Quality     | "Fixed" (not "Float" or "No Fix") |
| Power LED           | Solid green                       |
| ESP32 LED           | Blinking (data transmission)      |

***

## 🔧 Common Issues & Solutions

| Issue                            | Solution                                      |
| -------------------------------- | --------------------------------------------- |
| ESP32 won't connect to WiFi      | Check SSID/password, move closer to router    |
| Device shows "Offline" in onocoy | Verify NTRIP credentials, check internet      |
| GPS fix stuck at "Float"         | Wait 15–30 min for full fix, check antenna    |
| ESP32 keeps rebooting            | Insufficient power (use stronger USB adapter) |
| Web interface not loading        | Reconnect to ESP32 WiFi, check IP address     |

***

## 📚 Additional Resources

| Resource                 | Link                                                                                   |
| ------------------------ | -------------------------------------------------------------------------------------- |
| onocoy Registration      | [onocoy.com](https://onocoy.com/)                                                      |
| Device Setup Guide (PDF) | [onominer GitHub](https://github.com/airtkey/onominer/raw/main/device%20setup.pdf)     |
| onocoy DIY Guide (PDF)   | [onominer GitHub](https://github.com/airtkey/onominer/raw/main/onominer_diy_guide.pdf) |
| ESP32 NTRIP DUO          | [GitHub - incarvr6](https://github.com/incarvr6/esp32-ntrip-DUO)                       |

***

## 🎉 Congratulations!

You've successfully built your **ESP32 + UM980 onocoy Base Station**!

> 💡 **Next Steps:**
>
> * Register your device on onocoy
> * Monitor performance in the onocoy dashboard
> * Consider upgrading to a Raspberry Pi + Mosaic-X5 for higher rewards
