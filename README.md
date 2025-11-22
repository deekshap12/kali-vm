# kali-vm
This release contains the exported Kali Linux VirtualBox VM (.ova file).   You can download the OVA file and import it directly into Oracle VirtualBox to use the preconfigured Kali Linux environment.
# Kali Linux VirtualBox VM

![Kali Linux Logo](https://www.kali.org/images/kali-logo.svg)

## Overview
This repository contains a **pre-configured Kali Linux VirtualBox VM** (`.ova` file) for ethical hacking, penetration testing, and cybersecurity learning.  
It allows you to quickly get started without manually installing the OS or configuring the environment.

---

## System Requirements
- **Operating System:** Windows, macOS, or Linux  
- **Oracle VirtualBox:** Version 7.0 or later ([Download here](https://www.virtualbox.org/wiki/Downloads))  
- **RAM:** Minimum 2 GB (8 GB recommended)  
- **Disk Space:** At least 20 GB free  
- **CPU:** Virtualization enabled in BIOS/UEFI  

---

## Download
The `.ova` file is available in the **[Releases](https://github.com/your-username/your-repo/releases)** section.  
> **Tip:** If the file is compressed (`.zip`), extract it before importing into VirtualBox.

---

## Installation & Setup

### Step 1 — Install Oracle VirtualBox
1. Download VirtualBox for your operating system.  
2. Run the installer and follow the on-screen instructions.  
3. (Optional) Install the **VirtualBox Extension Pack** for additional features like USB 3.0 support.

### Step 2 — Import the VM
1. Open **Oracle VirtualBox**.  
2. Click **File → Import Appliance**.  
3. Select the downloaded `.ova` file.  
4. Click **Next**, review VM settings (RAM, CPU, disk, network).  
5. Click **Import** and wait for the process to finish.

### Step 3 — Start the VM
1. Select your imported Kali VM in VirtualBox.  
2. Click **Start**.  
3. Login credentials (default):
Username: kali
Password: kali 

---

## Post-Import Setup

### Update the System
Open a terminal in Kali and run:

```bash
sudo apt update && sudo apt upgrade -y

Install Guest Additions (Optional)
Enables full-screen, shared clipboard, and shared folders.
VirtualBox menu → Devices → Insert Guest Additions CD image → follow instructions.

Configure Network
VirtualBox supports several network modes:
NAT (default): VM can access the internet, but the host cannot access the VM directly.
Bridged Adapter: VM appears as a separate device on your local network.
Host-Only Adapter: VM can communicate only with the host machine.

To configure:
VirtualBox → Settings → Network → Adapter 1
Choose the desired network mode
Click OK

Verify network inside VM:
ip a          # check IP addresses
ping google.com  # test internet connectivity

Usage
Ideal for security labs, penetration testing, and cybersecurity practice.
Take snapshots before making major changes.
Only run hacking tools on networks you own or have permission to test.

Optional Tips
Allocate extra RAM and CPU for better performance.
Use snapshots to save VM states regularly.
Refer to VirtualBox User Manual for troubleshooting.

License
This VM and repository are provided for educational and ethical purposes only. Use responsibly.

Contact
For questions, issues, or suggestions, open an issue in this repository or contact the maintainer.


