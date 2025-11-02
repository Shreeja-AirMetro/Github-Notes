The differences between **Ubuntu Server**, **Ubuntu Desktop**, and other **Linux infrastructure variants** mainly revolve around their intended use, included software, and system resource requirements.

---

### 🔹 **1. Ubuntu Server**

**Purpose**: For headless environments (no GUI), optimized for performance and remote access.

**Key Features**:

- No graphical interface by default (CLI only).
- Pre-packaged with server-related software: Apache, Nginx, OpenSSH, MySQL/PostgreSQL, etc.
- Lower resource usage (RAM/CPU).
- Ideal for: web servers, database servers, cloud VMs, file servers, etc.

**Use Cases**:

- Hosting websites
- Cloud deployments (AWS, Azure, etc.)
- Container orchestration (Docker, Kubernetes)

---

### 🔹 **2. Ubuntu Desktop**

**Purpose**: For end users who need a GUI for everyday tasks.

**Key Features**:

- Comes with a full desktop environment (GNOME by default).
- Includes GUI apps: Firefox, LibreOffice, File Manager, etc.
- More resource-heavy than Server version.
- Ideal for: personal use, development machines with GUI, testing environments.

**Use Cases**:

- Software development
- Education & learning
- Multimedia and daily use
    

---

### 🔹 **3. Other Linux Infrastructure Options**

Beyond Ubuntu, many Linux distributions (distros) cater to different infrastructure needs. Some examples include:

|Distro|Description|Use Case|
|---|---|---|
|**CentOS Stream** / **RHEL**|Enterprise-grade server OS with long support cycles|Corporate servers, data centers|
|**Debian**|Base for Ubuntu, very stable|Servers, embedded systems|
|**Fedora Server**|Cutting-edge with server-specific packages|Testing enterprise features|
|**Alpine Linux**|Ultra-lightweight, security-focused|Docker containers, microservices|
|**Arch Linux**|Rolling-release, highly customizable|Power-user servers|
|**SUSE Linux Enterprise Server (SLES)**|Enterprise server OS|Enterprise infrastructure|
|**Rocky Linux / AlmaLinux**|RHEL-compatible, community-supported|Enterprise server replacement for CentOS|
|**Kali Linux**|Security auditing and penetration testing|Cybersecurity infrastructure|
|**OpenWRT / pfSense**|Router/firewall OS|Networking infrastructure|

---

### 🔹 Summary: Ubuntu Server vs Desktop

|Feature|Ubuntu Server|Ubuntu Desktop|
|---|---|---|
|GUI|❌ No (CLI only)|✅ Yes|
|Default Packages|Server tools|GUI apps, productivity|
|Resource Usage|Low|High|
|Use Case|Headless servers, remote access|Workstations, developers|
|Target Audience|Sysadmins, DevOps|End-users, developers|

---

### 🧱 Choosing Linux Infrastructure: Key Questions

To pick the right Linux distro for your infrastructure, consider:

- **Do you need a GUI?**
- **Is it for production or experimentation?**
- **Do you need enterprise support?**
- **What kind of hardware or VM environment?**
- **Security, scalability, and update needs?**


Let me know your goals or environment type (home lab, cloud, enterprise, IoT), and I can recommend the best-fit Linux infrastructure.

For your project involving **VMs for UAV + 5G network + Ground Station**, the ideal Linux infrastructure should be:

- **Lightweight and stable**
- **Support for networking tools (SDR, 5G stack, VPN, etc.)**
- **Reliable for headless/server environments**
- **Scalable for virtualization (libvirt, KVM, etc.)**
- **Good hardware/driver compatibility for SDR, GPS, radio, etc.**
    

---

## ✅ **Recommended Linux Infrastructure Stack for Your Use Case**

|Component|Recommendation|Why|
|---|---|---|
|**Hypervisor Host OS**|**Ubuntu Server (LTS)** or **Debian**|Stable, lightweight, great for KVM/libvirt|
|**Virtual Machines**|Mix of: • Ubuntu Server • Debian • Kali Linux (if doing network penetration testing or signal security)|Flexible, easy to manage with packages for networking, 5G, SDR|
|**5G Core / RAN / EPC Stack**|Use inside VMs: • **OpenAirInterface (OAI)** • **srsRAN 5G**|Open-source 5G implementations tested on Ubuntu/Debian|
|**Ground Station (UI/Display/Telemetry)**|**Ubuntu Desktop** (if GUI is needed)|Easy support for mapping, GUI telemetry tools|
|**Network Emulation/Orchestration**|**Ubuntu Server with GNS3 / Mininet / Docker / Kubernetes**|Emulate complex network topologies|
|**Firewall / Gateway VM**|**pfSense** (FreeBSD-based) or **OPNsense**|Advanced network control & NAT for UAV links|

