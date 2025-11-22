# Setup-and-Use-a-Firewall-on-Windows-Linux
This project involves configuring a host-based firewall (such as Windows Defender or Linux UFW) to control network traffic. You will create custom inbound and outbound rules to strictly allow or block specific ports and services, effectively hardening the operating system against unauthorized network access and attacks
[Firewall Setup Readme.pdf](https://github.com/user-attachments/files/23690942/Firewall.Setup.Readme.pdf)
[firewall_setup_readme.md](https://github.com/user-attachments/files/23690946/firewall_setup_readme.md)
# Firewall Setup and Usage Guide (Windows & Linux)

## 📌 Objective
This guide explains how to **set up**, **configure**, and **use** a firewall on both **Windows** and **Linux** systems. It follows a lab-friendly step-by-step approach suitable for cybersecurity and system administration practice.

---

# 🛡️ 1. Understanding Firewalls
A firewall is a security tool that monitors and controls incoming and outgoing network traffic based on predefined security rules. It helps protect your system from unauthorized access and attacks.

---

# 🪟 Windows Firewall Setup

## ✅ Step 1: Open Windows Firewall
- Go to **Control Panel** → **System and Security** → **Windows Defender Firewall**.
- Or search **"Windows Defender Firewall"** in the Start Menu.

## ✅ Step 2: Turn Firewall On/Off
- Click **Turn Windows Defender Firewall on or off**.
- Ensure both **Private** and **Public** networks have the firewall **enabled**.

## ✅ Step 3: Allow an App Through Firewall
- Go to **Allow an app or feature through Windows Defender Firewall**.
- Click **Change settings**.
- Select which apps can communicate through the firewall.

## ✅ Step 4: Create Custom Inbound/Outbound Rules
1. Open **Windows Defender Firewall with Advanced Security**.
2. Navigate to:
   - **Inbound Rules** → New Rule
   - **Outbound Rules** → New Rule
3. Choose rule type:
   - Program
   - Port
   - Predefined
   - Custom
4. Define:
   - Port number (e.g., 80, 443, 3389)
   - Protocol (TCP/UDP)
   - Action (Allow/Block)
   - Profile (Domain/Private/Public)
5. Name and save the rule.

## 📝 Example Rule
- Block all incoming connections on **port 23 (Telnet)**.

---

# 🐧 Linux Firewall Setup (UFW & FirewallD)

## Option A: UFW (Ubuntu/Debian)
UFW = Uncomplicated Firewall (beginner‑friendly)

### ✅ Step 1: Install UFW (if not installed)
```
sudo apt install ufw
```

### ✅ Step 2: Enable UFW
```
sudo ufw enable
```

### ✅ Step 3: Allow/Block Specific Ports
```
sudo ufw allow 22
sudo ufw allow 80
sudo ufw deny 23
```

### ✅ Step 4: Check Status
```
sudo ufw status verbose
```

---

## Option B: FirewallD (CentOS/RHEL/Fedora)

### ✅ Step 1: Start FirewallD
```
sudo systemctl start firewalld
sudo systemctl enable firewalld
```

### ✅ Step 2: Allow/Block Ports
```
sudo firewall-cmd --add-port=22/tcp --permanent
sudo firewall-cmd --remove-port=23/tcp --permanent
```

### ✅ Step 3: Reload Firewall
```
sudo firewall-cmd --reload
```

### ✅ Step 4: View Active Rules
```
sudo firewall-cmd --list-all
```

---

# 📋 Documentation Section
(Use for a report or GitHub repo)

### 🔍 What You Did
- Enabled firewall on Windows/Linux.
- Created inbound/outbound rules.
- Allowed and blocked ports.
- Verified firewall status.

### 📸 Screenshots to Include (optional):
- Windows Firewall main dashboard
- Custom rule creation
- UFW status output
- FirewallD active rules

---

# 🛡️ Summary
| Feature | Windows Firewall | Linux UFW | Linux FirewallD |
|--------|------------------|-----------|------------------|
| Beginner-friendly | Yes | Yes | Moderate |
| GUI available | Yes | No | No |
| Command-line support | Yes | Yes | Yes |
| Best for | Personal PCs | Ubuntu systems | Enterprise Linux servers |

Firewalls play a critical role in system hardening and prevent unauthorized access, brute-force attacks, and malicious connections.

---

If you want, I can also create **screenshots placeholders**, **a lab report format**, or **convert this into a PDF**.

