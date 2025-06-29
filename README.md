# firewall-configuration-task4
# 🔐 Cyber Security Internship - Task 4: Firewall Configuration

## 📌 Task Overview

**Objective:**  
Configure and test basic firewall rules using UFW (Uncomplicated Firewall) on a Linux system to control network traffic.

**Tools Used:**  
- Kali Linux  
- UFW (Uncomplicated Firewall)

---

## 🧪 Steps Performed

### ✅ 1. Enabled UFW:
```bash
sudo ufw enable
```
Enables the firewall and activates default rules.
### ✅ 2. Checked Firewall Status (Verbose):
```bash
sudo ufw status verbose
```
Displays current firewall rules, default policies, and logging level.
### ✅ 3. Added Rule to Block Telnet (Port 23):
```bash
sudo ufw deny 23
```
Blocks all incoming connections to port 23 (Telnet).
### ✅ 4. Tested Telnet Block Rule:
```bash
telnet localhost 23
```
Result: Connection refused, confirming the firewall rule is effective.
### ✅ 5. Allowed SSH (Port 22):
```bash
sudo ufw allow 22
```
Allows incoming SSH connections, which is essential for remote administration.
### ✅ 6. Removed Telnet Block Rule:
```bash
sudo ufw delete deny 23
```
Restores original state by removing the test block rule on port 23.
### ✅ 7. Final Firewall Status:
```bash
sudo ufw status verbose
```

🔎 Observations
   ` UFW is enabled and logging is set to low.`
   ` Default policy:`
        Incoming traffic: Denied
        Outgoing traffic: Allowed
    Firewall rules successfully:
        Blocked port 23 (Telnet)
        Allowed port 22 (SSH)
    Outbound traffic on ports 80 and 443 is permitted (web access).
    Firewall effectively filters traffic based on defined rules, helping protect the system      from unauthorized access.
