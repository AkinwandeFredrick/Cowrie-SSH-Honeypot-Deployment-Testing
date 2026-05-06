# Cowrie-SSH-Honeypot-Deployment-Testing

# Cowrie SSH Honeypot Deployment & Testing

**Report ID:** HONEYPOT-2026-0506-01  
**Date:** 06 May 2026  
**Author:** Akinwande Fredrick

## Executive Summary

Successfully deployed a **Cowrie SSH honeypot** on a VMware virtual machine for security research and attacker behavior analysis.

A reconnaissance scan from a Kali Linux machine confirmed the honeypot is operational, correctly emulating a legitimate OpenSSH server on port **2222**.

---

## System Details

| Parameter              | Value                                      |
|------------------------|--------------------------------------------|
| Host IP Address        | `192.168.1.32`                             |
| MAC Address            | `00:0C:29:15:80:C2`                        |
| Virtualization         | VMware Virtual Platform                    |
| Honeypot Software      | Cowrie v2.9.19.dev3+g23fcef400             |
| Listening Port         | TCP/2222                                   |
| Emulated Service       | OpenSSH 9.2p1 Debian 2+deb12u3             |
| Operating System       | Linux (Debian emulation)                   |

## Scan Summary

**Tool:** Nmap 7.99  
**Command:**
```bash
nmap -sV -p 2222 -Pn -oA cowrie_scan 192.168.1.32
