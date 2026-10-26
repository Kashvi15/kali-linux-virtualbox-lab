# Kali Linux VirtualBox Lab

## Overview
This repository documents my NetworkWalks Week 1 cybersecurity lab setup using Kali Linux and Oracle VirtualBox. It covers virtual networking, file sharing, clipboard integration, and troubleshooting.

## Lab Environment
- **Host OS:** Windows
- **Virtualization:** Oracle VirtualBox
- **Guest OS:** Kali Linux
- **Network:** VirtualBox NAT Network
- **Subnet:** `10.0.0.0/24`

## Setup and Configuration
- Installed and configured Kali Linux in VirtualBox.
- Configured the virtual network and verified internet connectivity.
- Enabled bidirectional shared clipboard and drag-and-drop.
- Shared the Windows Downloads folder with Kali Linux.
- Verified that files could be accessed through the shared folder.

## Troubleshooting

### 1. Internet Connectivity
After restarting the virtual machine, internet connectivity was lost.

**Troubleshooting performed:**
- Inspected network interfaces using `ip a`.
- Checked routing information using `ip route`.
- Examined NetworkManager connection status with `nmcli`.
- Activated the `Wired connection 1` profile.
- Verified connectivity using `ping 8.8.8.8` and `ping google.com`.
- Successfully ran `sudo apt update`.

### 2. Drag-and-Drop
Drag-and-drop initially did not work despite enabling bidirectional mode.

**Troubleshooting performed:**
- Checked VirtualBox drag-and-drop settings.
- Verified VirtualBox Guest Additions modules.
- Checked and restarted the VBoxClient drag-and-drop process.
- Tested file transfers between Windows and Kali Linux.

File transfer was subsequently verified using the shared folder and drag-and-drop workflow.

## Useful Commands

```bash
ip a
ip route
nmcli device status
ping -c 4 8.8.8.8
ping -c 4 google.com
sudo apt update
```

## Learning Outcomes
- Practised basic Linux networking commands.
- Learned to inspect network interfaces and routes.
- Gained experience troubleshooting VirtualBox networking.
- Configured shared folders and host-to-guest file transfer.
- Learned the importance of testing and verifying fixes.

## Disclaimer
This repository documents my learning and lab configuration. All future security testing will be performed in authorised, controlled environments.