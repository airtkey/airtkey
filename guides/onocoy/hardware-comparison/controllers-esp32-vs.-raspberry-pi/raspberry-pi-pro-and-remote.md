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

# Raspberry Pi – Pro & Remote

## 🔵 Raspberry Pi – Pro & Remote

The Raspberry Pi is a small single-board computer running a full Linux operating system. It gives you complete control over your mining station — from anywhere in the world.

***

### What is the Raspberry Pi?

The Raspberry Pi is a credit-card sized computer that runs Linux. In the context of onocoy mining, it acts as a powerful and flexible controller that connects your GNSS receiver to the onocoy network.

Unlike the ESP32, the Raspberry Pi runs a full OS — giving you SSH access, logging, monitoring, and the ability to run multiple services at once.

***

### Why Choose Raspberry Pi?

✅ Full remote access via SSH from anywhere&#x20;

✅ Works with both UM980 and Mosaic-X5&#x20;

✅ Complete logging and diagnostics&#x20;

✅ Easy remote software updates&#x20;

✅ Run multiple tools simultaneously&#x20;

✅ Very stable for 24/7 long-term operation&#x20;

✅ Highly customizable

***

### What You Need

| Component           | Description                                         | Approx. Cost |
| ------------------- | --------------------------------------------------- | ------------ |
| Raspberry Pi 4 or 5 | All versions from the Raspberry Pi 2W onwards work. | \~35-80€     |
| MicroSD Card        | Min. 16GB, Class 10                                 | \~8-15€      |
| GNSS Receiver       | UM980 or Mosaic-X5                                  | \~50-350€    |
| GNSS Antenna        | Multi-frequency, L1/L2/L5                           | \~80€        |
| USB Power Supply    | 5V, min. 3A (official Pi PSU)                       | \~10-15€     |
| USB-C cable         | For power                                           | \~5€         |
| USB -C cable        | To connect GNSS receiver                            | \~5€         |

> 💡 Total cost for a full Raspberry Pi + UM980 setup: approximately **130-250€**
>
> 💡 Total cost for a full Raspberry Pi + Mosaic-X5 setup: approximately 6**30-750€**

***

### How It Works

\[GNSS Antenna]\
↓\
\[UM980 or Mosaic-X5] ←→ USB / UART\
↓\
\[Raspberry Pi]\
(Linux OS)\
↓\
\[Ethernet / WiFi]\
↓\
\[onocoy Network]

The Raspberry Pi receives raw GNSS correction data from the receiver and forwards it to the onocoy servers. Because it runs Linux, you can monitor, configure and update everything remotely via SSH.

***

### Remote Access – Manage from Anywhere

One of the biggest advantages of the Raspberry Pi is full remote management:

### Remote Access – Manage from Anywhere

One of the biggest advantages of the Raspberry Pi is full remote management via **Tailscale**.

Tailscale is a free VPN tool that connects all your devices in a private network — no port forwarding, no static IP, no router configuration needed.

***

#### Why Tailscale?

✅ **Free** — no cost for personal use ✅ **Works everywhere** — home, mobile, travel ✅ **No port forwarding required** ✅ **No static IP needed** ✅ **Works on all platforms** — Windows, Mac, Linux, iOS, Android ✅ **Secure** — end-to-end encrypted

***

#### How It Works

Once Tailscale is installed on your Raspberry Pi and your phone or laptop, all devices are connected in a private network — as if they were on the same local network.

> 💡 No matter where you are — at work, on vacation or on your phone — your mining station is always just one command away.

***

> 🔗 Learn more at [tailscale.com](https://tailscale.com/)



💡 Once set up, you never need physical access again.\
Perfect for rooftop or remote installations.

### Recommended Models

Tabelle kopieren

| Model                | RAM   | Recommended for                                              |
| -------------------- | ----- | ------------------------------------------------------------ |
| Raspberry Pi 3B+     | < 1GB | <p>UM980 setup ✅<br>Mosaic-X5 setup ✅</p>                    |
| Raspberry Pi 4B      | < 1GB | <p>UM980 setup ✅<br>Mosaic-X5 setup ✅</p>                    |
| Raspberry Pi 4B      | < 1GB | <p>UM980 setup ✅<br>Mosaic-X5 setup ✅</p>                    |
| Raspberry Pi 5       | < 1GB | <p>Future proof  ✅<br>UM980 setup ✅<br>Mosaic-X5 setup ✅</p> |
| Raspberry Pi Zero 2W | 512MB | Budget option, UM980 only                                    |

***

### Limitations to Keep in Mind

❌ **Higher cost** than ESP32 \
❌ **Requires basic Linux knowledge** \
❌ **Higher power consumption** (\~3-5W) \
❌ **Slightly more complex initial setup**

***

### Ready to Build?

👉 [Build B: Raspberry Pi + UM980 / Mosaic X5 (Pro Build)](../../build-guides/build-b-raspberry-pi-+-um980-mosaic-x5-pro-build/)

***

### Video Tutorial 🎥

Watch the full Raspberry Pi build on YouTube: 👉 [Build Your Own Raspberry Pi Miner](https://www.youtube.com/@airtkey)
