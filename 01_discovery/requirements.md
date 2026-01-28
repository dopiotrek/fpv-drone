# Project Requirements & Discovery

## 1. Mission Profile
**Primary Use Case:**
- [ ] **Freestyle (Bashing):** High durability, acrobatics, 3-5min flight time.
- [ ] **Cinematic (Cruising):** Stability, smoothness, 5-8min flight time.
- [ ] **Long Range:** Efficiency, GPS reliability, 15+min flight time.

**Environment:**
- [ ] **Open Category A1 (Safe):** Flying small drones (<250g) near people/buildings.
- [ ] **Open Category A3 (Remote):** Flying larger drones (5-inch) >150m from people/buildings.

## 2. Regulatory & Compliance
*The drone class dictates where you can fly.*
- **Class:** [DECISION NEEDED]
    - [ ] **Nano (<250g):** "Tiny Whoop" or 2-3 inch. **Legal Advantage:** Can fly in A1. **Budget Advantage:** Cheaper.
    - [ ] **Mini (5-inch):** Standard Freestyle. **Legal Restriction:** Must fly in A3 (Far from people). **Performance:** Better wind resistance, carries GoPro easily.

**Current Regulatory Assumption:** EASA Open Category A3 (5-inch Build).

## 3. System Architecture
**Propulsion:**
- **Voltage:** 4S (14.8V) vs 6S (22.2V).
- **Target Thrust-to-Weight:** ~6:1 (Freestyle Standard).

**Avionics:**
- **Control Link:** ELRS 2.4GHz.
- **Video Link:** Analog 5.8GHz.

**Mechanical:**
- **Frame:** Carbon Fiber (Source One V5 or similar).
- **Payload Capacity:** 100g (GoPro) - *Only applies if 5-inch is selected.*

## 4. Verification Strategy
*How will we prove requirements are met?*
- [ ] **Mass Budget Check:** Total weight < Weight Limit (if 250g).
- [ ] **Propulsion Tables:** Verify hover throttle < 30%.
- [ ] **Smoke Test:** Electrical continuity check.
- [ ] **Maiden Flight:** Stable hover + Failsafe test.
