# Hardware Plan & Budget

## COMPUTE NODES & AI

- Orange Pi 5 Max 16GB LPDDR5 Dev Board (Qty: 6) - High-memory cluster nodes - $780.00 to $840.00
- RasTech Raspberry Pi 5 8GB Kit (Qty: 6) - General cluster compute nodes - $690.00 to $750.00
- RasTech Raspberry Pi 5 16GB Kit (Qty: 1) - Cluster Head Node / Master Controller - $150.00 to $170.00
- Yahboom Jetson Orin Nano 8GB SUB Dev Kit (Qty: 1) - Dedicated AI/ML hardware node - $559.00 to $599.00
- Bambu Lab P2S Combo 3D Printer & AMS 2 Pro (Qty: 1) - Custom enclosure & chassis fabrication - $949.00 to $1,199.00

## WORKSTATION / MANAGEMENT CONSOLE

- Framework Laptop 16 Custom Build (Qty: 1) - Primary control machine & portable workstation - $4,165.00
  - AMD Ryzen AI 9 HX 370, Radeon RX 7700S GPU Module
  - 32GB (2 x 16GB) DDR5-5600 RAM
  - 2TB SANDISK 850X (2280) + 2TB SANDISK SN770M (2230)
  - Black Bezel, Haptic Touchpad, US English Keyboard, 2x LED Matrix, RGB Macropad, Black & Orange Spacers
  - Expansion Cards: USB-C (Silver & Orange), USB-A (Black), Ethernet, MicroSD, SD, Audio

## CUSTOM FABRICATION, CASES & COOLING

- Official Raspberry Pi 5 Active Coolers (Qty: 7) - Dedicated active cooling for standard Pi 5 SBCs - ~$35.00
- PETG Filament 1.75mm 1kg Spools (Qty: 3) - High-heat filament for 3D printing custom 19" 3U/4U cluster rack drawers - ~$60.00
- M2.5 & M3 Brass Standoff + Screw Kit 300+ PCS (Qty: 1) - PCB and board mounting - ~$15.00
- Heat-Set Insert Installation Kit M2.5 / M3 (Qty: 1) - Threaded metal sockets for 3D prints - ~$20.00
- Nicpro 58PCS Art Drawing Supplies Kit (Qty: 1) - Finishing/labeling - $25.00

## CLUSTER ENCLOSURES & 3D-PRINTED MODIFICATIONS

This section records the planned physical enclosure approach. The designs are starting points, not yet verified fits for every board revision or the full NVMe/cooling configuration. Prototype one node and one section before printing or purchasing parts for the complete clusters.

### Cluster 1 — Raspberry Pi 5 swarm

