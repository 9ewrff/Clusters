# 10-Node Compute Blade CM5 Cluster

## 1. Overview & System Role
- **Purpose:** High-density 10-node Raspberry Pi Compute Module 5 (CM5) rackmount cluster.
- **Node Count:** 10 Compute Blade Nodes.

---

## 2. Hardware Bill of Materials (BOM)

### Compute Modules & Blades
- **10x** Raspberry Pi CM5 16GB (CM5016000)
- **10x** Compute Blade DEV boards
- **10x** Compute Blade Standard Fan Units
- **10x** GLOTRENDS Aluminum CM5 Heatsinks

### Storage
- **10x** Patriot P300 256GB NVMe SSDs (10-pack)

### Rackmount, Cabling & Networking
- **1x** DeskPi RackMate TT
- **1x** Compute Blade 10" 3D Print Rackmount chassis
- **1x** GigaPlus 2.5 Gbps 10-port PoE+ Switch
- **1x** GigaPlus 10" Rack Mount 3D Printed ears (Printables)
- **10x** Monoprice Cat6A SlimRun 6" Patch Cables (10-pack)
- **1x** ioplex SFP+ Twinax DAC Patch Cable

---

## 3. Power & Networking Requirements
- **Power Source:** Power over Ethernet (PoE+) supplied to all 10 Compute Blades via the GigaPlus switch.
- **Switch Uplink:** High-speed interconnect using SFP+ Twinax DAC cable.

---

## 4. Assembly & Physical Deployment
- **Rack Configuration:** Mounted in DeskPi RackMate TT using custom 10" 3D-printed rackmount brackets.
- **Cooling:** Combined GLOTRENDS aluminum heatsinks and Compute Blade standard fan units on every CM5 module.