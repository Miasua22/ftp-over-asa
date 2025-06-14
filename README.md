# FTP Over Cisco ASA 9.18

This project documents how to set up an FTP server that is externally accessible through a Cisco ASA 9.18 firewall. 
It includes full configuration of NAT, ACL, DHCP, and DNS, as well as testing with different FTP server software.

## 🔧 Environment

- **Firewall**: Cisco ASA 9.18
- **DHCP**: Configured on Cisco Switch
- **Tested FTP Software**:
  - WingFTP
  - FileZilla Server
  - CoreFTP Server

## 📁 Project Structure
ftp-over-asa/
├── README.md
├── ftp-server-setup.md
├── config/
│ ├── asa-config.txt
│ └── switch-dhcp.txt
├── test-results/
│ ├── filezilla.md
│ ├── wingftp.md
│ └── coreftp.md
└── troubleshooting.md


## 📡 Overview

This guide includes:

- ✅ ASA NAT + ACL configuration for FTP
- ✅ Passive port setup
- ✅ FTP server installation and setup
- ✅ Troubleshooting connection issues
- ✅ Testing with multiple FTP server software

## 📸 Network Diagram

To be added. It will show the FTP server behind ASA with static NAT and port forwarding.

---

Feel free to fork, use, or contribute!
