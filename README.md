# 🛠️ IT Support Automation Toolkit (PowerShell)

## 📌 Project Overview
In a corporate environment, L1/L2 Support Engineers spend significant time on repetitive diagnostic and maintenance tasks. This **PowerShell-based automation toolkit** was developed to streamline these workflows, reducing the **Mean Time to Resolution (MTTR)** for common performance and connectivity issues.

---

## 🚀 Key Modules & Functionality
- **🔍 System Health Audit:** Leverages **CIM/WMI instances** to instantly report CPU specs, total RAM, and OS version, assisting in rapid hardware assessment.
- **🧹 Disk Maintenance:** Automates the purging of system and user temporary caches to resolve "System Sluggishness" tickets.
- **🌐 Network Stack Reset:** Executes a one-click refresh of the TCP/IP stack (DNS Flush, IP Release/Renew) to fix 50% of connectivity issues.
- **⚙️ Modular Design:** Built using reusable function blocks, demonstrating structured programming and scalability.

---

## 🛠️ Technical Stack
* **Language:** PowerShell (Core/Desktop)
* **Management:** Windows Management Framework (WMF)
* **Tools:** Git, GitHub, Windows CLI
* **Concepts:** ITIL-aligned automation, Principle of Least Privilege (Security)

---

## 📖 How to Run (Security Best Practices)
To maintain system integrity, this script should be run without permanently altering the system's global security policy. Use the following methods:

### 1. The One-Time Bypass (Recommended)
This bypasses the execution policy **only for this specific run**:
```powershell
powershell.exe -ExecutionPolicy Bypass -File .\MaintenanceToolkit.ps1

```

## ⚡ Method 2: The "One-Shot" Execution (Pro Method)
This is the most efficient method for rapid deployment on any workstation without manual downloading. It fetches the latest code directly from this repository and executes it in memory (**Fileless Execution**).

**Instructions:** Open an **Administrative PowerShell** window and run:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]::Tls12; iex (New-Object System.Net.WebClient).DownloadString('[https://raw.githubusercontent.com/gaganbisen08/IT-Automation-Toolkit/main/MaintenanceToolkit.ps1](https://raw.githubusercontent.com/gaganbisen08/IT-Automation-Toolkit/main/MaintenanceToolkit.ps1)')
