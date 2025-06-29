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
## 🔎 Observations

- **UFW Status:** Enabled  
- **Logging Level:** Low  

- **Default Policies:**  
  - **Incoming Traffic:** Denied  
  - **Outgoing Traffic:** Allowed  

- **Firewall Rules Applied:**  
  - ✅ Blocked **Port 23 (Telnet)** – Confirmed with a refused connection  
  - ✅ Allowed **Port 22 (SSH)** – Ensures secure remote access  

- **Web Access:**  
  - Outbound traffic to **Ports 80 (HTTP)** and **443 (HTTPS)** is permitted  

- **Conclusion:**  
  The firewall is effectively filtering traffic based on the defined rules, helping secure the system by preventing unauthorized access while allowing necessary communication channels.

---

## ✅ Summary

In this task, UFW (Uncomplicated Firewall) was configured and tested on a Kali Linux system to manage network traffic securely. Basic rules were applied to block unauthorized services like Telnet and allow essential services such as SSH. The firewall's default policy was set to deny all incoming and allow all outgoing traffic, providing a solid baseline security posture. The tests confirmed that the firewall rules were enforced effectively, showcasing UFW’s ease of use and practical application in real-world scenarios for system protection.
