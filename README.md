# Master Cluster Budget & Infrastructure Summary

## 1. Executive Summary & Cost Breakdown

This document covers shared infrastructure, management hardware, fabrication equipment, and the master cost rollup across all four cluster environments:
1. **Raspberry Pi 5 Swarm Cluster** (7 Nodes)
2. **Orange Pi 5 Max Cluster** (6 Nodes)
3. **Jetson Orin Nano Node** (1 AI Acceleration Node)
4. **10-Node Compute Blade CM5 Cluster** (10 CM5 Nodes)

---

## 2. Workstation & Management Console

### Framework Laptop 16 Custom Build
- **Processor & Graphics:** AMD Ryzen AI 9 HX 370, Radeon RX 7700S GPU Module
- **Memory:** 32GB (2 x 16GB) DDR5-5600 RAM
- **Storage:** 2TB SanDisk 850X (M.2 2280) + 2TB SanDisk SN770M (M.2 2230) — *4TB Total NVMe*
- **Customizations:** Black Bezel, Haptic Touchpad, US English Keyboard, 2x LED Matrix, RGB Macropad, Black & Orange Spacers
- **Expansion Cards:** USB-C (Silver & Orange), USB-A (Black), Ethernet, MicroSD, SD, Audio
- **Cost:** **$4,165.00**

---

## 3. Custom Fabrication & Assembly Tools

### Equipment & Materials
- **Bambu Lab P2S Combo 3D Printer & AMS 2 Pro:** Custom enclosure & chassis fabrication — **$949.00 – $1,199.00**
- **PETG Filament 1.75mm 1kg Spools (3x):** High-heat filament for rack drawers & cages — **~$60.00**
- **M2.5 & M3 Brass Standoff + Screw Kit (300+ PCS):** PCB & board mounting — **~$15.00**
- **Heat-Set Insert Installation Kit M2.5 / M3:** Threaded metal sockets for 3D prints — **~$20.00**
- **Nicpro 58PCS Art Drawing Supplies Kit:** Finishing and node labeling — **$25.00**
- **Subtotal:** **$1,069.00 – $1,319.00**

---

## 4. Shared Power & Core Networking Infrastructure

### Power Hubs & Infrastructure
- **1U PDU Horizontal Rackmount Power Strip (1x):** Central power hub for rack components — **$60.99**
- **Orange Pi Dedicated USB-C Power / Buck Converters:** 5V/5A USB-C PSUs — **~$90.00 – $120.00**
- **Jetson Dedicated 19V 4.74A DC Adapter:** — **~$20.00**
- **100W USB-C to USB-C Patch Cables (15x):** 1.5ft cables for clean USB-C power runs — **~$30.00**
- **Power Safety Note:** The Bambu 3D Printer must be powered via a separate, dedicated wall outlet/circuit to prevent tripping the PDU breaker during bed heat-up.

### Networking Core
- **24-Port 2.5G Managed Switch w/ 220W+ PoE+ (1x):** Central switch with manual PoE allocation — **~$340.00 – $380.00**
- **GEARit Cat6 Patch Cables 1ft (24-Pack):** Cluster network patch runs — **$18.00**
- **Subtotal:** **$558.99 – $628.99**

---

## 5. Master Budget Rollup Summary

| Category / Component Group | Cost Range (USD) |
| :--- | :--- |
| **Raspberry Pi 5 Swarm Cluster** | $1,285.94 – $1,365.94 |
| **Orange Pi 5 Max Cluster** | $981.00 – $1,055.00 |
| **Jetson Orin Nano AI Node** | $579.00 – $619.00 |
| **10-Node CM5 Cluster (Est.)** | ~$1,100.00 – $1,350.00 |
| **Shared Power & Networking Infrastructure** | $558.99 – $628.99 |
| **Fabrication & Assembly Tools** | $1,069.00 – $1,319.00 |
| **Cluster & Infrastructure Subtotal** | **$5,573.93 – $6,337.93** |
| **Framework Laptop 16 Workstation** | $4,165.00 |
| **Grand Total Estimate** | **$9,738.93 – $10,502.93** |

---

## 6. General Deployment & Site Requirements

1. **Power Budget:** Ensure the lab circuit can supply ~15A peak across the Bambu 3D printer, PDU rack, and work console.
2. **Thermal & Ventilation:** The combined heat dissipation from 23+ compute boards and power supplies requires active room ventilation.
3. **Spares & Prototyping:** Reserve budget buffer (~5–10%) for filament test prints, spare fasteners, or replacement patch cables.