---

## 🔧 Example VM Setup

|VM Name|OS|Purpose|
|---|---|---|
|`uav-control`|Ubuntu Server|Sends telemetry, receives commands|
|`5g-core`|Ubuntu Server|Runs 5G core (AMF/SMF/UPF) using OAI or srsRAN|
|`5g-ran`|Ubuntu Server|Radio access (gNodeB) interfacing with SDR|
|`ground-ui`|Ubuntu Desktop|GUI apps for telemetry/map/controls|
|`net-gateway`|pfSense|NAT, VPN, firewall, routing|
|`test-agent`|Kali or Ubuntu|For security testing or simulated UAV traffic|

---

## 📡 Tools & Technologies to Consider

- **KVM + libvirt** or **Proxmox VE** (for VM management)
- **Docker / Podman** (for lightweight service isolation)
- **GNU Radio** + **SDR drivers** (e.g., USRP, RTL-SDR)
- **OpenAirInterface / srsRAN 5G** (for 5G stack)
- **ZeroMQ, ROS2, or MAVLink** (for UAV comms)
    

---

## 🧠 Final Advice

- **Use Ubuntu Server 22.04 LTS** for most VMs—it has the best support for 5G and networking stacks like OpenAirInterface.
- If you plan to do **heavy networking or GUI-based control**, one or two Ubuntu Desktop VMs are fine.
- Use **pfSense or OPNsense** for gateway/firewall/NAT functionality.
- If you want an all-in-one host OS that can run VMs, containers, and has a GUI for management, consider **Proxmox VE** (Debian-based hypervisor).


---
### VM details and VM setup from Screenshots 

To do : Setup MobaXterm terminal
Setup 
UAV --> terminal with Cell and Satcom net adapter --> cell Control --> Cell Emulator ---> Ground
                     |                                                                                                         |
                     |                                                                                                         |
                     v                                                                                                        |
                     Sat emu ---------------------------------------------------------------



### Key details for each VM 
1. OS
2. Network adapters 
3.  Serial Ports 
4. Check USB
UAV - normal ubuntu machine 
![[uav.png|1200]]


### UAV OS: Ubuntu 64 bit 
Network Adapters : 
	- Adap 1 - Host only adapter Virtualbox Host-Only Ethernet Adapter
	- Adap 2 - UAV to terminal - Internal Network 
Ports: 
	- Port 1: Serial port enabled COM1 IRQ 4 I7O Port: 03F8  Port Mode: Hostpipe Path: \\.\pipe\uavusb
	- Port 2: Serial port COM2 IRQ 3 I/o Port 02F8 Host pipe  \\.\pipe\uavterminal1
	- Port 3: COM3 IRQ 4, I/O port 03E8 Host Pipe \\.\pipe\uavterminal2


### Terminal Ubuntu 64bit 
![[terminal.png|1200]]

Adapter 
	- Adap 1: Host only Adapter virtual Box Host-only Ethernet Adapter 
	- Adap 2 - uav  to terminal internal network 
	- Adap 3 - terminal to sat internal network
	- Adap 4 - terminal to cell internal network
		- Adapter type: Intel Pro/1000 MT Desktop , Promiscuous Mode: Deny Mac address :  - Cable connected
Port 
port 1 and port 2

### Cell Ctrl 
![[cell-ctrl.png|1200]]
Adap 3 - Internal cell to cell - Paravirtualized Network (virtio-net)
Deny , Cable connected 
ctrl no port USB and Adapters 
### Cell Emulator Fedora 64 bit

Adapter:
	 Adap 1 - Paravirtualized Network Host-only- VirtualBox-Only Ethernet Adapter 
	 Adap 2 paravirtualized Network - Internal Network Celltocell 
	 Adap 3 - paravirtualized Network - Internal Network Cell emu to ground

### Ground  ubuntu 64 bit
![[ground.png|1200]]
USB : Usb 1.1 OHCI Controller 
Adapter 
	Adap 1 Virtual Host only ethernet adapter 
	Adap 2 - cellto cell Intel Pro
	Adap 3 Internal Network Satemu to ground - Intel Pro
no port
USB

### Details 

fedora add delay, packet loss 
sat emu+ sat control is together 
In UAV VM build aand make px4,  MAVlink, SITL

commands
make link -cell open 
ppp@172.22.2.1
run router - set low latency serial link 
at terminal - link both open 
test terminal low latency, high latency 
ground : test cell link and satllink 


### References 

1. https://brianlinkletter.com/2019/02/build-a-network-emulator-using-libvirt/
2. https://github.com/cmu-sei/welled
3. https://brianlinkletter.com/open-source-network-simulators/
4. https://blog.purestorage.com/purely-technical/emulation-vs-virtualization/
5. 