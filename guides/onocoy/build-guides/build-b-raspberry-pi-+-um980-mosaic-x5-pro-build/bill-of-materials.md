# Bill of Materials

{% hint style="info" %}
**Build B** is the professional-grade solution with more connectivity options, better WiFi range, and support for both UM980 and Mosaic-X5 GNSS modules. Total cost: \~€200-600 depending on GNSS module choice.
{% endhint %}

## 🔧 Core Components

| Component                  | Recommendation                        | Est. Price | Source                                                                          |
| -------------------------- | ------------------------------------- | ---------- | ------------------------------------------------------------------------------- |
| **Raspberry Pi 4B** (1GB+) | Official starter kit                  | \~€70      | [raspberrypi.com](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/) |
| **GNSS Module**            | UM980 or Mosaic-X5                    | €230-590   |                                                                                 |
| **GNSS Antenna**           | Beitian BS-800S (Multi-band L1/L2/L5) | \~€80      | [AliExpress](https://aliexpress.us/item/3256808846936564.html)                  |
| **microSD Card**           | 32GB+, Class 10                       | \~€8       | Any reputable brand                                                             |
| **USB-C Power Supply**     | 5V/3A (official Pi adapter)           | \~€10      | [raspberrypi.com](https://www.raspberrypi.com/products/micro-usb-power-supply/) |
| **Ethernet Cable**         | Cat5e/Cat6                            | \~€5       | Any electronics store                                                           |

{% hint style="info" %}
For onocoy mining, we recommend the **Septentrio Mosaic-X5** as the best long-term investment. While the Unicore UM980 offers a good balance of quality and price, the Mosaic-X5 provides superior interference resistance and future-proofing — especially important as more stations appear in your area, since **better hardware receives better rewards**.
{% endhint %}

{% hint style="warning" %}
The u-blox ZED-X20P does **not** support GLONASS and is therefore **not suitable for Onocoy**.
{% endhint %}

## 🔌 Optional Accessories

| Component                                | Notes                             | Est. Price   |
| ---------------------------------------- | --------------------------------- | ------------ |
| **Aluminum Heat Sink or cooling system** | Passive cooling                   | €5-15        |
| **Enclosure/Case**                       | 3D-printable files available      | DIY or \~€10 |
| **Mounting Bracket**                     | Pole mount for outdoor antenna    | \~€10        |
| **LM400 Cable**                          | SMA to TNC-K (⚠️ TNC-K required!) | \~€25        |

## 🛠️ Required Tools

| Tool                    | Purpose                             |
| ----------------------- | ----------------------------------- |
| **Raspberry Pi Imager** | Flashing OS to SD card              |
| **Computer**            | For initial setup and configuration |
| **SD Card Reader**      | To flash the microSD card           |

## 💰 Total Cost Estimate

| Configuration       | Est. Total |
| ------------------- | ---------- |
| **UM980 Build**     | \~€280-350 |
| **Mosaic-X5 Build** | \~€520-763 |

## 📦 Where to Buy

* **Raspberry Pi**: [raspberrypi.com](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/) / Amazon / Ebay
* **UM980/Mosaic-X5**: [gnss.store](https://gnss.store/collections/cors-fanless-stations)/ [gns-electronics.](https://www.gns-electronics.de/) / [witmotion](https://witmotion-sensor.com/products/rtk-gps-gnss-modules-centimeter-level-um982-um980-um960?_pos=1&_sid=63959976d&_ss=r\&variant=42873258311877)
* **Beitian Antenna & Cable**: [Beitian Shop](https://store.beitian.com/collections/gnss-antenna/products/beitian-high-gain-high-precision-gnss-antenna-provide-stability-and-reliability-gnss-signal-for-positioning-applications-bt-800s?variant=44374047490335)

\
📂 Related Documentation

* [Hardware Assembly](/broken/pages/7d87fc7e48862a4131d9657eeb23163573518975) ← Next: Assemble your hardware
* [Hardware Comparison](/broken/pages/62562b7c9975b58ddf56093073b3a1252a4b8e01) ← UM980 vs Mosaic-X5 detailed comparison
* [RTKit BOM Source](https://github.com/airtkey/RTKit/blob/main/bom.md)
