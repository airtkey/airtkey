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

# Which Setup is Right for Me? (Decision Guide)

### Which Setup is Right for Me?

There are different ways to get started with onocoy mining. This page helps you find the right path for your situation.

***

### 🛒 Option 1 – Buy a Ready-Made Device

The fastest way to get started is to buy a pre-configured onocoy-compatible miner. These devices are plug & play — no soldering, no flashing, just connect and mine.

_onocoy is hardware-agnostic, meaning it works with any compatible device — not just their partner products._

👉 See the full list of recommended devices: [https://docs.onocoy.com/documentation/3.-become-a-miner/1.-get-a-station](https://docs.onocoy.com/documentation/3.-become-a-miner/1.-get-a-station)

#### Popular ready-made options:

| Device                                                                             | Chip       | Connectivity    |
| ---------------------------------------------------------------------------------- | ---------- | --------------- |
| [GNS Electronics NTRIP-X](https://www.gns-electronics.de/)                         | UM980      | WiFi            |
| [SparkFun RTK mosaic-X5](https://www.sparkfun.com/sparkfun-rtk-mosaic-x5.html)     | Mosaic-X5  | WiFi / Ethernet |
| [ArduSimple RTK Base Station](https://www.ardusimple.de/product/rtk-base-station/) | Mosaic-X5  | Ethernet        |
| [Locosys GB-10WB ](https://www.locosystech.com/de/product/GB-10WB.html)/ GB-104B   | TBD        | WiFi / LTE      |
| [GNSS Store Miners](https://gnss.store/)                                           | UM980 / X5 | WiFi / PoE      |
| [onoLink Miner](https://onolink.io/product/onolink-miner/)                         | UM980      | WiFi            |

> 💡 Ready-made devices are great if you want to get started quickly without any technical knowledge.

***

### 🔧 Option 2 – Build It Yourself (DIY)

_onocoy is fully hardware-agnostic — meaning you can build your own station using off-the-shelf components._

### Why go DIY?

🛠️ You enjoy building and tinkering with electronics&#x20;

📦 Import restrictions in your country make it hard to buy ready-made GNSS devices&#x20;

💸 You want to reduce import costs and duties&#x20;

🧰 You already own parts like an ESP32 or Raspberry Pi

&#x20;🔁 You want to reuse the hardware for other projects later&#x20;

🌍 You live in a region where ready-made miners are hard to source or expensive to ship

> onocoy works with any receiver that meets the technical requirements — no official device needed!

#### DIY Requirements (from onocoy):

* Triple- or quad-band GNSS receiver (supports GPS, Galileo, BeiDou, GLONASS)
* High quality GNSS antenna
* NTRIP Server functionality
* WiFi / Ethernet connection (either built-in or via ESP32 / Raspberry Pi)

> ⚠️ Single or dual-band receivers will earn rewards, but at a much lower level than triple/quad-band receivers.

***

### 🗺️ DIY Build Paths

#### 🟢 Build A – ESP32 + UM980 (Budget Starter)

✅ Best for: Beginners, low budget, simple setup&#x20;

✅ Cost: \~80-120€&#x20;

✅ No Linux knowledge needed&#x20;

✅ Easy WiFi setup via web browser&#x20;

❌ Limited remote management&#x20;

❌ Not easily upgradeable

👉 Go to [Build Guide A](../build-guides/build-a-esp32-+-um980-budget-starter/)

***

#### 🔵 Build B – Raspberry Pi + Mosaic-X5 (Pro Build)

✅ Best for: Advanced users, maximum performance

&#x20;✅ Cost: \~300-500€

&#x20;✅ Full remote access via Tailscale VPN

&#x20;✅ Best-in-class GNSS receiver&#x20;

✅ Full Linux flexibility&#x20;

❌ Higher cost&#x20;

❌ Requires some Linux knowledge

👉 Go to [Build Guide B](../build-guides/build-b-raspberry-pi-+-um980-mosaic-x5-pro-build/)

***

### 💡 The Smart Starter Path – Raspberry Pi + UM980

You don't have to go all-in from the start.\
A great strategy is to begin with a Raspberry Pi + UM980 and upgrade the GNSS module later.

**Why this works:**&#x20;

The Raspberry Pi and the GNSS receiver are separate components. \
You can swap the UM980 for a Mosaic-X5 at any time — without replacing the rest of your setup.

#### **Step-by-step upgrade path:**

1. 🟡 Start: Raspberry Pi + UM980 → Lower cost, remote access, learn the system
2. 🔵 Upgrade: Swap UM980 → Mosaic-X5 → Better performance, higher onocoy quality score → More ONO rewards 💰

> 💰 onocoy rewards better hardware with higher quality scores. Starting small and upgrading later is a smart, cost-effective approach!

***

### 📊 Full Comparison

| Path        | Controller   | Receiver  | Cost       | Upgradeable | Difficulty |
| ----------- | ------------ | --------- | ---------- | ----------- | ---------- |
| Ready-Made  | Built-in     | Built-in  | \~150-500€ | ❌           | ⭐ Easy     |
| Budget DIY  | ESP32        | UM980     | \~80-120€  | ❌           | ⭐⭐ ⭐Med    |
| Smart Start | Raspberry Pi | UM980     | \~150-200€ | ✅           | ⭐⭐ Easy    |
| Pro Build   | Raspberry Pi | Mosaic-X5 | \~300-500€ | ✅           | ⭐⭐ Easy    |

***

> 💡 Not sure yet?\
> &#x20;→ Quickest start: Buy a ready-made device \
> → Lowest cost DIY: ESP32 + UM980 \
> → Best long-term value: Raspberry Pi + UM980 (upgradeable to Mosaic-X5)
