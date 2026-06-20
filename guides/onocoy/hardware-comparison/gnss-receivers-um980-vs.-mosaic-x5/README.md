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

# GNSS Receivers: UM980 vs. Mosaic-X5

## 📡 GNSS Receivers: UM980 vs. Mosaic-X5

The GNSS receiver is the heart of your mining station. It determines how accurately your station tracks satellites — and directly impacts your onocoy quality score and rewards.

***

### Full Spec Comparison

| Feature                | UM980                  | Mosaic-X5                  |
| ---------------------- | ---------------------- | -------------------------- |
| Manufacturer           | Unicore Communications | Septentrio                 |
| Price                  | \~ 100€                | \~ 450 - 600€              |
| Constellations         | GPS, GLONASS,          | GPS, GLONASS,              |
|                        | Galileo, BeiDou        | Galileo, BeiDou            |
| Tracking Channels      | 1408                   | 448                        |
| Multi-frequency        | L1, L2, L5             | L1, L2, L5, L6             |
| Anti-Jamming           | Basic                  | Advanced (AIM+)            |
| Anti-Spoofing          | ❌                      | ✅                          |
| onocoy Quality Score   | Good                   | Excellent                  |
| Compatible Controllers | ESP32, Raspberry Pi    | Raspberry Pi (recommended) |

***

### 🟡 UM980 – The Budget Champion

The UM980 by Unicore Communications is a powerful multi-frequency GNSS receiver at a fraction of the cost of professional modules.

**Strengths:** \
✅ Very affordable (\~100€)&#x20;

✅ Multi-frequency: L1, L2, L5

&#x20;✅ Works with ESP32 and Raspberry Pi&#x20;

✅ Great entry point for onocoy mining&#x20;

✅ Large community & good documentation

**Weaknesses:** ❌ Lower quality score vs. Mosaic-X5 ❌ No anti-spoofing protection ❌ Basic anti-jamming only

> 💡 Perfect for beginners and budget builds. Still delivers solid onocoy rewards!

***

### 🔵 Mosaic-X5 – The Professional Choice

The Mosaic-X5 by Septentrio is a professional-grade GNSS receiver used in surveying, autonomous vehicles and scientific applications.

**Strengths:** \
✅ Industry-leading accuracy&#x20;

✅ Advanced anti-jamming (AIM+ technology)&#x20;

✅ Full anti-spoofing protection&#x20;

✅ Supports L1, L2, L5, L6 (PPP corrections)&#x20;

✅ Highest onocoy quality score&#x20;

✅ Extremely reliable 24/7 operation

**Weaknesses:** ❌ Higher price (\~250-350€) ❌ Requires Raspberry Pi (not compatible with ESP32) ❌ Overkill for casual miners

> 💡 Best choice if you want maximum rewards and plan to run a serious long-term mining station.

***

### 📊 Real World Performance

Want to see the actual difference in numbers?

👉 [Performance Metrics & Real Data](performance-metrics-and-real-data.md#performance-metrics-and-real-data)

***

### 🏁 Still not sure which one to pick?

👉 [When to Choose Which?](../../getting-started/which-setup-is-right-for-me-decision-guide.md)

