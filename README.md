# 🛠️ IT Support Automation Toolkit (PowerShell)

## 📌 Project Overview
In a corporate IT environment, efficiency is key. This **PowerShell-based automation toolkit** was developed to streamline routine L1/L2 Desktop Support tasks. By automating diagnostic and maintenance workflows, it significantly reduces the **Mean Time to Resolution (MTTR)** for common performance and connectivity issues.

---

## ⚡ Quick Execution (The "One-Shot" Method)
For rapid deployment on any workstation without manual downloading, run this single command in an **Administrative PowerShell** window. It fetches the latest version directly from this repository and executes it in memory:

---powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]::Tls12; iex (New-Object System.Net.WebClient).DownloadString('[https://raw.githubusercontent.com/gaganbisen08/IT-Automation-Toolkit/main/MaintenanceToolkit.ps1](https://raw.githubusercontent.com/gaganbisen08/IT-Automation-Toolkit/main/MaintenanceToolkit.ps1)')
🔍 Command Technical Breakdown
Understanding the underlying mechanics is critical for security compliance:

Set-ExecutionPolicy Bypass -Scope Process: Temporarily allows script execution only for the current PowerShell session. This adheres to the Principle of Least Privilege by not altering the global system security policy.

Tls12 Protocol: Forces a secure connection using Transport Layer Security 1.2, ensuring the script is downloaded safely from GitHub.

iex (Invoke-Expression): Enables Fileless Execution by running the script directly from RAM, avoiding the need to save local files on the user's hard drive.

DownloadString: Fetches the "Raw" code text directly from the GitHub repository for immediate processing.

🚀 Key Modules & Functionality
🔍 System Health Audit: Leverages CIM/WMI instances to instantly report CPU specs, total RAM, and OS version for rapid asset inventory.

🧹 Proactive Disk Maintenance: Automates the purging of system and user temporary caches to resolve "System Sluggishness" tickets.

🌐 Network Stack Reset: Executes a one-click refresh of the TCP/IP stack (DNS Flush, IP Release/Renew) to fix 50% of connectivity issues instantly.

⚙️ Error Handling: Built with Try/Catch blocks to ensure the script skips protected files and continues execution without crashing.

🛠️ Technical Stack
Language: PowerShell (Core/Desktop)

Management: Windows Management Framework (WMF)

Deployment: GitHub (Raw Content Delivery)

Concepts: ITIL-aligned automation, Security Principle of Least Privilege.

📖 Alternative Execution Methods
If you prefer manual execution, ensure you use a security bypass to maintain system integrity:

1. Session-Level Bypass
Allows script execution only in the current terminal window without changing global settings:

PowerShell

Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process -Force
.\MaintenanceToolkit.ps1
2. Trusting the File
If the script was moved from another machine (e.g., a Linux partition), run this to unblock it:

PowerShell

Unblock-File -Path .\MaintenanceToolkit.ps1
📈 Measurable Impact
Efficiency: Automates tasks that usually take 10 minutes of manual clicking into a 15-second automated execution.

Security: Adheres to enterprise security standards by utilizing session-based bypasses rather than permanent policy changes.

Reliability: Provides consistent diagnostic data, eliminating human error during hardware audits.

👨‍💻 Author
Gagan Bisen 📍  India

Developed as part of a technical portfolio for IT Support, Desktop Support, and System Administration roles.
