# 🖥️ Windows Server Installation Guide

This guide walks through installing **Windows Server** inside a Virtual Machine (VM).  

---

## 🔧 Before You Start
- **VM Software**: Install [VirtualBox](https://www.virtualbox.org/) or [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html).  
- **ISO File**: Download a Windows Server ISO (e.g., Windows Server 2019 or 2022) from [Microsoft’s Evaluation Center](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022).  
- **Recommended VM Settings**:  
  - RAM: at least 4 GB (8 GB+ preferred)  
  - CPU: 2 cores or more  
  - Disk: 40 GB minimum (Dynamic disk is fine)  
  - Network: NAT (internet access) or Bridged (LAN access)  

---

## 📀 Installation Steps
1. **Start the VM** → select your Windows Server ISO to boot.  
2. Choose **Language / Time / Keyboard** → **Next → Install now**.  
3. **Select Edition**:  
   - *Standard (Desktop Experience)* = with GUI (recommended).  
   - *Standard (Server Core)* = command-line only, lightweight.  
4. **Accept License Agreement** → Next.  
5. **Installation Type** → choose **Custom (fresh install)**.  
6. Select the **Unallocated Disk** → Next.  
   - Setup will copy files and reboot several times.  
7. When prompted, set a **strong Administrator password**.  

---

## 🔑 First Login Setup
- Log in as **Administrator** with the password you created.  
- **Server Manager** will load automatically on first login.  

---

## 🔄 Apply Updates
1. Open **Settings → Windows Update**.  
2. Click **Check for updates** → install everything → reboot if needed.  
3. *(Optional but recommended)* Rename the server:  
   - **Server Manager → Local Server → Computer name → Change…**  
   - Example: `Active-Directory` → reboot to apply.  

---

## 🛡 Quick Hardening Baseline
- **Windows Defender Firewall**: verify Domain, Private, and Public profiles are **On**.  
- **Windows Update**: keep **Automatic Updates** enabled.  
- **Local Security Policy** (`secpol.msc`):  
  - Minimum password length: **12 characters**  
  - Password complexity: **Enabled**  
  - Account lockout threshold: **5 attempts**  

---

## 🖼 Screenshots

<p align="center">
  <img src="https://github.com/user-attachments/assets/3fb4d9df-73b0-41fd-b8a3-bf85a421d41b" width="80%" alt="Wireshark Conversations" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/7ba5dfe7-947d-4d0a-882c-983b99385589" width="80%" alt="HTTP Stream Analysis" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/e7d522f2-a551-4777-abb4-e9234c233c94" width="80%" alt="DNS Query Example" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/2c1597db-8a1f-4444-976b-04d104cddcc1" width="80%" alt="DNS Query Example" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/c2d1e37c-db46-46d8-9733-9aacc7f279f8" width="80%" alt="DNS Query Example" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/f76e0272-f04b-4076-a785-7334ff062dfd" width="80%" alt="DNS Query Example" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/bab6c91a-c885-4009-9e8c-b1867fc1049b" width="80%" alt="DNS Query Example" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/2c62534f-a0f4-4b75-a2ca-9dbfea8a64e0" width="80%" alt="DNS Query Example" />  
  <br><br>
</p>

---
