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

## POWER INFRASTRUCTURE

- 1U PDU Horizontal Rackmount Power Strip (Qty: 1) - Rack central power hub (cluster only) - $60.99
- Dedicated 5V/5A (25W) USB-C Power Supplies or 12V/24V Central PSU w/ Buck Converters (Qty: 6) - Dedicated 5V/5A per Orange Pi node - ~$90.00 to $120.00
- 19V 4.74A 90W DC Power Adapter w/ Barrel Jack (Qty: 1) - Dedicated power supply for Jetson Orin Nano - ~$20.00
- 100W/5A USB-C to USB-C Braided Patch Cables 1.5ft (Qty: 15) - Clean USB-C power runs - ~$30.00 *(Note: Bambu 3D Printer must be powered via a separate, dedicated wall outlet/circuit to avoid tripping the PDU breaker during bed heat-up).*

## NETWORKING

- 24-Port 2.5G Managed Switch w/ 220W+ PoE+ (Qty: 1) - Sufficient PoE headroom and manual power allocation per port - ~$340.00 to $380.00
- GEARit Cat6 Patch Cables 1ft, 24-Pack (Qty: 1) - Network patch runs - $18.00 *(Note: Requires `PSU_MAX_CURRENT=5000` added to Raspberry Pi `/boot/firmware/cmdline.txt` to enable 5A power profiling over PoE+).*

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
every OS. It separates common Debian/Ubuntu-family preparation from
Raspberry Pi-specific power settings. Validate package and service names
on your chosen Ubuntu, Raspberry Pi OS, and Armbian releases before
running it. The Jetson is intentionally excluded from the generic
Longhorn setup unless you later decide to use it as a
Kubernetes/Longhorn node.

Create `base-setup.yml` on your Framework laptop:

``` yaml
---
- name: Common preparation for Debian/Ubuntu-family cluster nodes
  hosts: pi_cluster:orange_cluster
  become: true
  tasks:
    - name: Update apt cache and upgrade packages
      ansible.builtin.apt:
        update_cache: true
        upgrade: dist
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

    - name: Enable iSCSI daemon where this service exists
      ansible.builtin.service:
        name: iscsid
        enabled: true
        state: started

- name: Raspberry Pi power configuration (verify before enabling)
  hosts: pi_cluster
  become: true
  tasks:
    - name: Add USB high-current setting only when confirmed appropriate for this OS and power setup
      ansible.builtin.lineinfile:
        path: /boot/firmware/config.txt
        line: "usb_max_current_enable=1"
        state: present
        create: false
      notify: Reboot Pi nodes

  handlers:
    - name: Reboot Pi nodes
      ansible.builtin.reboot:
        msg: "Rebooting to apply the changed Raspberry Pi configuration"
        reboot_timeout: 300
```

**Power-setting caution:** The USB current-limit setting and the
PSU-current declaration are different settings and are not
interchangeable. Do not blindly add either one to all Pis. First
document the actual supply/HAT configuration for each node and verify
the appropriate setting for the selected firmware/OS. The playbook above
deliberately flags the USB setting for confirmation rather than treating
it as a universal fix. Test on one Pi and confirm that a reboot is
actually required before applying it to all seven.

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

--k3s-extra-args "--disable=servicelb"\
--local-path \~/.kube/pi-config.yaml

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

--k3s-extra-args "--disable=servicelb"\
--local-path \~/.kube/orange-config.yaml

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
