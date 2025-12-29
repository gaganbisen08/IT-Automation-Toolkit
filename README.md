# 🛠️ Automated IT Maintenance & Troubleshooting Toolkit

## 📌 Project Overview
A modular **PowerShell** automation script designed to streamline routine Desktop Support maintenance and diagnostic tasks. This toolkit was built to reduce the time spent on repetitive manual troubleshooting, such as clearing system caches, auditing hardware specs, and resetting network configurations.

---

## 🚀 Key Features
- **System Health Audit:** Generates a quick report of the Computer Name, CPU model, and Total RAM.
- **Automated Disk Maintenance:** Purges temporary files and system caches to free up disk space.
- **Network Stack Reset:** Flushes DNS and refreshes IP configurations to resolve 50% of "No Internet" support tickets in one click.
- **Error Handling:** Designed to skip protected files without crashing the script.

---

## 🛠️ Technical Skills Demonstrated
* **Scripting & Automation:** Windows PowerShell (Core/Desktop).
* **System Administration:** Managing Windows file systems and registry (temp files).
* **Networking:** TCP/IP stack management and DNS troubleshooting.
* **Documentation:** Clear technical writing for end-user or technician use.

---

## 📥 How to Use
1. **Prerequisite:** Open PowerShell as **Administrator**.
2. **Enable Scripts:** Run the following command if scripts are blocked:
   ```powershell
   Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
