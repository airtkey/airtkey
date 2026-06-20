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

# What Makes a Good Antenna?

## 🔍 What Makes a Good Antenna?

Not all antennas are created equal. For a professional GNSS base station, you need more than a simple GPS patch antenna.

***

### Key Features to Look For

| Feature                    | Why It Matters                            |
| -------------------------- | ----------------------------------------- |
| Multi-constellation        | Receives GPS, GLONASS, Galileo, BeiDou    |
| Multi-frequency (L1/L2/L5) | More data = higher accuracy               |
| Low noise amplifier (LNA)  | Boosts weak satellite signals             |
| Choke ring / ground plane  | Reduces multipath interference            |
| Calibration certificate    | Required for full onocoy reward potential |
| Weather resistance (IP67)  | Survives rain, heat, cold                 |

***

### What is Multipath — and Why Does It Matter?

Multipath happens when satellite signals bounce off buildings, roofs or other surfaces before reaching your antenna.

This causes small position errors — which directly affects your data quality and onocoy rewards.

A **choke ring** or **ground plane** around the antenna base significantly reduces multipath by blocking signals coming from low angles or below.

***

### Why Antenna Calibration Matters for onocoy

Calibration means that the exact phase center of your antenna has been professionally measured and documented.

#### What is the phase center?

The phase center is the exact point inside the antenna where the signal is received. This point is not always in the physical center of the antenna — and it can shift slightly depending on the satellite direction.

#### Why does this matter?

onocoy validators check your correction data against a network of reference stations. If your antenna's phase center is unknown or incorrect, your data will appear slightly off — even if your hardware is perfect.

**A calibrated antenna:**&#x20;

✅ Has a known and documented phase center&#x20;

✅ Is recognized by professional GNSS software&#x20;

✅ Produces more accurate correction data&#x20;

✅ Can lead to better reward scores on onocoy

> 💡 For serious miners, a calibrated antenna is not optional — it's the foundation of high-quality data.

***

### Recommended Antennas

#### 🥇 Beitian BT-800S — Best Value Calibrated Antenna

The Beitian BT-800S is my personal go-to antenna and the one I use on my own stations.

**Why I recommend it:**

✅ Fully calibrated — recognized by onocoy

✅ Integrated mini choke ring

✅ Multi-constellation & multi-frequency

✅ Excellent price-to-performance ratio

✅ Solid build quality for outdoor use

> The mini choke ring integration is a big plus at this price point — it reduces multipath without the bulk of a full choke ring antenna.

<figure><img src="https://30081112.s21i.faiusr.com/2/ABUIABACGAAg9v-fqwYogOqzywYwoAY4oAY.jpg" alt=""><figcaption></figcaption></figure>

***

#### 🥈 EM-500 — Solid Budget Option

The EM-500 from Emlid is a great entry-level antenna for miners who want decent performance without breaking the bank.

**Why it works:**

✅ Multi-constellation support

✅ Good signal quality for the price

✅ Easy to source globally

✅ Compatible with UM980 & Mosaic-X5

> A solid choice if you're just getting started and want to keep costs low.

<figure><img src="../../../../.gitbook/assets/Hbe4cef7461f64333be0dd1d7168c726aQ (1).jpg" alt=""><figcaption></figcaption></figure>

***

### Quick Comparison

| Antenna         | Calibrated | Choke Ring | Price Range | Best For           |
| --------------- | ---------- | ---------- | ----------- | ------------------ |
| Beitian BT-800S | ✅ Yes      | ✅ Mini     | \~\~        | Best value overall |
| EM-500          | ❌ No       | ❌ No       | \~          | Budget starter     |

***

> 💡 **Always check** if your antenna model is listed in the IGS antenna calibration database for maximum compatibility with onocoy. 🔗 [IGS Antenna Database](https://www.igs.org/mgex/equipment/)
