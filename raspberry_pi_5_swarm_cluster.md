# Raspberry Pi 5 Swarm Cluster

## 1. Overview & System Role
- **Purpose:** General cluster compute nodes and master management node.
- **Node Count:** 7 Nodes Total (1 Head Node + 6 Worker Nodes).

---

## 2. Hardware Bill of Materials (BOM) & Costs

### Compute Boards
- **1x** RasTech Raspberry Pi 5 16GB Kit (Head Node / Master Controller) — **$150.00 – $170.00**
- **6x** RasTech Raspberry Pi 5 8GB Kit (Worker Nodes) — **$690.00 – $750.00**

### Storage & HAT Expansion
- **1x** Crucial P3 Plus 1TB M.2 2280 NVMe SSD (Master Node Storage) — **~$70.00**
- **6x** Fanxiang S501 128GB NVMe SSDs (Worker Node Storage) — **$215.94**
- **7x** Waveshare PCIe to M.2 HAT+ (B) 2280 Version w/ PoE — **~$125.00**

### Cooling & Mounting
- **7x** Official Raspberry Pi 5 Active Coolers — **~$35.00**
- **1x** C4Labs Zebra Bramble Cluster Case (Base enclosure for worker nodes)
- Custom 3D-Printed socket/adapter for Master Node mounting

---

## 3. Power & Networking Requirements
- **Power Source:** Power over Ethernet (PoE+) via Waveshare PCIe HAT+ (B).
- **Network Interface:** Standard 1GbE Ethernet per board connecting to central 2.5G Managed Switch (PoE+ supplied).
- **Note on Power Settings:** Do not add `PSU_MAX_CURRENT=5000` to `cmdline.txt`. This is a bootloader property, not a standard setting to make a PoE HAT supply 5A.

---

## 4. Physical Enclosure & Build Notes
- **Clearance Checks:** Verify that the C4Labs Zebra Bramble case provides adequate vertical clearance for the combined stack of the Pi 5, Official Active Cooler, and Waveshare M.2 HAT+.
- **Accessibility:** Ensure easy access to Ethernet, power connectors, and NVMe drives to simplify node swap/maintenance.
- **Prototyping:** Fit-test one node with all HATs, thermal components, and cables before assembling the entire stack.