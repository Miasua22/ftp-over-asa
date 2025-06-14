# FTP Server Setup Guide

This document explains how to set up an FTP server behind Cisco ASA for external access.

## 1. Install FTP Server

We tested with:

- **WingFTP** – Windows-based, supports multiple protocols
- **FileZilla Server** – Free and open source
- **CoreFTP Server** – Lightweight option

Basic steps:

1. Install the FTP server on a machine in the internal network (e.g., 192.168.1.100)
2. Configure **Passive Ports** (e.g., 50000–50100)
3. Set up a test user account

## 2. ASA Configuration (NAT + ACL)

- **Static NAT** from public IP to internal FTP server
- Allow TCP 21 (FTP command), and passive ports (e.g., TCP 50000–50100)
- Optional: Enable FTP inspection (or disable if causing issues)

## 3. DNS and DHCP

- DNS should resolve to ASA’s external IP
- DHCP provided from Cisco Switch

See `config/` folder for examples.

## 4. Test from External

Try connecting using:

- `ftp://your.public.ip` in FileZilla (Client)
- Ensure firewall rules are working
