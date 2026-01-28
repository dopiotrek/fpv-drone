# Parts Selection Log

## Core Decisions

### 1. Power System: 4S vs 6S
**Recommendation: 4S**

| Feature | 4S (14.8V) | 6S (22.2V) |
| :--- | :--- | :--- |
| **Battery Price** | ~15€ - 20€ | ~25€ - 35€ |
| **Motor KV** | Higher (~2400KV) | Lower (~1750KV) |
| **Flight Feel** | Softer, more forgiving | Sharp, "locked in", consistent power |
| **Voltage Sag** | Noticeable at end of flight | Less noticeable |

**Decision:** We will target a **4S build** to strictly adhere to the 200€ budget limit. 6S batteries would add ~50€ to the total cost of ownership (getting 3-4 packs).

### 2. Frame: TBS Source One V5
- **Why?** It's the "AK-47" of drone frames. Open source design, which means parts (arms) are available everywhere cheaply.
- **Alternatives:** Apex Clone (heavier), Nazgul Frame (harder to get parts).

### 3. Stack: SpeedyBee F405 V3/V4
- **Why?** It has onboard Bluetooth. You can configure Betaflight from your phone in the field without a laptop.
- **Price:** ~65€ is unbeatable for a 50A ESC and F4FC.

### 4. Motors
- **Target Spec:** 2306 or 2207 Stator size.
- **Target KV:** 2400KV (for 4S).
- **Models:** Emax ECO II or Xing-E Pro.

### 5. Video System
- **Analog:** Cheapest way to fly.
- **VTX:** SpeedyBee TX800 (Cheap, reliable, easy mount on SpeedyBee stack).
- **Camera:** Foxeer Razer Mini (Best budget analog cam).

### 6. Control Link
- **ELRS (ExpressLRS):** There is no reason to use anything else today. Range is kilometers, price is <15€.
