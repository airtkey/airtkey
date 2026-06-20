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

# Pros & Cons Overview

## ⚖️ Pros & Cons Overview

A direct comparison of both controllers to help you make the right decision.

***

### ⚡ ESP32

#### ✅ Pros

* **Very affordable** — costs only 5-15€
* **Plug & play** — pre-flashed firmware available
* **Ultra low power** — runs on \~0.5W
* **Compact size** — fits anywhere
* **No technical Linux knowledge required**
* **Perfect for beginners**
* **Large community support**
* **Works great with UM980**

#### ❌ Cons

* **No remote management** — limited SSH/VNC access
* **Only compatible with UM980** (not Mosaic-X5)
* **Less flexible** — harder to customize
* **No display or UI** — status via LED only
* **Limited logging and diagnostics**
* **Firmware updates require USB connection**

***

### 🔵 Raspberry Pi

#### ✅ Pros

* **Full Linux OS** — complete flexibility
* **Remote access via SSH and VNC** — manage from anywhere
* **Compatible with UM980 , Mosaic-X5 and more**
* **Full logging and diagnostics**
* **Easy software updates remotely**
* **Expandable** — add display, storage, sensors
* **Runs multiple services simultaneously**
* **Professional grade reliability**

#### ❌ Cons

* **Higher cost** — 35-80€ for the Pi alone
* **Higher power consumption** — \~3-5W
* **Requires basic Linux knowledge**
* **Slightly more complex initial setup**
* **Larger form factor**

***

### Side by Side Summary

| Feature              | ESP32              | Raspberry Pi         |
| -------------------- | ------------------ | -------------------- |
| Price                | \~5-15€ 💚         | \~35-80€             |
| Power consumption    | \~0.5W 💚          | \~3-5W               |
| Setup difficulty     | Easy 💚            | Moderate             |
| Remote management    | Limited            | Full SSH/VNC 💚      |
| Compatible receivers | UM980 only         | UM980 + Mosaic-X5 💚 |
| Flexibility          | Low                | High 💚              |
| Best for             | Beginners / Budget | Pro / Serious miners |

***

### Bottom Line

> **Start with ESP32** if you want the easiest and cheapest way to get your first station online.
>
> **Choose Raspberry Pi** if you want full control, remote management and plan to use the Mosaic-X5.

***

👉 [ESP32 – Budget & Simple](esp32-budget-and-simple.md) 👉 [Raspberry Pi – Pro & Remote](raspberry-pi-pro-and-remote.md)

