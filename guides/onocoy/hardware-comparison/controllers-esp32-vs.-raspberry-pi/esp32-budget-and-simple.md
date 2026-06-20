---
layout:
  width: default
  title:
    visible: false
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# ESP32 – Budget & Simple

## ⚡ ESP32 – Budget & Simple

The ESP32 is a small microcontroller that was originally designed for IoT projects — and it turns out to be a perfect low-cost controller for onocoy mining.

***

### What is the ESP32?

The ESP32 is a tiny microcontroller chip with built-in WiFi and Bluetooth. In the onocoy mining world, it acts as a bridge between your GNSS receiver (UM980) and the onocoy network.

It runs pre-flashed firmware — no operating system, no complex setup. Just flash and go.

***

### Why Choose ESP32?

✅ Costs only 5-15€&#x20;

✅ Ultra low power consumption (\~0.5W)&#x20;

✅ No Linux knowledge required&#x20;

✅ Pre-built firmware available&#x20;

✅ Compact — fits in any enclosure&#x20;

✅ Reliable 24/7 operation&#x20;

✅ Great starting point for beginners

***

### What You Need

| Component        | Description                    | Approx. Cost |
| ---------------- | ------------------------------ | ------------ |
| ESP32 board      | ESP32 WROOM-32                 | \~5-15€      |
| UM980 module     | GNSS receiver                  | \~100€       |
| GNSS Antenna     | Multi-frequency, L1/L2/L5      | \~80€        |
| USB power supply | 5V, min. 1A                    | \~5-10€      |
| USB cable        | For power and initial flashing | \~2-5€       |

> 💡 Total cost for a full ESP32 + UM980 setup: approximately 18&#x30;**-200€**

***

### How It Works

\[GNSS Antenna] \
↓ \
\[UM980] ←→ UART/Serial \
↓ \
\[ESP32] \
↓ \
\[WiFi] \
↓ \
\[onocoy Network]

***

The ESP32 receives raw GNSS correction data from the UM980 via serial (UART) and forwards it directly to the onocoy servers via WiFi.

***

### Limitations to Keep in Mind

❌ **Only works with UM980** — not compatible with Mosaic-X5 ❌ **No remote SSH access** — need physical access for changes ❌ **Firmware updates require USB** connection to a PC ❌ **Limited diagnostics** — no detailed logs or remote dashboards

***

### Ready to Build?

👉 [Build A: ESP32 + UM980 – Full Build Guide](../../build-guides/build-a-esp32-+-um980-budget-starter/)

This guide covers:

* Full bill of materials
* Wiring & assembly
* Flashing the ESP32 firmware
* Flashing the UM980 module
* Connecting to onocoy

***

### Video Tutorial 🎥

Watch the full build on YouTube: 👉 [DIY ESP32 Version – Step by Step](https://www.youtube.com/@airtkey)
