# Cloud Computing Lab 01

**Name:** Zuha Irfan  
**Reg No:** 2023-BSE-073  
**Class:** BSE-5B  
**Subject:** Cloud Computing  
**Lab No:** 01  

---

## Task

### 1. Install VMware Workstation Pro
- Download and install VMware Workstation Pro on your system.

---

### 2. Download Ubuntu Server ISO
- Get the latest Ubuntu Server ISO file from the official website.

---

### 3. Create a New Virtual Machine in VMware
1. Open **VMware Workstation Pro**.
2. Click **Create a New Virtual Machine**.
3. Select **Typical (recommended)**.
4. When prompted for installation media:
   - Choose **Installer disc image file (ISO)**.
   - Browse and select the Ubuntu Server ISO.
5. Continue through the wizard using the default settings unless instructed otherwise.

---

### 4. Start the Virtual Machine
1. Click **Power on this virtual machine**.
2. The Ubuntu Server installer will boot using the ISO file.

Follow the installer steps:
- Select your **language**.
- Choose the **keyboard layout**.
- Select **installation options** using the spacebar to mark selections with `(x)`.
- Configure:
  - **Networking**
  - **Proxy**
  - **Ubuntu archive mirror**
  - **Storage guide** & **Storage configuration**
- Set up a **profile**.
- **Upgrade to Ubuntu Pro** (optional).
- Configure **SSH**.

---

### Common Installation Errors
If you face errors (e.g., APT package configuration failures), possible causes include:
1. Ubuntu Server file not unblocked.
2. No internet connection.
3. Bad mirror or unreachable repository.
4. Corrupted ISO file.
5. Insufficient disk space or partition errors.
6. Virtual machine misconfiguration (storage controller issues, etc.).

**Solution:**  
Check and fix issues one by one, then restart from **Step 4**.

---

### 5. Access Ubuntu Server from Windows
1. Find the IP address of your Ubuntu Server:
   ```bash
   ip addr

