# Jetson Orin Nano AI Node

## 1. Overview & System Role
- **Purpose:** Dedicated AI/ML edge inference and acceleration node.
- **Node Count:** 1 Standalone Node.

---

## 2. Hardware Bill of Materials (BOM) & Costs

### Compute Board
- **1x** Yahboom Jetson Orin Nano 8GB SUB Dev Kit — **$559.00 – $599.00**

### Power Supply
- **1x** 19V 4.74A 90W DC Power Adapter with Barrel Jack — **~$20.00**

### Storage & Mounting
- Shared allocation from cluster accessories / M2.5 brass standoffs.
- Optional custom 3D-printed rack shelf adapter.

---

## 3. Power & Networking Requirements
- **Power Input:** Dedicated 19V DC barrel jack input (powered via central 1U PDU or wall outlet).
- **Network Interface:** 1GbE / Multi-Gigabit Ethernet connected to central managed switch.

---

## 4. Integration Notes
- **Placement:** Can be mounted alongside or within the cluster 19" rack drawer setup.
- **Thermal Management:** Ensure uninhibited intake and exhaust airflow around the Jetson fan assembly during heavy ML workloads.