- **Base enclosure:** [C4Labs Zebra Bramble cluster case](https://www.amazon.com/dp/B07VNHDM5Y) for the six Raspberry Pi 5 8GB worker nodes.
- **Master node:** Raspberry Pi 5 16GB, mounted in a custom 3D-printed socket/adapter designed to fit the chosen enclosure layout.
- **Cooling:** The plan includes seven official Raspberry Pi 5 Active Coolers. Confirm that the Bramble case has enough vertical clearance and airflow for the coolers on all seven boards.
- **NVMe:** The seven Pi nodes are planned to use Waveshare PCIe-to-M.2 HAT+ (B) boards with NVMe drives and PoE. Check the actual HAT/SSD stack height against the enclosure; the unmodified case may not provide enough room.
- **Design checks:** Confirm board mounting-hole positions, USB/Ethernet/power connector access, cable bend radius, SSD access, and room to remove an individual node for maintenance. If needed, modify the case spacers or create a taller mounting layer rather than forcing boards or connectors into place.

### Cluster 2 — Orange Pi 5 Max swarm

- **Base design to modify:** [Orange Pi 5 SBC Cluster Cage — Printables model 1211068](https://www.printables.com/model/1211068-orangepi-5-sbc-cluster-cage).
- **Cluster layout:** Six Orange Pi 5 Max 16GB boards, with one master and five workers.
- **Modification goal:** Retain the original cage's general stacking/layout concept, but adapt board mounts and clearances for the Orange Pi 5 Max. Do not assume the original Orange Pi 5 version matches the Max board's dimensions, mounting holes, port placement, or cooling hardware.
- **CAD workflow:** Prefer STEP or other editable CAD source if the creator provides it. If only STL files are available, mesh editing is possible but may make precise changes to mounting features harder. Keep an untouched copy of the original model and save the modified version as a separate project.
- **Required checks before printing the full cage:**
  1. Compare the Orange Pi 5 Max board outline and mounting-hole locations with the original model.
  2. Check Ethernet, USB, HDMI, USB-C power, and other required connectors against the cage walls and neighboring boards.
  3. Allow room for the selected heatsink/fan and airflow between stacked boards.
  4. Check NVMe-drive and adapter placement, if used, so they do not collide with the next layer.
  5. Add sensible cable paths, node labels (master / worker-1 through worker-5), and accessible fasteners.
  6. If the cage will attach to a shelf or rack, add mounting points only after checking the printed frame's strength and dimensions.
- **Prototype-first rule:** Print one mounting section or a single-board fit test first. Test with a real Orange Pi 5 Max, its cooling hardware, NVMe hardware (if fitted), and connected cables. Check stability, access, and temperatures before printing the complete six-board cage.

### Fabrication and material notes

- PETG is the planned filament. Print a small fit-test first and account for printer tolerances; holes and slots may need tuning for the actual printer and filament profile.
- Use M2.5/M3 hardware only where it matches the board and model's intended fasteners. Avoid screws or standoffs that can touch components or stress the PCB.
- Do not treat a printed enclosure as a heatsink. Preserve airflow and verify sustained-load temperatures after assembly.
- **Budget status:** The enclosure links above are design choices, but their exact purchase prices, any required extra hardware, and the cost of failed prototypes have not been added to the grand total. Recheck the budget after the final enclosure design and bill of materials are known.

## POWER INFRASTRUCTURE

- 1U PDU Horizontal Rackmount Power Strip (Qty: 1) - Rack central power hub (cluster only) - $60.99
- Dedicated 5V/5A (25W) USB-C Power Supplies or a properly rated 12V/24V central PSU with buck converters (Qty: 6) - Intended for the six Orange Pi nodes; verify the exact Orange Pi 5 Max input specification before buying - ~$90.00 to $120.00
- 19V 4.74A 90W DC Power Adapter w/ Barrel Jack (Qty: 1) - Dedicated power supply for Jetson Orin Nano - ~$20.00
- 100W/5A USB-C to USB-C Braided Patch Cables 1.5ft (Qty: 15) - Clean USB-C power runs - ~$30.00 *(Note: Bambu 3D Printer must be powered via a separate, dedicated wall outlet/circuit to avoid tripping the PDU breaker during bed heat-up).*

## NETWORKING

- 24-Port 2.5G Managed Switch w/ 220W+ PoE+ (Qty: 1) - Sufficient PoE headroom and manual power allocation per port - ~$340.00 to $380.00
- GEARit Cat6 Patch Cables 1ft, 24-Pack (Qty: 1) - Network patch runs - $18.00 *(Power note: do not add `PSU_MAX_CURRENT=5000` to `cmdline.txt`. Raspberry Pi documents this as a bootloader configuration property, not a way to make a PoE HAT supply 5A. See the power-verification section below.)*

## STORAGE & EXPANSION

- Crucial P3 Plus 500GB M.2 2280 NVMe SSD (Qty: 3) - Orange Pi nodes 1–3 - ~$135.00
- Fanxiang S501 256GB NVMe SSD (Qty: 3) - Orange Pi nodes 4–6 - $66.00 to $80.00
- Waveshare PCIe to M.2 HAT+ (B) 2280 Version w/ PoE (Qty: 7) - Full 2280 SSD & PoE power support for RPi 5 nodes - ~$125.00
- Crucial P3 Plus 1TB M.2 NVMe SSD (Qty: 1) - RPi 5 16GB Head Node - ~$70.00
- Fanxiang S501 128GB NVMe SSD (Qty: 6) - RPi 5 8GB Worker Nodes - $215.94

### Itemized Hardware Breakdown

**[1] Compute Nodes & AI Boards (15 Units Total)**

- 6x Orange Pi 5 Max 16GB RAM LPDDR5
- 6x Raspberry Pi 5 8GB Kits
- 1x Raspberry Pi 5 16GB Kit
- 1x Yahboom Jetson Orin Nano 8GB SUB Kit
- 1x Bambu Lab P2S Combo 3D Printer

**[2] Workstation / Management Console (1 Unit Total)**

- 1x Framework Laptop 16 (Ryzen AI 9 HX 370, RX 7700S, 32GB RAM, 4TB Total NVMe)

**[3] Custom Fabrication, Mounting & Cooling (13 Items / Kits)**

- 7x Official Raspberry Pi 5 Active Coolers
- 3x PETG Filament Spools (1kg each)
- 1x M2.5 & M3 Brass Standoff + Screw Kit
- 1x Heat-Set Insert Installation Kit
- 1x Nicpro 58PCS Art Drawing Supplies Kit

**[4] Power Infrastructure (23 Items / Bundles)**

- 1x 1U Horizontal Rackmount PDU (Cluster Only)
- 6x Dedicated 5V/5A (25W) USB-C Power Supplies or Central 12V/24V PSU w/ Buck Converters
- 1x 19V 4.74A DC Power Adapter (Jetson)
- 15x 100W USB-C to USB-C Cables (1.5ft)

**[5] Networking (2 Bundles Total)**

- 1x 24-Port 2.5G Managed Switch (220W+ PoE+ Budget)
- 1x GEARit Cat6 Patch Cables (24-Pack)

**[6] Storage & Pi Expansion (20 Total Units)**

- 3x Crucial P3 Plus 500GB M.2 2280 NVMe SSDs
- 3x Fanxiang S501 256GB NVMe SSDs
- 7x Waveshare PCIe to M.2 HAT+ (B) 2280 Adapters w/ PoE
- 1x Crucial P3 Plus 1TB M.2 2280 NVMe SSD
- 6x Fanxiang S501 128GB NVMe SSDs

### Updated Final Cost Summary

| Category | Cost Range |
| --- | ---: |
| Compute Boards & 3D Printer Subtotal | $3,128.00 – $3,558.00 |
| Custom Fabrication, Cases & Cooling | $155.00 |
| Power Infrastructure Subtotal | $200.99 – $230.99 |
| Networking Subtotal | $358.00 – $398.00 |
| Storage & Pi Expansion Subtotal | $611.94 – $625.94 |
| **Cluster & Infrastructure Subtotal** | **$1,325.93 – $1,409.93** |
| Framework Laptop 16 Addition | $4,165.00 |
| **Updated Grand Total Estimate** | **$8,618.93 – $9,132.93** |

---

## Hardware Verification Notes — Read Before Buying

### Raspberry Pi 5 power and Waveshare PoE M.2 HAT+ (B)

The listed HAT appears to be the Waveshare **PoE M.2 HAT+ (B)**, not the similarly named original PoE M.2 HAT+. The manufacturer's product page lists Raspberry Pi 5 support, IEEE 802.3af/at PoE, NVMe drives in 2230/2242/2260/2280 sizes, and compatibility with the official Pi 5 Active Cooler. Its published output is **5V up to 4.5A** from the GPIO header and **12V up to 2A** from the 2-pin header, with a stated combined output limit of about 25W. This is not the same as guaranteeing 5V/5A to the Pi in every workload.

**Power-setting correction:**
- Do **not** put `PSU_MAX_CURRENT=5000` in `/boot/firmware/cmdline.txt`. Raspberry Pi documents `PSU_MAX_CURRENT` as a bootloader configuration property; it tells firmware to assume a supply current rating and skip USB-PD negotiation. It does not increase the physical output of a PoE HAT.
- Waveshare's HAT wiki mentions `usb_max_current_enable=1` in `/boot/firmware/config.txt` if a power-limit warning appears. Do not force this setting automatically across all seven nodes. First follow the instructions for the exact HAT and OS, and verify that the actual supply path can safely support the selected setting.
- The seven Raspberry Pi nodes are intended to use the seven PoE HATs. The six 5V/5A supplies listed above are for the six Orange Pi nodes, not the Raspberry Pis. Keep the power paths clearly separated in the final wiring diagram.
- The switch model is not specified in this plan, so its PoE budget cannot yet be confirmed. Seven 802.3at ports can each request up to 30W at the switch side; a 220W aggregate budget leaves little headroom if all seven nodes approach their maximum draw. Check the switch's **per-port 802.3at support and total PoE budget**, account for conversion losses, and validate real node draw under CPU + NVMe load. If uncertain, choose a switch with more PoE headroom or use a separately engineered power plan.
- The 100W rating on a USB-C cable is only a cable rating; it does not provide power without a suitable source.

### NVMe and physical fit

The listed Crucial P3 Plus and Fanxiang S501 drives are intended to be NVMe M.2 drives; verify each exact SKU before purchase. The PoE M.2 HAT+ (B) supports 2280 NVMe drives, but the Raspberry Pi's PCIe link and firmware determine actual speed, so do not expect the SSD's advertised maximum Gen4 speed on a Pi 5. The manufacturer's page says the (B) version is compatible with the official Pi 5 Active Cooler, but still prototype one assembled node in the planned rack drawer and check connector access, SSD clearance, airflow, and temperatures.

### Items that cannot be fully verified from the current list

- **PoE switch:** no manufacturer/model number is listed, so exact port standards, aggregate power budget, and management features remain unverified.
- **Orange Pi 5 Max power supply:** confirm the official input voltage/current for the exact board revision and selected supply before buying.
- **Orange Pi OS + Longhorn:** support depends on the exact Armbian image, kernel, architecture, and current Longhorn release. Prove NVMe detection, required kernel/filesystem features, iSCSI, and persistent-volume mounting on one node before committing to six.
- **Jetson adapter:** confirm that the 19V adapter's barrel size, polarity, voltage, and current match the exact Yahboom kit documentation. Do not rely on voltage/current alone.
- **Printer circuit:** use the printer's manufacturer-rated supply and a properly rated outlet/circuit. A separate outlet does not necessarily mean a separate electrical circuit; avoid overloading a circuit and ask a qualified adult/electrician if unsure.

# Software Plan

**Software:**

### CLUSTER 1: THE PI SWARM (General Compute & Routing)

**Hardware:** 1x Pi 5 16GB (Master) + 6x Pi 5 8GB (Workers)

-   **Operating System:** Ubuntu Server 24.04 LTS (64-bit) or Raspberry
    Pi OS Lite (64-bit) -- *Choose one consistently where practical,
    then validate kernel and Longhorn prerequisites on that OS.*
-   **Orchestration Engine:** K3s by SUSE -- *Lightweight Kubernetes
    designed for edge devices.*
-   **Distributed Storage:** Longhorn -- *Provides replicated volumes
    across eligible nodes in this cluster; it does not create one
    automatically combined disk. Capacity depends on replica count,
    placement, and reserved space.*
-   **Networking / Ingress:** MetalLB (Load Balancer) & Traefik (Ingress
    Controller) -- *Routes local network traffic to your containers.*
-   **Monitoring:** Prometheus & Grafana -- *Dashboards for cluster
    health, RAM usage, and thermal tracking.*

### CLUSTER 2: THE ORANGE PI SWARM (Heavy Compute & Databases)

**Hardware:** 1x Orange Pi 5 Max (Master) + 5x Orange Pi 5 Max (Workers)

-   **Operating System:** A supported Armbian image for the exact Orange
    Pi 5 Max model -- *Verify board support, kernel features, and
    Kubernetes/Longhorn compatibility before deployment.*
-   **Orchestration Engine:** K3s by SUSE -- *Runs as a completely
    independent Kubernetes cluster from the Pis.*
-   **Distributed Storage:** Longhorn (preferred if compatibility checks
    pass) or OpenEBS (evaluate separately) -- *Storage is managed
    independently from the Raspberry Pi cluster; the two clusters do not
    share one automatic storage pool.*
-   **Workload Focus:** PostgreSQL/Redis clusters, CI/CD runners, and
    data processing backends.

### STANDALONE AI NODE (Machine Learning Inference)

**Hardware:** 1x Jetson Orin Nano

-   **Operating System:** Nvidia JetPack SDK (Ubuntu-based) -- *Required
    to unlock proprietary CUDA and Tensor core drivers.*
-   **Container Runtime:** Docker Engine + Nvidia Container Toolkit --
    *Do not use Kubernetes here; standalone Docker makes GPU passthrough
    seamless.*
-   **AI Services:** Ollama (LLMs), Whisper (Audio), or YOLO (Vision) --
    *Exposed as REST APIs for the two K3s clusters to call over the
    network.*

### WORKSTATION / MANAGEMENT CONSOLE

**Hardware:** Framework Laptop 16

-   **Operating System:** Ubuntu 24.04 LTS or Fedora Workstation.
-   **Infrastructure Automation:** Ansible -- *Uses a hosts.ini
    inventory and separate common/platform-specific tasks for the 7
    Raspberry Pis, 6 Orange Pis, and Jetson. Test against one node
    before broad rollout.*
-   **Cluster Bootstrap:** k3sup ("ketchup") -- *A command-line tool
    used to install K3s on both clusters over SSH in seconds.*
-   **Cluster Management:** K9s & kubectl -- *Terminal-based dashboards
    to switch between and manage both K3s clusters instantly.*

**Setting it up:**

1.  **Flash with ext4:Raspberry Pi Imager / BalenaEtcher.**

**Choose and validate the OS image for each board before deployment. Use
ext4 or XFS for Longhorn data as supported by the selected Longhorn
release and host OS. Confirm the root filesystem and partition layout
after first boot; do not assume every image expands exactly as expected.
Because Longhorn data may share the root drive, reserve space for the
OS, logs, and container images, and monitor free space.**

2.  **Install Storage Dependencies:Run via Ansible.**

**Before installing Longhorn, verify the current Longhorn prerequisites
for each selected OS/kernel. Install the required host packages on the
Kubernetes nodes in both clusters; package names and service names can
vary by OS. Add OS-aware tasks to Ansible rather than assuming all 14
nodes are identical:**

**apt update && apt install open-iscsi nfs-common util-linux -y**

3.  **Enable the iSCSI Daemon:Critical for persistent volumes.**

**The iSCSI service must be active so your Kubernetes pods can
successfully mount the Longhorn volumes, especially after a node
reboot:**

**systemctl enable --now iscsid**

**Storage safety note:**

Because Longhorn data may share a drive with the OS, a workload that
consumes too much storage can leave the host without enough free space.
Do **not** automatically lower Longhorn's Storage Minimal Available
Percentage from 25% to 15%. Choose a threshold only after calculating OS
and workload needs; keep adequate free space for the OS, logs, container
images, and updates. Configure replica counts and placement
deliberately, monitor disk usage, and test what happens when a node or
drive fails. Replication consumes additional capacity: two replicas need
roughly twice, and three replicas roughly three times, the logical
volume size, before other overhead.

This playbook is a starting template, not a drop-in configuration for
every OS. It applies common Debian/Ubuntu-family preparation to the two
Kubernetes clusters and deliberately leaves all Raspberry Pi power
settings untouched. Validate package and service names on your chosen
Ubuntu, Raspberry Pi OS, and Armbian releases before running it. The
Jetson is intentionally excluded from the generic Longhorn setup unless
you later decide to use it as a Kubernetes/Longhorn node.

Create `base-setup.yml` on your Framework laptop. This is a **starting template**: validate package/service names on each selected OS first, and run it against one test node before a full rollout. It deliberately does not change Raspberry Pi power settings.

```yaml
---
- name: Common preparation for Debian/Ubuntu-family cluster nodes
  hosts: pi_cluster:orange_cluster
  become: true
  tasks:
    - name: Update apt cache
      ansible.builtin.apt:
        update_cache: true
        cache_valid_time: 3600

    - name: Install common tools and Longhorn prerequisites
      ansible.builtin.apt:
        name:
          - curl
          - git
          - util-linux
          - open-iscsi
          - nfs-common
          - nvme-cli
        state: present

    - name: Enable iSCSI daemon
      ansible.builtin.service:
        name: iscsid
        enabled: true
        state: started
```

**Do not add a power-setting task to this playbook yet.** First establish which nodes use the Waveshare PoE HAT and which firmware/OS is installed. If a manufacturer-documented setting is needed, apply it manually to one test Pi after confirming the power supply can support it, reboot only if required, and verify the result before automating it.

To run this, you will also need your inventory file. Create hosts.ini in
the same directory:

    [pi_cluster]
    192.168.1.50
    192.168.1.51
    192.168.1.52
    192.168.1.53
    192.168.1.54
    192.168.1.55
    192.168.1.56

    [orange_cluster]
    192.168.1.60
    192.168.1.61
    192.168.1.62
    192.168.1.63
    192.168.1.64
    192.168.1.65

    [ai_node]
    192.168.1.70

    [all:children]
    pi_cluster
    orange_cluster
    ai_node

*(Be sure to replace the IPs above with the actual IP addresses your
router assigns to the boards).*

Run the playbook from your laptop terminal:

    ansible-playbook -i hosts.ini base-setup.yml -K

With the operating systems prepped and dependencies installed, it is
time to turn these independent boards into two unified Kubernetes
clusters.

You will use **k3sup** (pronounced "ketchup") on your Framework laptop.
It connects to your nodes over SSH, installs the K3s binary, and
automatically downloads the kubeconfig files to your laptop so you can
manage the clusters locally.

**1.Install k3sup and kubectl:**Run on your Framework laptop.

Download the k3sup binary and install the Kubernetes command-line tool
(kubectl) on your control machine so you can interact with the clusters.

Bash

    curl -sLS https://get.k3sup.dev | sh
    sudo install k3sup /usr/local/bin/
    sudo snap install kubectl --classic

**2.Bootstrap the Pi Cluster (Master):**

Create the first cluster by installing the K3s server on your 16GB
Raspberry Pi. This command saves the access credentials as
pi-config.yaml.

Bash

    mkdir -p ~/.kube
    k3sup install --ip 192.168.1.50 --user clusteradmin \
      --k3s-channel stable \
      --k3s-extra-args "--disable servicelb" \
      --local-path "$HOME/.kube/pi-config.yaml"

**3.Join the Pi Worker Nodes:**IPs:

Instead of typing the command six times, use a simple bash loop to join
all 8GB Pi nodes to the master.

Bash

    for i in {51..56}; do
      k3sup join --ip 192.168.1.$i --server-ip 192.168.1.50 \
        --user clusteradmin --k3s-channel stable
    done

**4.Bootstrap the Orange Pi Cluster (Master):**

Now, create the completely isolated second cluster on your first Orange
Pi 5 Max. This saves a separate configuration file named
orange-config.yaml.

Bash

    k3sup install --ip 192.168.1.60 --user clusteradmin \
      --k3s-channel stable \
      --k3s-extra-args "--disable servicelb" \
      --local-path "$HOME/.kube/orange-config.yaml"

**5.Join the Orange Pi Worker Nodes:**IPs: .61 to .65.

Loop through the remaining Orange Pi IP addresses to join them to their
master node.

Bash

    for i in {61..65}; do
      k3sup join --ip 192.168.1.$i --server-ip 192.168.1.60 \
        --user clusteradmin --k3s-channel stable
    done

## Verifying Your Clusters

Because you have two separate clusters, you must tell kubectl which one
you want to talk to by setting the KUBECONFIG environment variable.

**To view the Pi Swarm:**

Bash

    export KUBECONFIG=~/.kube/pi-config.yaml
    kubectl config current-context
    kubectl get nodes -o wide

*(You should see all 7 Pi nodes listed with a Ready status).*

**To view the Orange Pi Swarm:**

Bash

    export KUBECONFIG=~/.kube/orange-config.yaml
    kubectl config current-context
    kubectl get nodes -o wide

*(You should see all 6 Orange Pi nodes listed with a Ready status).*

Deploying Longhorn will bind all the NVMe drives in your clusters into a
highly available, replicated storage pool. Because Longhorn runs as a
cloud-native application inside Kubernetes, the easiest and most
standard way to install it is using **Helm** (the package manager for
Kubernetes).

You will run these commands from your Framework laptop terminal to
deploy Longhorn onto both clusters.

**1.Install Helm:**Run on your Framework laptop.

If you don't have Helm installed on your Linux laptop yet, grab the
official installation script.

Bash

    curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
    bash get_helm.sh

**2.Add the Longhorn Helm Repo:**Add the repository to Helm.

Tell Helm where to find the Longhorn installation packages and update
your local repository list.

Bash

    helm repo add longhorn https://charts.longhorn.io
    helm repo update

**3.Deploy to the Pi Cluster:**KUBECONFIG=\~/.kube/pi-config.yaml.

Set your terminal context to the Pi cluster, then tell Helm to create a
dedicated namespace and install Longhorn.

Bash

    export KUBECONFIG=~/.kube/pi-config.yaml

    helm install longhorn longhorn/longhorn \
      --namespace longhorn-system \
      --create-namespace

*Note: It will take a minute or two for all the Longhorn pods to spin
up. You can watch the progress with kubectl get pods -n longhorn-system
-w.*

**4.Deploy to the Orange Pi
Cluster:**KUBECONFIG=\~/.kube/orange-config.yaml.

Switch your terminal context to the Orange Pi cluster and run the exact
same installation command.

Bash

    export KUBECONFIG=~/.kube/orange-config.yaml

    helm install longhorn longhorn/longhorn \
      --namespace longhorn-system \
      --create-namespace

**5.Access the UI and Adjust Storage Limits:**Critical Safety Setting.

Remember the warning about keeping enough free space for the OS? First,
port-forward the Longhorn UI to your laptop. Review the Storage Minimal
Available Percentage setting on each cluster and choose a value based on
measured capacity and OS needs; do not automatically change the default
to 15%:

Bash

    # Ensure you are targeting the right cluster, then run:
    kubectl port-forward -n longhorn-system svc/longhorn-frontend 8000:80

Open your laptop's browser and go to http://localhost:8000.

Navigate to **Settings \> General** and review **Storage Minimal
Available Percentage**. Keep an adequate reserve for the OS and
workloads; apply a changed value only after documenting why it is
appropriate. Repeat the review for the second cluster.

Once Longhorn is running and a StorageClass/PVC is configured,
applications can request persistent volumes. Confirm the StorageClass
replica settings and eligible disks before deploying databases. Each
cluster's Longhorn deployment uses only that cluster's drives.

**1.Carve out IP address ranges:**

Check your router's subnet and DHCP settings and reserve a block of
unused IP addresses **outside** the DHCP assignment range. Confirm that
addresses are on the correct Layer-2 subnet and are not already
statically assigned.

You will need a distinct, non-overlapping block for each cluster so they
don't fight over the same IPs. The example ranges below are placeholders
only; adapt them to your actual subnet and router configuration.

**2.Install MetalLB via Helm:**Run on your Framework laptop.

Use Helm to deploy the MetalLB controller. (Remember to swap your
KUBECONFIG context and run this for both clusters).

Bash

    helm repo add metallb https://metallb.github.io/metallb
    helm repo update

    helm install metallb metallb/metallb \
      --namespace metallb-system \
      --create-namespace

**3.Create the Address Pool:**metallb-pool.yaml.

MetalLB sits completely idle until you give it a pool of addresses to
manage. Create a file named metallb-pool.yaml.

*(Be sure to update the IP range below to match the safe block you
identified in Step 1).*

YAML

    apiVersion: metallb.io/v1beta1
    kind: IPAddressPool
    metadata:
      name: primary-pool
      namespace: metallb-system
    spec:
      addresses:
      - 192.168.1.200-192.168.1.220
    ---
    apiVersion: metallb.io/v1beta1
    kind: L2Advertisement
    metadata:
      name: primary-l2
      namespace: metallb-system
    spec:
      ipAddressPools:
      - primary-pool

**4.Apply the Configuration:**

Apply the configuration to activate the pool. You will need to create
and apply a slightly different version of this file (with a different IP
range) for your second cluster.

Bash

    kubectl apply -f metallb-pool.yaml

**K3s prerequisite:** K3s enables its built-in ServiceLB by default.
Because this design uses MetalLB instead, disable ServiceLB when
creating each cluster (the `k3sup install` examples above include
`--k3s-extra-args "--disable=servicelb"`). If you change this on an
already-running cluster, follow the K3s documentation for safely
updating server configuration rather than blindly rerunning the install
command.

**Jetson Nano:**

Setting up the Jetson Orin Nano is different from standard Linux boards
because it relies on Nvidia's proprietary **JetPack SDK**, which bundles
Ubuntu with the necessary GPU drivers (CUDA, TensorRT). The good news is
that JetPack comes with Docker and the Nvidia Container Toolkit
pre-installed.

Here is how to get the AI node ready for inference.

**1.Install the JetPack SDK:**Flash the OS.

Unlike your Pi clusters, do not use standard Ubuntu. Download the
**Jetson Linux (JetPack) SD Card Image** directly from Nvidia's
developer site. Flash it to an SD card (or NVMe drive) using
BalenaEtcher, insert it into the Jetson, and complete the initial Ubuntu
setup on a monitor.

**2.Enable Docker Without Sudo:**Run on the Jetson terminal.

Docker is already installed by JetPack, but you need to add your user to
the Docker group so you don't have to type sudo for every command.

Bash

    sudo usermod -aG docker $USER

*Note: You must log out and log back in (or run newgrp docker) for this
change to take effect.*

**3.Set NVIDIA as the Default Runtime:**Optional but highly recommended.

The Nvidia Container Toolkit is also pre-installed. By default, you have
to add --gpus all to every Docker run command. You can configure Docker
to use the Nvidia runtime automatically.

Edit the Docker daemon configuration file:

Bash

    sudo nano /etc/docker/daemon.json

Update it to look like this (adding the "default-runtime" line):

JSON

    {
        "runtimes": {
            "nvidia": {
                "path": "nvidia-container-runtime",
                "runtimeArgs": []
            }
        },
        "default-runtime": "nvidia"
    }

Restart Docker to apply the changes:

Bash

    sudo systemctl restart docker

**4.Test the GPU Passthrough:**

Verify that Docker can see the Orin Nano's GPU by running Nvidia's base
container for Jetson devices (L4T - Linux for Tegra).

Bash

    docker run --rm -it nvcr.io/nvidia/l4t-base:35.4.1 /bin/bash

*(Choose a container tag compatible with the JetPack/L4T version
installed on the device. Do not assume `35.4.1` is appropriate; check
NVIDIA compatibility documentation first.)*

Once inside the container, run:

Bash

    cat /etc/nv_tegra_release

This only reports the container's L4T release; it does **not** prove
CUDA/GPU acceleration is working. Type `exit`, then run a
CUDA-compatible test container/workload supported by your JetPack
release and verify that CUDA initializes successfully and the GPU is
visible from inside the container. Follow NVIDIA's Jetson container
documentation for the exact test image and command.

With the base environment complete, this node is ready to host heavy AI
workloads as standalone Docker containers, keeping the heavy GPU
processing off your K3s clusters.


## Final Bring-Up Checklist

Use this sequence when the hardware is eventually available. Do not skip directly to the full deployment.

1. **One Raspberry Pi node:** boot the selected OS, check undervoltage/power warnings, confirm the PoE HAT and NVMe drive are detected, and run a sustained CPU + disk test while watching temperatures.
2. **Power budget:** record the switch model, PoE standard per port, aggregate PoE budget, and measured draw. Confirm the seven-node plan has margin; do not infer it from the “220W+” label alone.
3. **One Orange Pi node:** verify the exact board-supported OS image, power supply, NVMe detection, Ethernet stability, kernel, and storage prerequisites.
4. **Ansible:** run syntax validation (`ansible-playbook --syntax-check -i hosts.ini base-setup.yml`) and then target a single test host. Check the inventory groups carefully; the generic playbook intentionally excludes the Jetson.
5. **K3s:** install one server and one worker first. Confirm both are `Ready` before joining the remaining nodes. Check the installed k3sup help for `--k3s-extra-args` syntax and keep the ServiceLB/MetalLB plan consistent.
6. **MetalLB:** reserve unused addresses outside DHCP and use non-overlapping pools for the two separate clusters. Deploy a test LoadBalancer service and confirm it can be reached from another machine on the LAN.
7. **Longhorn:** install only after the required dependencies and supported filesystem are confirmed. Create a small test PVC, write/read data, reboot a node, and test a node/drive-loss scenario before putting important data on it.
8. **Jetson:** match the container to the installed JetPack/L4T release and run a supported CUDA/PyTorch or inference test. `cat /etc/nv_tegra_release` alone is not a GPU test.
9. **Rack prototype:** print one drawer first. Check cooler/HAT/SSD fit, cable bend radius, airflow, safe access to connectors, and sustained temperatures before printing the full rack.

### Official references used for this review

- Raspberry Pi documentation — power supply, PoE, and bootloader configuration: https://www.raspberrypi.com/documentation/computers/raspberry-pi.html and https://www.raspberrypi.com/documentation/computers/config_txt.html
- Waveshare — PoE M.2 HAT+ (B) product specifications and wiki: https://www.waveshare.com/product/poe-m.2-hat-plus-b.htm and https://www.waveshare.com/wiki/PoE_M.2_HAT%2B_%28B%29
- k3sup — command-line usage and `--k3s-extra-args`: https://github.com/alexellis/k3sup
- Longhorn — installation requirements: https://longhorn.io/docs/1.13.0/deploy/install/
- NVIDIA — Jetson Orin Nano CUDA and Docker setup: https://docs.nvidia.com/jetson/orin-nano-devkit/user-guide/setup_cuda.html and https://docs.nvidia.com/jetson/orin-nano-devkit/user-guide/latest/setup_docker.html

The exact switch model, exact Orange Pi power supply, and physical thermal performance remain unverified because the plan does not provide enough detail or actual hardware to test them.
