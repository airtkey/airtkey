# Wiring & Assembly

{% hint style="warning" %}
Perform all wiring with **power disconnected**. Never connect or disconnect components while powered.
{% endhint %}

## 🛡️ ESD Safety First

The UM980 GPS module is **sensitive to electrostatic discharge (ESD)**. Before you begin:

* [ ] Work on an **ESD-safe mat** with grounding wrist strap
* [ ] Use an **ESD-safe soldering station** with a fine tip
* [ ] Avoid touching the UM980 pins directly with your fingers

{% hint style="danger" %}
Static electricity can permanently damage the UM980. Take precautions!
{% endhint %}

## 🔗 Wiring Diagram

### UM980 → ESP32 Connection

| Signal        | UM980 Pin | ESP32 Pin  | Wire Color |
| ------------- | --------- | ---------- | ---------- |
| RX (Receive)  | RX        | TX (GPIO1) | 🟡 Yellow  |
| TX (Transmit) | TX        | RX (GPIO3) | 🔵 Blue    |
| Power (5V)    | VCC       | 5V         | 🔴 Red     |
| Ground        | GND       | GND        | ⚫ Black    |

### 4010 Fan → ESP32 Connection

| Signal     | Fan Wire | ESP32 Pin | Wire Color |
| ---------- | -------- | --------- | ---------- |
| Power (+)  | Red      | 3V3       | 🔴 Red     |
| Ground (-) | Black    | GND       | ⚫ Black    |

## 📝 Wiring Table (Quick Reference)

```
┌─────────────────────────────────────────────────────────┐
│  UM980 GPS Module          →         ESP32 WROOM        │
├─────────────────────────────────────────────────────────┤
│  UM980 RX   (Pin 4)       →    ESP32 TX (GPIO 1)  🟡    │
│  UM980 TX   (Pin 5)       →    ESP32 RX (GPIO 3)  🔵    │
│  UM980 VCC  (Pin 6)       →    ESP32 5V           🔴    │
│  UM980 GND  (Pin 1)       →    ESP32 GND          ⚫    │
├─────────────────────────────────────────────────────────┤
│  4010 Cooling Fan                                       │
├─────────────────────────────────────────────────────────┤
│  Fan + (Red wire)      →    ESP32 3V3            🔴     │
│  Fan - (Black wire)    →    ESP32 GND            ⚫     │
└─────────────────────────────────────────────────────────┘
```

## 🔧 Step-by-Step Wiring Instructions

{% stepper %}
{% step %}
## Prepare Your Wires

1. Cut **4 wires** at **6 cm length** each
2. Strip **both ends** of each wire (\~2–3mm)
3. Twist the strands and **tin with solder**

{% hint style="info" %}
Use a different color for each wire type to avoid confusion later.
{% endhint %}
{% endstep %}

{% step %}
## Solder Connections

1. **Tin the ESP32 pins** first with a small amount of solder
2. **Tin the UM980 pins** (be careful, these are delicate!)
3. Carefully solder each wire to the corresponding pin
4. Let joints cool for 10 seconds before moving
{% endstep %}

{% step %}
## Verify Connections

| Check       | Method                               |
| ----------- | ------------------------------------ |
| No bridges  | Visual inspection + magnifying glass |
| Cold joints | Gentle tug test on each wire         |
| Polarity    | Multimeter continuity check          |

{% hint style="warning" %}
Double-check polarity before powering! Reversed 5V/GND can damage components.
{% endhint %}
{% endstep %}
{% endstepper %}

## 🔨 Assembly Instructions

{% stepper %}
{% step %}
## Mount Components

1. Cut **double-sided 3M tape** strips to size
2. Clean all mounting surfaces with isopropyl alcohol
3. Attach tape to:
   * [ ] ESP32 (bottom side)
   * [ ] UM980 GPS module (bottom side)
   * [ ] 4010 Fan (center)
4. Mount components in enclosure with **clear separation** for airflow
{% endstep %}

{% step %}
## Fan Orientation

{% hint style="info" %}
The 4010 fan should blow **into** the enclosure for positive air pressure (keeps dust out).
{% endhint %}
{% endstep %}

{% step %}
## Route Cables

* Keep **power cables separate** from signal cables
* Avoid sharp bends in wires
* Secure with small zip ties if needed
{% endstep %}

{% step %}
## Close Enclosure

1. Connect the **external GNSS antenna** to the UM980
2. Connect the **USB-C power cable**
3. Close and secure the enclosure
{% endstep %}
{% endstepper %}

## 📸 Wiring Reference Image

<figure><img src="https://private-user-images.githubusercontent.com/49254419/412208902-f17d28dc-4bc7-4647-8311-7a1c44526d17.jpg?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODE5NDM1OTAsIm5iZiI6MTc4MTk0MzI5MCwicGF0aCI6Ii80OTI1NDQxOS80MTIyMDg5MDItZjE3ZDI4ZGMtNGJjNy00NjQ3LTgzMTEtN2ExYzQ0NTI2ZDE3LmpwZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA2MjAlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNjIwVDA4MTQ1MFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTdlMjk5NTgzYmJlM2E3Y2M4ZDQ0NmU2NTY3M2Y0ODY3YmIyZWQ0Mzk5NWE0OTYwMTc0OGNjNTk4ZDA0NjU4MjEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRmpwZWcifQ.op2C9RE2aymaQAUSW9BmYfC_NBhvtEyBJSykVQwad6Q" alt=""><figcaption><p>The illustration includes LED wiring, but that is not required.</p></figcaption></figure>

## 🔍 Visual Checklist

Before powering on, verify:

* [ ] All 4 UM980 wires connected correctly (colors match table)
* [ ] Fan wires connected to 3V3 and GND
* [ ] No solder bridges between pins
* [ ] Components secured with tape
* [ ] GNSS antenna connected to UM980
* [ ] USB-C cable ready for power

## 📁 Enclosure Files

Download the 3D printable enclosure files:

🔗 **GitHub:** [onominer/case\_3d\_print](https://github.com/airtkey/onominer/tree/main/case_3d_print)

{% hint style="info" %}
Print with 20% infill, no supports needed. Use PLA or PETG for best results.
{% endhint %}
