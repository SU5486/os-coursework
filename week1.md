# Week 1 – System Planning and Setup

## 1. System Architecture

![System Architecture](assets/week1-architecture.png)

The system uses a dual-machine architecture. A Windows workstation is used for administration, while Ubuntu Server runs as a headless virtual machine inside VirtualBox. The server is accessed remotely using SSH, which reflects real-world server management practices.

## 2. Operating System Selection

Ubuntu Server 24.04 LTS was chosen for this coursework because it is stable, well supported, and widely used in industry. The long-term support version provides regular security updates, which is important for a server environment.

Ubuntu Server also includes built-in tools such as OpenSSH, UFW, and AppArmor, which are required later in the coursework. Compared to other distributions like Debian or CentOS-based systems, Ubuntu offers a good balance between ease of use and reliability.

## 3. Workstation Configuration

The workstation system is my Windows laptop. Windows PowerShell is used as the SSH client to connect to the Ubuntu Server virtual machine. VirtualBox is used as the virtualisation platform.

This approach avoids the need for an additional Linux desktop virtual machine and keeps the setup simple while still meeting the coursework requirements.

## 4. Network Configuration

The Ubuntu Server virtual machine is configured using VirtualBox NAT networking. Port forwarding is enabled so that connections to port 2222 on the host machine are forwarded to port 22 on the server.

This configuration allows secure remote access to the server while keeping it isolated from the external network. NAT networking also allows the server to access the internet for updates.

![Network Configuration](assets/week1-network.png)

uname -a
assets/week1-uname.png

free -h
assets/week1-memory.png

df -h
assets/week1-disk.png

ip addr
assets/week1-network-info.png

lsb_release -a
assets/week1-os.png

## 5. Baseline System Information

The following command-line tools were used to document the initial system state.

### Kernel and System Information
```bash
uname -a

Memory Usage
free -h

Disk Usage
df -h

Network Interfaces
ip addr

Operating System Version
lsb_release -a

---

# 🅶 STEP G — Reflection 

Add this at the end:

```md
## 6. Reflection

This week helped me understand the importance of planning before configuring a server system. Setting up a headless Ubuntu Server and accessing it remotely showed how real servers are managed in practice. I also became more comfortable using basic Linux command-line tools, which will be important for the later stages of the coursework.

