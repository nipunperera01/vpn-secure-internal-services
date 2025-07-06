# VPN-Secured Internal Services (OpenVPN Project)

This project demonstrates how to set up a secure remote access solution using **OpenVPN** on an **Ubuntu Server**. Internal services like **Apache2 (web server)** and **SSH** are made accessible **only** through the VPN, secured with strict **UFW firewall rules**.

---

## 📌 Key Objectives

- Deploy OpenVPN server on Ubuntu
- Generate and distribute `.ovpn` client configs
- Restrict internal services to VPN clients using UFW
- Verify access through different network paths

---

## 🧠 Why This Matters

🔒 Organizations often expose sensitive services to internal users only.  
A VPN ensures **private, encrypted access** to critical services (web, SSH) over public or untrusted networks.

This project is a **real-world simulation** of secure remote access used in industry.

---

## ⚙️ Tech Stack

- 🐧 Ubuntu Server 22.04 (VMware)
- 🌐 OpenVPN
- 🔥 UFW Firewall
- 📁 SCP for file transfer
- 🧪 Windows as VPN client

---

## 📷 Project Screenshots

| Feature                               | Screenshot                                 |
|--------------------------------------|--------------------------------------------|
| UFW Rules (VPN-only Access)          | ![ufw](screenshots/ufw-rules.png)          |
| VPN Client Connected                 | ![vpn](screenshots/vpn-client connected.png) |
| Web App Access via VPN               | ![web](screenshots/vpn-access.png)         |
| Access Blocked without VPN           | ![fail](screenshots/local-blocked.png)     |
| SCP Transfer of .ovpn file           | ![scp](screenshots/client1.ovpn file install to client using scp.png) |
| SSH Access within VPN                | ![ssh](screenshots/ssh connect-with vpn.png) |

---

## 📁 Folder Structure

.
├── client1.ovpn
├── screenshots/
│ ├── ufw-rules.png
│ ├── vpn-client connected.png
│ ├── vpn-access.png
│ ├── local-blocked.png
│ ├── ssh connect-with vpn.png
│ ├── client1.ovpn file install to client using scp.png
│ └── ovpn client file creation.png
└── README.md

---

## ✅ Outcome

After implementation:

✅ Web and SSH access are **only available** through VPN IP `10.8.0.0/24`  
❌ Local IP (e.g., `192.168.x.x`) is **denied**, even if users are on the same LAN

---

## 🧑‍💻 Author

**Nipun Perera**  
Network & Cybersecurity Enthusiast  
