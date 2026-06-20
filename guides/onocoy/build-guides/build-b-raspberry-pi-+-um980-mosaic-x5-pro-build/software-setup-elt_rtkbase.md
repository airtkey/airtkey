# Software Setup (ELT\_RTKBase)

> 💡 **This guide installs ELT\_RTKBase** — the open-source base station software that powers your GNSS station. It supports both UM980 and Mosaic-X5 receivers out-of-the-box and integrates seamlessly with onocoy.

***

## 📋 Prerequisites

* Raspberry Pi with microSD card (32GB+ recommended)
* GNSS module connected (UM980 or Mosaic-X5)
* Internet connection (Ethernet or WiFi)
* Computer for SSH access

***

{% stepper %}
{% step %}
## Download Required Files

1. **Download Raspberry Pi Imager**:
   * [raspberrypi.com/software](https://www.raspberrypi.com/software/)
{% endstep %}

{% step %}
## Flash the SD Card

1. **Launch Raspberry Pi Imager**
2. **Select Device**: Click "Raspberry Pi 4 ( or your version)"
3.  Click **"Choose OS"** →

    * `Raspberry Pi OS (other)`
    * → `Raspberry Pi OS Lite (64-bit)`
    * ✅ Confirm it shows **Bookworm** in the description

    1. Click **"Choose Storage"** → Select your microSD card

    > ❌ Do NOT use the Desktop version&#x20;
    >
    > ❌ Do NOT use Bullseye or older \
    > ✅ Only **Lite 64-bit Bookworm**
4. **Select Storage**: Choose your microSD card
5. **Click NEXT** → Click "EDIT SETTINGS"
{% endstep %}

{% step %}
## Configure Settings

In the settings editor, fill in:

| Setting                        | Recommended Value                  |
| ------------------------------ | ---------------------------------- |
| **Hostname**                   | `rtkbase` (or your custom name)    |
| **WiFi SSID**                  | Your WiFi network name             |
| **WiFi Password**              | Your WiFi password                 |
| **WiFi Hidden**                | No (unless your network is hidden) |
| **Enable SSH**                 | ✅ Yes                              |
| **Set password for 'pi' user** | Your secure password               |

{% hint style="info" %}
If you set hostname to `rtkbase`, you can access the web interface at `http://rtkbase.local`
{% endhint %}
{% endstep %}

{% step %}
## Write & Boot

1. Click **SAVE** → **YES** to confirm
2. Wait for the write process to complete
3. Click **CONTINUE**
4. **Eject the SD card** and insert into your Raspberry Pi
5. **Connect power** and wait 2-3 minutes for first boot
{% endstep %}
{% endstepper %}

***

## Install ELT\_RTKBase

> ⚠️ And f**or users** who already have Raspberry Pi OS running.

{% stepper %}
{% step %}
## Connect GNSS Receiver

{% hint style="warning" %}
**Important:** Connect the GNSS receiver and the antenna BEFORE running the installation script!
{% endhint %}

Ensure your UM980 or Mosaic-X5 is connected via USB.
{% endstep %}

{% step %}
## Download & Run Installer

```bash
# Download the installer
wget https://github.com/GNSSOEM/ELT_RTKBase/raw/main/install.sh

# Make it executable
chmod +x install.sh

# Run the installation
./install.sh
```

{% hint style="info" %}
The first run may trigger a reboot — this is normal!
{% endhint %}
{% endstep %}

{% step %}
## Complete Installation

After the reboot, run the installer again:

```bash
./install.sh
```

Wait for the installation to complete, then proceed to configuration.

> ℹ️ **Note:** The installation may finish with an error message — this can be ignored in most cases. Simply proceed and check if the dashboard is accessible in your browser.
{% endstep %}
{% endstepper %}

***

## Access the Web Interface

{% stepper %}
{% step %}
## Open the Browser

1. Open your browser
2. Go to `http://rtkbase.local` (or use the Pi's IP address)
3. Please enter the RTKBase password:
   * **Password:** `admin`

{% hint style="warning" %}
**Important:** Change the default password immediately after first login!
{% endhint %}
{% endstep %}

{% step %}
## Configure for onocoy

### Navigate to Settings → NTRIP Server

| Setting                       | Value                                                   |
| ----------------------------- | ------------------------------------------------------- |
| **NTRIP Server**              | Enabled                                                 |
| **Protocol**                  | NTRIP v2 HTTP                                           |
| **Caster Host**               | servers.onocoy.com                                      |
| **Caster Port**               | `2101`                                                  |
| **Mountpoint & Caster Login** | Your onocoy credential                                  |
| **Password**                  | Your credential password (not your dashboard passwort!) |

{% hint style="info" %}
Get your onocoy credentials from your [onocoy Dashboard](https://www.onocoy.com/).
{% endhint %}

###
{% endstep %}

{% step %}
## Verify Connection

1. Go to **Status** page
2. Check the following indicators:

| Indicator            | Expected State |
| -------------------- | -------------- |
| **Satellites**       | >20 visible    |
| **Solution**         | Fixed or Float |
| **NTRIP Connection** | Connected      |
{% endstep %}
{% endstepper %}

***

## 🛠️ Useful SSH Commands

Connect via SSH:

```bash
ssh pi@rtkbase.local
# or
ssh pi@<your-pi-ip-address>
```

Useful commands:

```bash
# Check service status
sudo systemctl status rtkbase

# View logs
sudo journalctl -u rtkbase -f

# Restart service
sudo systemctl restart rtkbase

# Update software
sudo /home/pi/rtkbase/scripts/update.sh
```

***

## 📊 ELT\_RTKBase Features

| Feature               | Description                         |
| --------------------- | ----------------------------------- |
| **NTRIP Server**      | Stream RTCM3 corrections to onocoy  |
| **NTRIP Caster**      | Serve rovers locally (e.g., drones) |
| **TCP Server/Client** | Alternative data streaming          |
| **Data Logging**      | Record RTCM3 and RINEX data         |
| **Web Interface**     | Easy configuration                  |
| **Tailscale VPN**     | Built-in remote access              |
| **Auto-restart**      | Recovery from disconnections        |

***

## 🔧 Advanced Configuration

### Change Communication Speed

For lower latency, increase the baud rate:

1. Go to **Settings**
2. Change **Speed** from `115200` to `921600`
3. Click **Save**

> ⚠️ **Note:** Some receivers may work unstably at 921600. If issues occur, revert to 115200.

***

## 📂 Next Steps

* [VPN & Remote Access](/broken/pages/421e9d3c45b8e6eec528169905278abdb5030ec4) → Set up Tailscale for remote management
