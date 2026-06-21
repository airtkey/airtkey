# Bill of Materials

{% hint style="info" %}
**Estimated Total Cost: \~80–100€** — The most affordable entry point into onocoy staking.
{% endhint %}

## 🛒 Required Hardware

| Component            | Description                                      | Est. Price (€) | Buy Link                                                                          |
| -------------------- | ------------------------------------------------ | -------------- | --------------------------------------------------------------------------------- |
| ESP32 WROOM          | Dev Board with external WiFi antenna recommended | 8–12           | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=ESP32+WROOM+antenna) |
| UM980 GPS Module     | Unicorecomm RTK GNSS board                       | 100            | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=UM980+GNSS)          |
| GNSS Antenna         | 360° clear sky view required                     | 15–25          | [Beitian](https://www.beitian.com/en/sys-pd/1138.html)                            |
| 4010 Fan             | 40×40mm, 5V cooling fan                          | 3–5            | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=4010+fan+5V)         |
| USB-C Socket         | For power connection                             | 2–4            | AliExpress/Amazon                                                                 |
| USB-C Cable          | Quality cable for stable power                   | 5–8            | —                                                                                 |
| Enclosure (3D Print) | Optional but recommended                         | \~5 (filament) | [Download from GitHub](bill-of-materials.md#)                                     |

> 📦 **3D Print Files:** Find STL files for the enclosure on the [onominer GitHub repository](https://github.com/airtkey/onominer/tree/main/case_3d_print).

## 🔧 Required Materials

| Material             | Quantity      | Notes                                    |
| -------------------- | ------------- | ---------------------------------------- |
| Wires (4 colors)     | 4× \~6cm each | Black, Red, Yellow, Blue recommended     |
| Double-sided 3M Tape | 1 strip       | For mounting components inside enclosure |
| M3 Screws            | 2×            | Optional — for lid attachment            |
| M3 Thread Cutter     | 1×            | Optional — if lid will be screwed shut   |

## 🔨 Required Tools

| Tool                       | Notes                                               |
| -------------------------- | --------------------------------------------------- |
| ESD-safe Soldering Station | **Fine tip required** — the UM980 is ESD-sensitive! |
| Side Cutters               | For trimming wire ends                              |
| Wire Stripper              | Standard AWG 24–28 range                            |
| Multimeter                 | For verifying connections (recommended)             |
| 3D Printer                 | Optional — only if using printed enclosure          |

{% hint style="warning" %}
**Warning:** The UM980 GPS module is **ESD-sensitive**. Always use an ESD-safe workspace and soldering station to avoid permanent damage!
{% endhint %}

## 💰 Cost Summary

```
Hardware Total:       ~100–124€
Tools (one-time):     ~30–50€ (if not already owned)
=================================
Estimated Start:      ~100–174€
```

{% hint style="info" %}
**Tip:** You may already own most tools! The only mandatory new purchase is the ESP32 + UM980 combo (\~100–120€).
{% endhint %}

> 🔗 **Pro Tip:** Buy everything from AliExpress if you're patient — saves \~30% vs. Amazon. Use a multi-item order to reduce shipping costs.
