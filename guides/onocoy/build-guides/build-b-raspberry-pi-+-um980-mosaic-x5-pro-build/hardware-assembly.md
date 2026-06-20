# Hardware Assembly

{% hint style="info" %}
💡 **Time required:** \~20-45 minutes\
**Difficulty:** Beginner\
**Important:** Make all connections BEFORE plugging in power!
{% endhint %}

***

## ⚠️ Safety Warnings

{% hint style="danger" %}
⚠️ **CRITICAL:** Always disconnect power before connecting the antenna or any cables!
{% endhint %}

{% hint style="danger" %}
⚠️ **Power Supply Warning:** Do NOT use "fast" USB chargers (Quick Charge, Power Delivery) — they can supply up to 20V and will destroy your equipment. Use only a simple 5V/2-3A USB-C adapter.\
The original is preferable.
{% endhint %}

***

{% stepper %}
{% step %}
## Prepare the Raspberry Pi 4

1.  **Flashing the OS**\
    &#x20;🚨 **Do this before any hardware assembly!** <br>

    👉 **Go to:** Software Setup Page and complete the flashing before continuing here.


2. **Insert the microSD card** with Raspberry Pi OS into the SD card slot on the underside of the Pi.
3. **Connect to Ethernet** (recommended for stability) or prepare for WiFi setup later.
4. **Connect your cooling solution**
{% endstep %}

{% step %}
## Connect the GNSS Module

### For **UM980**:

| Connection    | From         | To                    |
| ------------- | ------------ | --------------------- |
| USB-C Cable   | UM980        | Raspberry Pi USB port |
| Antenna Cable | GNSS Antenna | UM980                 |

```
┌─────────────────┐         USB → USB-C              ┌─────────────┐
│     UM980       ├────────────────────────►────-────┤  Raspberry  │
│                 │                                  │    Pi 4B    │
└─────────────────┘                                  └─────────────┘
        │
        │  Cable
        ▼
┌─────────────────┐
│   GNSS Antenna  │
│   (Roof/Mast)   │
└─────────────────┘
```

### For **Mosaic-X5** :

| Connection    | From          | To                    |
| ------------- | ------------- | --------------------- |
| USB-C Cable   | Mosaic-X5     | Raspberry Pi USB port |
| Antenna Cable | GNSS Antenna  | Mosaic-X5             |

```
┌─────────────────┐         USB-C Cable              ┌─────────────┐
│   Mosaic-X5     ├──────────────────────────►───────┤  Raspberry  │
│                 │                                  │    Pi 4B    │
└─────────────────┘                                  └─────────────┘
        │
        │  Cable
        ▼
┌─────────────────┐
│   GNSS Antenna  │
│   (Roof/Mast)   │
└─────────────────┘
```
{% endstep %}

{% step %}
## Connect to ETH/USB Hub HAT (Optional)

{% hint style="info" %}
💡 **Required for UM980** when using a Raspberry Pi Zero 2W. For Pi 4B, you can connect the UM980 directly via OTG cable.
{% endhint %}

For **Raspberry Pi Zero 2W** setups:

1. Mount the **Waveshare ETH/USB Hub HAT** on the GPIO pins
2. Connect **UM980** to the USB Hub via USB-A to USB-C OTG
3. Connect **Ethernet** to the Hub (if available)
4. Power the HAT via GPIO or microUSB
{% endstep %}

{% step %}
## Antenna Placement

{% hint style="warning" %}
⚠️ **Antenna placement is critical for performance!**
{% endhint %}

### Best Practices:

| Requirement         | Why It Matters                                      |
| ------------------- | --------------------------------------------------- |
| **360° sky view**   | Maximize satellite visibility                       |
| **No obstructions** | Avoid buildings, trees, walls blocking signals      |
| **High position**   | Roof or mast mounting is ideal                      |
| **Ground plane**    | Use a metal plate or grounded structure if possible |
| **Secure mounting** | Wind-resistant pole or tripod mount                 |

### Outdoor Antenna Setup:

1. Mount antenna on a **pole or tripod** with clear sky view
2. Run **TNC-K coax cable** to your base station
3. **Seal connectors** with heat shrink tubing or self-vulcanizing tape
4. Ensure antenna cable is **not stressed** at connectors
{% endstep %}

{% step %}
## Power Connection

{% hint style="warning" %}
⚠️ **Use ONLY a 5V/2-3A USB-C power supply!**
{% endhint %}

1. **Connect power last** — after all other cables are in place
2. Use the **official Raspberry Pi power supply** or a quality 5V/3A adapter
3. The Pi will boot and show activity lights
{% endstep %}

{% step %}
## Verify Connections

| LED                         | Meaning                             |
| --------------------------- | ----------------------------------- |
| **Power (Red)**             | Solid = Power connected             |
| **Activity (Green)**        | Flashing = SD card access / Booting |
| **Ethernet (Yellow/Green)** | Solid = Network connected           |
{% endstep %}
{% endstepper %}

***

***

## ✅ Assembly Checklist

* [ ] Insert microSD card
* [ ] Connect GNSS module (UM980/Mosaic-X5)
* [ ] Connect GNSS antenna
* [ ] Connect Ethernet (recommended)
* [ ] Connect cooling (optional)
* [ ] Verify all cables secure
* [ ] Connect power LAST
* [ ] Wait for boot (2-3 minutes)

***

## 📂 Next Steps

* [Software Setup](/broken/pages/eaa141464f35780ce36299d80963e65514e5cb91) → Install ELT\_RTKBase
* [VPN Setup](/broken/pages/41221ba5f36f94b0651a223101d944f99a78a757) → Configure Tailscale for remote access
