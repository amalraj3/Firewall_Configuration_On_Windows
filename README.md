# 🔐 Firewall_Configuration_On_Windows# 

To configure and test Windows Firewall rules that block and allow specific network traffic on designated ports, and demonstrate how firewall rules manage inbound traffic.

---

## 🛠 Tools & Environment

- **Operating System**: Windows 11 Home (64-bit)
- **Firewall Tool**: Windows Defender Firewall with Advanced Security (`wf.msc`)
- **Command-Line Tools**: PowerShell (`Test-NetConnection`)
- **Target Port**: TCP Port 23 (Telnet)

---

## 🔧 Steps Performed

### ✅ 1. Opened Firewall Management Tool
- Used `wf.msc` to open **Windows Defender Firewall with Advanced Security**

### ✅ 2. Reviewed Inbound Rules
- Navigated to **Inbound Rules**
- Verified current allowed and blocked ports

### ✅ 3. Created New Rule to Block Port 23
- **New Rule** → **Port** → TCP → Port 23 → **Block the connection**
- Applied to all profiles (Domain, Private, Public)
- Named: `Block Port 23 - Telnet`

### ✅ 4. Tested Port Accessibility via PowerShell
```powershell
Test-NetConnection -ComputerName localhost -Port 23
