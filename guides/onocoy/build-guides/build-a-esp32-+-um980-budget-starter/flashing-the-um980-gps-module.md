# Flashing the UM980 GPS Module

{% hint style="info" %}
**What is this?** The UM980 needs to be configured to output RTCM3 correction data for RTK positioning. This step sets it up correctly for use with onocoy.
{% endhint %}

## 📋 Prerequisites

* UM980 GPS module
* USB-C cable
* Windows PC (required for this step)
* Administrator rights

## 📥 Step-by-step

{% stepper %}
{% step %}
## Step 1: Download Required Files

Download the configuration files from the onominer GitHub repository:

🔗 **GitHub:** [onominer/software](https://github.com/airtkey/onominer/tree/main/software)

1. Download the entire `software` folder
2. Extract to your **Desktop** (important for path length!)
3. You should now have a `GPS MODULE` folder on your Desktop

```
Desktop/
└── GPS MODULE/
    ├── nmeaConf.exe
    ├── UM980_RTCM3_OUT.txt
    └── Driver/
        └── CH340 driver files
```
{% endstep %}

{% step %}
## Step 2: Install the  Driver

{% hint style="warning" %}
**Required only if UM980 isn't detected as a COM port.**
{% endhint %}

1. Open the `Driver` folder inside `GPS MODULE`
2. Unzip the `um980_driver`&#x20;
3. Install it
4. Grant administrator privileges if prompted
{% endstep %}

{% step %}
## Step 3: Connect the UM980

1. Connect the **UM980 to your PC** via USB-C cable
2. Connect the **GNSS antenna** to the UM980
3. Wait for Windows to recognize the device

{% hint style="info" %}
**Tip:** The UM980 should power on automatically when connected via USB.
{% endhint %}
{% endstep %}

{% step %}
## Step 4: Identify the COM Port

1. Open **Device Manager** (Press `Win + X` → Device Manager)
2. Expand **"Ports (COM & LPT)"**
3. Look for **"USB-Enhanced-SERIAL CH341"** (or similar)
4. Note the COM port number (e.g., `COM5`)

```
Device Manager
└── Ports (COM & LPT)
    └── USB-Enhanced-SERIAL CH340 (COM5)  ← Note this number!
```

{% hint style="warning" %}
**Note:** Your COM port number may be different (COM3, COM4, etc.)
{% endhint %}
{% endstep %}

{% step %}
## Step 5: Configure the UM980

1. Open **Terminal** (PowerShell or Command Prompt)
2. Navigate to the GPS MODULE folder:

```bash
cd Desktop\GPS MODULE
```

3. Run the configuration command:

```bash
.\nmeaConf.exe COM5 UM980_RTCM3_OUT.txt
```

{% hint style="warning" %}
**Important:** Replace `COM5` with your actual COM port number!
{% endhint %}
{% endstep %}

{% step %}
## Step 6: Verify Configuration

After running the command, you should see:

```
Opening serial port COM5...
Loading configuration from UM980_RTCM3_OUT.txt...
Configuration sent successfully!
```

{% hint style="info" %}
**Success!** The UM980 is now configured for RTCM3 output.
{% endhint %}
{% endstep %}
{% endstepper %}

## 🔧 Troubleshooting

| Problem               | Solution                                   |
| --------------------- | ------------------------------------------ |
| "Access denied" error | Run Terminal as Administrator              |
| COM port not found    | Check USB connection, install CH341 driver |
| Configuration fails   | Check COM port number is correct           |
| No output shown       | Try a different COM port, check USB cable  |
| Device not responding | Unplug/replug USB, try different port      |

## 📋 Configuration Checklist

* [ ] `GPS MODULE` folder extracted to Desktop
* [ ] UM980 connected via USB-C
* [ ] COM port identified in Device Manager
* [ ] Terminal opened in correct folder
* [ ] Configuration command executed successfully
* [ ] GNSS antenna connected to UM980

## 📚 Additional Resources

| Resource              | Link                                                             |
| --------------------- | ---------------------------------------------------------------- |
| UM980 Commands Manual | [Unicorecomm Documentation](https://en.unicorecomm.com/)         |
| onominer Repository   | [GitHub - airtkey/onominer](https://github.com/airtkey/onominer) |
| RTCM3 Protocol Info   | [RTCM Standard](https://www.rtcm.org/)                           |

{% hint style="info" %}
The UM980 only needs to be configured once! Settings are saved to non-volatile memory.
{% endhint %}
