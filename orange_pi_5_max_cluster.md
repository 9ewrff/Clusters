# Orange Pi 5 Max Swarm Cluster

## 1. Overview & System Role
- **Purpose:** High-memory SBC cluster nodes for memory-intensive workloads.
- **Node Count:** 6 Nodes Total (1 Master + 5 Workers).

---

## 2. Hardware Bill of Materials (BOM) & Costs

### Compute Boards
- **6x** Orange Pi 5 Max 16GB LPDDR5 Dev Board — **$780.00 – $840.00**

### Storage & Expansion
- **3x** Crucial P3 Plus 500GB M.2 2280 NVMe SSD (Nodes 1–3) — **~$135.00**
- **3x** Fanxiang S501 256GB NVMe SSD (Nodes 4–6) — **$66.00 – $80.00**

### Cooling & Mounting
- Custom active cooling heatsinks/fans adapted for Orange Pi 5 Max layout.
- Custom 3D-Printed Cluster Cage (based on modified Printables Model 1211068).

---

## 3. Power & Networking Requirements
- **Power Source:** Dedicated 5V/5A (25W) USB-C Power Supplies per node or central 12V/24V PSU with buck converters (**~$90.00 – $120.00**).
- **Power Cabling:** 100W/5A USB-C to USB-C Braided Patch Cables (1.5ft).
- **Networking:** Multi-Gigabit Ethernet ports connected to central 2.5G switch.

---

## 4. Physical Enclosure & Build Notes
- **CAD Workflow:** Modify Printables model 1211068. Do not assume the standard Orange Pi 5 layout matches the Orange Pi 5 Max version for ports, screw holes, or component heights.
- **Design Checks:**
  1. Measure connector alignments (Ethernet, USB-C power, HDMI).
  2. Verify vertical clearance for NVMe SSDs and cooling modules.
  3. Ensure sufficient airflow channels for stacked operation.
- **Prototyping:** Print a single-node test fit before printing the complete 6-board cage in PETG filament.