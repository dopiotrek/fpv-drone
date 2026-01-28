This is an exciting journey. Building a drone from scratch is one of the most rewarding engineering challenges because it combines mechanical skills, electronics, and software configuration.

Given your **200 EUR budget**, **limited tools**, and **no 3D printer**, we need to be strategic. A "5-inch Analog Freestyle Drone" is the gold standard for DIY beginners because parts are standardized, cheap, and durable.

Here is your project structure, designed to be hosted on GitHub.

---

### **Part 1: The GitHub Repository Structure**

Since you want to document your journey, treat this repository as a "Lab Notebook." This structure will help you organize your research and build process.

**Repository Name Idea:** `diy-fpv-drone-build`

**Folder Layout:**

```text
/
├── /docs
│   ├── /learning          # Notes on aerodynamics, PID loops, battery safety
│   ├── /diagrams          # Wiring diagrams (drawn by you or saved from research)
│   └── /datasheets        # PDFs/Links to manuals for your Flight Controller, VTX, etc.
├── /build_logs
│   ├── 01_parts_selection.md  # Why you chose these specific parts
│   ├── 02_frame_assembly.md   # Photos and notes on assembling the frame
│   └── 03_wiring.md           # Documentation of your soldering work
├── /configuration
│   ├── betaflight_dump.txt    # Backup of your settings (crucial for recovery)
│   └── vtx_table.json         # Video Transmitter configuration file
├── BOM.md                     # Bill of Materials (Your shopping list & prices)
└── README.md                  # Main entry point: Project goals, final photo, current status

```

---

### **Part 2: The "200 EUR" Component List (Bill of Materials)**

To stay within ~200 EUR for the **drone itself**, we must choose "high-value" budget components.
*Note: This budget covers the drone. You will still need a Radio Transmitter (Controller), Goggles, and Batteries/Charger. If 200 EUR is your **total** total budget for everything, we would need to look at "Tiny Whoop" Ready-to-Fly kits instead.*

**Target Build:** 5-Inch Analog Freestyle Quadcopter (4S or 6S)

| Component | Recommendation (Search for these) | Est. Price | Why? |
| --- | --- | --- | --- |
| **Frame** | **TBS Source One V5** (5-inch) | ~35 € | Open source, cheap, durable, NO 3D printer needed (carbon fiber). |
| **Stack (FC+ESC)** | **SpeedyBee F405 V3 or V4 Stack** | ~65 € | Best value on the market. Bluetooth configuration via phone app (easy for beginners). |
| **Motors (4x)** | **Emax ECO II** 2306 or **iFlight Xing-E Pro** | ~55 € | Reliable budget workhorses. (2400KV for 4S battery, 1750KV for 6S). |
| **Camera** | **Foxeer Razer Mini** or **Caddx Ant** | ~20 € | Good analog image quality for the price. |
| **Video Transmitter** | **SpeedyBee TX800** or **Eachine TX805** | ~20 € | Cheap, adjustable power, reliable. |
| **Receiver** | **BetaFPV ELRS Nano RX** | ~15 € | ELRS is the modern standard. Incredible range, cheap price. |
| **Props** | **Gemfan Hurricane 51466** (Pack of 4) | ~5 € | Durable and smooth flight feel. |
| **Misc** | Battery strap, XT60 pigtail (usually comes with Stack) | ~5 € | Essential small parts. |
| **Total** |  | **~215 €** | *Prices fluctuate; look for sales on AliExpress or local hobby shops.* |

> **Critical Research Task:** Before buying, verify your "Motor KV" matches your "Battery Voltage".
> * **4S Battery (cheaper):** Look for ~2400KV - 2550KV motors.
> * **6S Battery (more power):** Look for ~1700KV - 1950KV motors.
> 
> 

---

### **Part 3: The "Hidden" Costs (Tools & Ground Station)**

Since you have limited tools, you will need to acquire these. Do not attempt to build without them.

1. **Soldering Iron:** Essential. You need one that can get hot enough (400°C) to solder thick battery wires. (e.g., TS100 or a generic adjustable 60W iron).
2. **Hex Drivers:** Sizes 1.5mm, 2.0mm, and 2.5mm. (The L-keys from IKEA furniture are frustrating; get proper drivers).
3. **Multimeter:** **Mandatory** for safety. You must check for short circuits before plugging in a battery, or you will fry your 65€ stack instantly.
4. **Radio & Goggles:** If you don't have these, they are extra.
* *Budget Radio:* **Radiomaster Pocket** (ELRS version) ~65 €
* *Budget Goggles:* **Eachine EV800D** ~90 €



---

### **Part 4: The Project Phases**

Use these phases as "Milestones" in your GitHub repository.

#### **Phase 1: Research & Procurement**

* **Goal:** Understand how the parts connect.
* **Action:** Draw a wiring diagram. How does the Receiver connect to the Flight Controller (FC)? Where does the Video Transmitter (VTX) get power?
* **Documentation:** Upload your wiring diagram to `/docs/diagrams`.

#### **Phase 2: Frame Assembly**

* **Goal:** Assemble the carbon fiber frame.
* **Action:** Follow the Source One manual. Use "Loctite" (blue thread locker) on screws connecting into metal motors to prevent vibrations from loosening them.
* **Documentation:** Take photos of the bare frame.

#### **Phase 3: The Stack & Soldering**

* **Goal:** Mount the Flight Controller and ESCs and solder the motors.
* **Action:** This is the hardest part.
1. Mount the ESC (bottom board).
2. Cut motor wires to length and solder to ESC pads.
3. Solder the XT60 power lead (capacitor is mandatory!).
4. Solder the Receiver and Camera to the FC (top board).


* **Tag:**

#### **Phase 4: Smoke Test & Configuration**

* **Goal:** Power up without smoke.
* **Action:** Use your **Multimeter** in "Continuity Mode" on the battery connector. If it beeps, you have a short circuit. DO NOT PLUG IN.
* **Tool:** Download **Betaflight Configurator**. This software is used to program the drone.

#### **Phase 5: Maiden Flight**

* **Goal:** A stable hover.
* **Action:** Go to an open grass field. Do not fly indoors.

---

### **Next Step**

To get you started on **Phase 1 (Research)**, would you like me to generate a specific **wiring diagram description** for the SpeedyBee F405 stack connecting to an ELRS receiver? This will be the first technical document for your GitHub repo.