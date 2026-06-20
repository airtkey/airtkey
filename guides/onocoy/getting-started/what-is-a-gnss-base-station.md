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

# What is a GNSS Base Station?

### What is a GNSS Base Station?

GNSS stands for Global Navigation Satellite System — it's the technology behind GPS, Galileo, GLONASS and BeiDou.

#### How it works:

A GNSS base station is a receiver placed at a fixed, known location. It continuously receives signals from satellites and calculates correction data based on its exact position.

This correction data (called RTK corrections) is then sent over the internet to mobile receivers — improving their accuracy from meters to centimeters.

#### What your station does:

📡 Receives satellite signals 24/7

🧮 Calculates correction data&#x20;

📤 Streams data to onocoy via NTRIP protocol&#x20;

💰 Earns ONO rewards for contributing

#### What you need:

* A GNSS receiver (UM980 or Mosaic-X5)
* A controller (ESP32 or Raspberry Pi)
* A good antenna with clear sky view
* A stable internet connection

> 💡 Your station works automatically once set up — no daily maintenance needed!
